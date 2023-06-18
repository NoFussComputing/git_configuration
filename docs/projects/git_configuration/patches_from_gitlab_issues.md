---
title: Create merge request from patch files found in gitlab issues
description: How to use No Fuss Computings Ansible role git configuration; automation to create merge requests from patch files found within gitlab issue comments/uploaded.
date: 2023-06-18
template: project.html
about: https://gitlab.com/nofusscomputing/projects/ansible/git_configuration
---

This task file is used to create merge requests in GitLab based on the patches found in GitLab issue comments. It includes a block with minimum required variables and an `include_tasks` task to execute the `gitlab_apply_issue_patch.yaml` playbook. The `gitlab_api_token` variable is defined using the value from `role_git_conf.gitlab.api_token`. The task is tagged with `always` to ensure it is always executed.


## Automation Structure

This task includes the `gitlab_apply_issue_patch.yaml` playbook using the `ansible.builtin.include_tasks` module. It applies the playbook with the `always` tag. The playbook is responsible for creating merge requests based on the patches found in the GitLab issue comments.

The `gitlab_api_token` variable must be defined as is also required, variable `project_path`.


### Tags

This task is tagged with `always` to ensure it is always executed. however, to run the automation you must specify tag `gitlab_issue_patches`


### Condition

The task is conditionally executed based on the presence of the `gitlab_issue_patches` tag in the `ansible_run_tags` variable. If the tag is present, the task is executed.


### Inventory

The playbook does not require an inventory as it operates on the specified GitLab repository and merge requests.


## Task file: gitlab_apply_issue_patch.yaml

This task file is used to apply patches to the specified repository and merge requests in GitLab. It includes tasks for downloading patches, applying them, pushing the changes to the patch branch, replying to the patch thread, removing the patch from the user's comment, and updating the merge request description. The playbook also includes tasks for collecting telemetry data and debugging.

The task file collects telemetry data by setting the `task_finish_epoch` and `task_duration_ansible` facts. These facts capture the start and end timestamps of each task's execution, allowing for the calculation of task durations.


### Structure

The task file consists of the following tasks:

1. **Include Tasks: Download Patch Files**

   This task includes the `gitlab/issues.yaml` task file to download the patch files specified in the `gitlab_issue_patch_files` variable.

2. **Apply Patches Found**

   This task includes the `git/patch.yaml` task file to apply the patches found.

3. **Push the changes to the patch branch - {{ task_item.branch_name }}**

   This task includes the `git/repository.yaml` task file to push the changes to the patch branch.

4. **Reply to patch thread**

   This task includes the `gitlab/notes.yaml` task file to reply to the patch thread.

5. **Remove the patch from the user's comment so it doesn't get picked up anymore**

   This task includes the `gitlab/notes.yaml` task file to remove the patch from the user's comment.

6. **Telemetry fact**

   This task sets the `task_finish_epoch` fact using the `ansible.builtin.set_fact` module.

7. **Final Telemetry facts**

   This task sets the `task_duration_ansible` fact using the `ansible.builtin.set_fact` module.

8. **Comment on Merge Request**

   This task includes the `gitlab/notes.yaml` task file to comment on the merge request.

9. **Update Merge Request**

    This task includes the `gitlab/merge_request.yaml` task file to update the merge request, this includes creating one if it doesn't exist.

10. **Telemetry fact**

    This task sets the `task_finish_epoch` fact using the `ansible.builtin.set_fact` module.

11. **Final Telemetry facts**

    Cleans any variable from the task no longer required.


### Task: Initial Telemetry facts

- **Name**: Initial Telemetry facts

- **Description**: Sets initial telemetry facts including the task duration and start epoch.

- **Module**: ansible.builtin.set_fact

- **Arguments**:

  - `task_duration_human`: Sets the time it takes for a human to delete a CI/CD job, which is 900 seconds.

  - `task_start_epoch`: Sets the start epoch using the current Ansible date and time.

- **Conditional**: None

- **Tags**: None


### Task: Gitlab CI Detection

- **Name**: Gitlab CI Detection

- **Description**: Sets facts related to GitLab CI environment variables.

- **Module**: ansible.builtin.set_fact

- **Arguments**:

  - `project_path`: Sets the GitLab project path using the CI_PROJECT_PATH environment variable.

  - `gitlab_api_token`: Sets the GitLab API token using the GIT_COMMIT_TOKEN environment variable.

  - `repo_root`: Sets the repository root directory using the CI_PROJECT_DIR environment variable.

  - `gitlab_job_number`: Sets the GitLab job number using the CI_JOB_ID environment variable.

  - `gitlab_job_url`: Sets the GitLab job URL using the CI_JOB_URL environment variable.

- **Conditional**: Executes the task only if the CI environment variable is present.

- **Tags**: None


### Task: Gitlab include repository config file

- **Name**: Gitlab include repository config file

- **Description**: Includes the repository config file if running in a GitLab CI environment.

