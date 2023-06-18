---
title: Patch Task file
description: How to use No Fuss Computings Ansible role git configuration; task file repository for gitlab projects.
date: 2023-06-18
template: project.html
about: https://gitlab.com/nofusscomputing/projects/ansible/git_configuration
---

This Ansible task file performs various operations related to managing a Git repository. It includes tasks for cleaning the repository, cloning the repository, setting Git user details, creating a new branch, checking the current branch, and pushing a branch.


## Task 1: Facts - Task Variables

- **Name**: Facts - Task Variables

- **Description**: Sets the `repo_root` variable as the repository root directory.

- **Module**: `ansible.builtin.set_fact`

- **Arguments**:

  - `repo_root`: The path to the repository root directory.

- **Tags**: None


## Task 2: Clean Repository

- **Name**: clean

- **Description**: Cleans the repository by removing the repository root directory.

- **Module**: `ansible.builtin.file`

- **Arguments**:

  - `path`: The path to the repository root directory.

  - `mode`: The mode of the directory (directory).

  - `state`: Specifies the desired state of the directory, which is "absent" to remove it.

- **Conditional**: The task is only executed when the `gitlab_api_token` and `project_path` variables are defined.

- **Tags**:

  - git

  - git_clone

  - git_clone_branch_default


## Task 3: Clone Repository to Default Branch

- **Name**: Clone Repository to default branch

- **Description**: Clones the repository to the default branch.

- **Module**: `ansible.builtin.command`

- **Arguments**:

  - `cmd`: The Git command to clone the repository to the default branch.

- **Registers**: `git_clone_branch_default`

- **Conditional**: The task is only executed when the `gitlab_api_token` and `project_path` variables are defined.

- **Tags**:

  - git

  - git_clone

  - git_clone_branch_default


## Task 4: Update Git Submodules on Default Branch

- **Name**: Update git submodules init default branch

- **Description**: Updates the Git submodules on the default branch.

- **Module**: `ansible.builtin.shell`

- **Arguments**:

  - `cmd`: The shell command to fetch all, update submodules, and update submodules recursively.

- **Registers**: `git_clone_branch_default_submodule_init`

- **Tags**:

  - git

  - git_clone

  - git_clone_branch_default

  - git_clone_branch_default_submodule_init


## Task 5: Set Git User Details

- **Name**: Set Git User details

- **Description**: Sets the Git user's email or name for the repository.

- **Module**: `ansible.builtin.command`

- **Arguments**:

  - `cmd`: The Git command to set the user's email or name.

- **Registers**: `git_user_set_email`, `git_user_set_name`

- **Conditional**: The task is only executed when `repo_root` is defined.

- **Tags**:

  - git

  - git_user

  - git_user_set

  - git_user_set_email


## Task 6: Check Remote for Existing Branch

- **Name**: check remote for existing branch {{ git_branch_name }}

- **Description**: Checks if the specified branch already exists in the remote repository.

- **Module**: `ansible.builtin.command`

- **Arguments**:

  - `cmd`: The bash command to check if the branch exists in the remote repository.

- **Registers**: `git_branch_existing`

- **Conditional**: The task is only executed when `git_branch_name` is not empty.

- **Tags**:

  - git

  - git_branch

  - git_branch_create

  - git_branch_create_existing

  - git_branch_existing


## Task 7: Create Git Branch

- **Name**: Create git branch {{ git_branch_name }}

- **Description**: Creates a new branch in the Git repository.

- **Module**: `ansible.builtin.command`

- **Arguments**:

  - `cmd`: The Git command to create a new branch from the default branch.

- **Registers**: `git_branch_create`

- **Conditional**: The task is only executed when `git_branch_name` is not empty, `default_branch` is defined, and the `git_branch_existing` task did not change.

- **Tags**:

  - git

  - git_branch

  - git_branch_create


## Task 8: Show Current Branch

- **Name**: Show current branch, expecting {{ git_branch_name }}

- **Description**: Retrieves the current branch in the Git repository.

- **Module**: `ansible.builtin.command`

- **Arguments**:

  - `cmd`: The Git command to show the current branch.

- **Registers**: `git_branch_current`

- **Conditional**: The task is only executed when `git_branch_name` is not empty.

- **Tags**:

  - git

  - git_branch

  - git_branch_push

  - git_branch_current


## Task 9: Push Git Branch

- **Name**: Push git branch {{ git_branch_name }}

- **Description**: Pushes the local branch to the remote repository.

- **Module**: `ansible.builtin.command`

- **Arguments**:

  - `cmd`: The Git command to push the branch to the origin.

- **Registers**: `git_branch_push`

- **Conditional**: The task is only executed when `git_branch_name` is not empty and the current branch matches the expected branch name.

- **Tags**:

  - git

  - git_branch

  - git_branch_push


## Task 10: Clear Task Variables

- **Name**: Clear task variables

- **Description**: Resets the task-specific variables to their default values.

- **Module**: `ansible.builtin.set_fact`

- **Arguments**:

  - `task_git_clone_branch_default`: Sets the `task_git_clone_branch_default` variable to `false`.

  - `task_git_user_set`: Sets the `task_git_user_set` variable to `false`.

  - `task_git_branch_create`: Sets the `task_git_branch_create` variable to `false`.

  - `git_branch_name`: Resets the `git_branch_name` variable.

- **Tags**: None


## Variables

The following variables can be customized in this task file:

```yaml
gitlab_api_token: "GITLAB_API_TOKEN"
project_path: "GITLAB_PROJECT_PATH"
default_branch: "DEFAULT_BRANCH_NAME"
git_user_email: "GIT_USER_EMAIL"
git_user_name: "GIT_USER_NAME"
git_branch_name: "BRANCH_NAME"
```

- `gitlab_api_token`: The GitLab API token for authentication.

- `project_path`: The GitLab project path (e.g., `group/repository`).

- `default_branch`: The name of the default branch.

- `git_user_email`: The email address of the Git user.

- `git_user_name`: The name of the Git user.

- `git_branch_name`: The name of the Git branch.

## Tags

The tasks in this task file are tagged with the following tags:

- git

- git_clone

- git_clone_branch_default

- git_clone_branch_default_submodule_init

- git_user

- git_user_set

- git_user_set_email

- git_user_set_name

- git_branch

- git_branch_create

- git_branch_create_existing

- git_branch_existing

- git_branch_current

- git_branch_push


## Usage

To use this Ansible task file, you can include it in your playbook or role and provide values for the required variables. Here's an example of how you can use this task file:

1. Create a playbook (e.g., `git_operations.yaml`) and define the necessary variables:

```yaml
---

- hosts: your_hosts
  vars:
    gitlab_api_token: "YOUR_GITLAB_API_TOKEN"
    project_path: "YOUR_PROJECT_PATH"
    default_branch: "master"
    git_user_email: "your_email@example.com"
    git_user_name: "Your Name"
    git_branch_name: "your_branch"
  
  tasks:
    - include_tasks: git/repository.yaml
```

2. Create a separate file for the task file (e.g., `git_operations_tasks.yaml`) and copy the content of the task file into it.

3. Run the playbook:

```shell
ansible-playbook git_operations.yaml
```

Make sure to replace the placeholder values (`YOUR_GITLAB_API_TOKEN`, `YOUR_PROJECT_PATH`, `your_email@example.com`, `Your Name`, `your_branch`) with the appropriate values for your GitLab setup.

Note: You may need to adjust the playbook structure and additional tasks based on your specific requirements and the tasks you want to execute.