- **Module**: ansible.builtin.include_vars

- **Arguments**:

  - `file`: Specifies the path to the repository config file (`.nfc_automation.yaml`) in the repo root directory.

- **Conditional**: Executes the task only if the CI environment variable is present.

- **Tags**: None


### Task: Gitlab CI config Expansion to cover required variables

- **Name**: Gitlab CI config Expansion to cover required variables

- **Description**: Sets facts related to GitLab CI config variables to cover required variables for subsequent tasks.

- **Module**: ansible.builtin.set_fact

- **Arguments**:

  - `temp_repo_creation_directory`: Sets the temporary repository creation directory using the repo_root variable.

  - `default_branch`: Sets the default branch using the role_git_conf.gitlab.default_branch variable. If not defined, the value is omitted.

  - `merge_request_labels`: Sets the merge request labels using the role_git_conf.gitlab.merge_request.patch_labels variable. If not defined, the value is omitted.

- **Conditional**: Executes the task only if the CI environment variable is present.

- **Tags**: None


### Task: Fetch Gitlab issues with patch

- **Name**: Fetch Gitlab issues with patch

- **Description**: Includes the gitlab/issue_patches.yaml task file to fetch GitLab issues with patches.

- **Module**: ansible.builtin.include_tasks

- **Arguments**:

  - `file`: Specifies the path to the gitlab/issue_patches.yaml task file.

  - `apply.tags`: Specifies the tags to apply to the included tasks.

- **Conditional**: Always executed.

- **Tags**: Always


### Task: Debug Gitlab issue patch files

- **Name**: Debug Gitlab issue patch files

- **Description**: Prints the gitlab_issue_patch_files variable for debugging purposes.

- **Module**: ansible.builtin.debug

- **Arguments**:

  - `msg`: Specifies the message to be printed, which includes the value of the gitlab_issue_patch_files variable.

- **Conditional**: None

- **Tags**: None


### Task: Local Repository Setup default branch

- **Name**: Local Repository Setup default branch - {{ default_branch }}

- **Description**: Includes the git/repository.yaml task file to set up the local repository for the default branch.

- **Module**: ansible.builtin.include_tasks

- **Arguments**:

  - `file`: Specifies the path to the git/repository.yaml task file.

  - `apply.tags`: Specifies the tags to apply to the included tasks.

- **Conditional**: Executes the task only if gitlab_issue_patch_files variable is not empty.

- **Tags**: Always


### Task: Download All Patches, {{ gitlab_issue_patch_files | length }} Found

- **Name**: Download All Patches, {{ gitlab_issue_patch_files | length }} Found

- **Description**: Includes the git/patch.yaml task file to download all the patches found.

- **Module**: ansible.builtin.include_tasks

- **Arguments**:

  - `file`: Specifies the path to the git/patch.yaml task file.

  - `apply.tags`: Specifies the tags to apply to the included tasks.

- **Conditional**: Executes the task only if gitlab_issue_patch_files variable is not empty and the author's project membership level is greater than or equal to patch_file_minimum_access_level.

- **Tags**: Always


### Task: Create the patch branch - {{ task_item.branch_name }}

- **Name**: Create the patch branch - {{ task_item.branch_name }}

- **Description**: Includes the git/repository.yaml task file to create the patch branch.

- **Module**: ansible.builtin.include_tasks

- **Arguments**:

  - `file`: Specifies the path to the git/repository.yaml task file.

  - `apply.tags`: Specifies the tags to apply to the included tasks.

- **Conditional**: Executes the task only if gitlab_issue_patch_files variable is not empty and the author's project membership level is greater than or equal to patch_file_minimum_access_level.

- **Tags**: Always


### Task: Push the patch branch - {{ task_item.branch_name }}

- **Name**: Push the patch branch - {{ task_item.branch_name }}

- **Description**: Includes the git/repository.yaml task file to push the patch branch.

- **Module**: ansible.builtin.include_tasks

- **Arguments**:

  - `file`: Specifies the path to the git/repository.yaml task file.

  - `apply.tags`: Specifies the tags to apply to the included tasks.

- **Conditional**: Executes the task only if gitlab_issue_patch_files variable is not empty and the author's project membership level is greater than or equal to patch_file_minimum_access_level.

- **Tags**: Always


### Task: Create the Merge Requests

- **Name**: Create the Merge Requests

- **Description**: Includes the gitlab/merge_request.yaml task file to create merge requests.

- **Module**: ansible.builtin.include_tasks

- **Arguments**:

  - `file`: Specifies the path to the gitlab/merge_request.yaml task file.

  - `apply.tags`: Specifies the tags to apply to the included tasks.

- **Conditional**: Executes the task only if gitlab_issue_patch_files variable is not empty and the author's project membership level is greater than or equal to patch_file_minimum_access_level.

- **Tags**: Always


### Task: Filter patch files

- **Name**: Filter patch files

- **Description**: Executes a shell command to filter patch files based on certain conditions.

- **Module**: ansible.builtin.shell

- **Arguments**:

  - `cmd`: Specifies the shell command to execute.

  - `executable`: Specifies the shell executable to use.

- **Registered Variable**: gitlab_issue_patch_files_add_mr

- **Conditional**: None

- **Tags**: None


### Task: Apply Patches Found

- **Name**: Apply Patches Found

- **Description**: Includes the git/patch.yaml task file to apply the patches found.

- **Module**: ansible.builtin.include_tasks

- **Arguments**:

  - `file`: Specifies the path to the git/patch.yaml task file.

  - `apply.tags`: Specifies the tags to apply to the included tasks.

- **Conditional**: None

- **Tags**: git_patch_download


### Task: Push the changes to the patch branch - {{ task_item.branch_name }}

- **Name**: Push the changes to the patch branch - {{ task_item.branch_name }}

- **Description**: Includes the git/repository.yaml task file to push the changes to the patch branch.

- **Module**: ansible.builtin.include_tasks

- **Arguments**:

  - `file`: Specifies the path to the git/repository.yaml task file.

  - `apply.tags`: Specifies the tags to apply to the included tasks.

- **Conditional**: None

- **Tags**: Always


### Task: Reply to patch thread

- **Name**: Reply to patch thread

- **Description**: Includes the gitlab/notes.yaml task file to reply to the patch thread.

- **Module**: ansible.builtin.include_tasks

- **Arguments**:

  - `file`: Specifies the path to the gitlab/notes.yaml task file.

  - `apply.tags`: Specifies the tags to apply to the included tasks.

- **Conditional**: None

- **Tags**: Always


### Task: Remove the patch from the users comment so it doesn't get picked up anymore

- **Name**: Remove the patch from the users comment so it doesn't get picked up anymore

- **Description**: Includes the gitlab/notes.yaml task file to remove the patch from the user's comment.

- **Module**: ansible.builtin.include_tasks

- **Arguments**:

  - `file`: Specifies the path to the gitlab/notes.yaml task file.

  - `apply.tags`: Specifies the tags to apply to the included tasks.

- **Conditional**: None

- **Tags**: Always


### Task: Telemetry fact

- **Name**: Telemetry fact

- **Description**: Sets the task_finish_epoch fact using the ansible.builtin.set_fact module.

- **Module**: ansible.builtin.set_fact

- **Arguments**:

  - `task_finish_epoch`: Specifies the value to set for the fact.

- **Conditional**: None

- **Tags**: None


### Task: Final Telemetry facts

- **Name**: Final Telemetry facts

- **Description**: Sets the task_duration_ansible fact using the ansible.builtin.set_fact module.

- **Module**: ansible.builtin.set_fact

- **Arguments**:

  - `task_duration_ansible`: Specifies the value to set for the fact.

- **Conditional**: Executes the task only if gitlab_issue_patch_files variable is not empty and the length of gitlab_issue_patch_files is greater than 1.

- **Tags**: None


### Task: Comment on Merge Request

- **Name**: Comment on Merge Request

- **Description**: Includes the gitlab/notes.yaml task file to comment on the merge request.

- **Module**: ansible.builtin.include_tasks

- **Arguments**:

  - `file`: Specifies the path to the gitlab/notes.yaml task file.

  - `apply.tags`: Specifies the tags to apply to the included tasks.

- **Conditional**: None

- **Tags**: Always


## Automation Variables

The task expects the following variables to be defined:

- `gitlab_api_token`: The GitLab API token used for authentication. 

- `project_path`: The Gitlab project path to run this task on


## Tags

The role uses the following tags for the automation task to run:

- `gitlab_issue_patches`


## Usage

To use this automation, follow these steps:

1. Make sure you have the necessary dependencies and Ansible installed on your system.

2. Update the `gitlab_api_token` variable in your playbook or inventory file with the appropriate value for your GitLab API token.

3. Ensure that the `gitlab_apply_issue_patch.yaml` playbook is available in the same directory or path specified.

4. Include this task file in your Ansible playbook or role by using the `include_tasks` module with the appropriate file path.

5. Run your playbook, and the task will create merge requests based on the patches found in the GitLab issue comments.

   **Example Playbook:**

   ```yaml
   - name: Example Playbook
     hosts: servers
     tasks:
       - name: Include Create Merge Requests task file
         include_tasks: gitlab_apply_issue_patch.yaml.yaml
         vars:
            gitlab_api_token: The GitLab API token used for authentication. 
            project_path: the gitlab project path
   ```

   **Example Role:**

   ```yaml
   - name: Example Role
     hosts: servers
     roles:
       - role: my_role
         tasks_from: gitlab_apply_issue_patch.yaml.yaml
            gitlab_api_token: The GitLab API token used for authentication. 
            project_path: the gitlab project path
   ```
