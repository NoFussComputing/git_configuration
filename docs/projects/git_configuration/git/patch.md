---
title: Patch Task file
description: How to use No Fuss Computings Ansible role git configuration; task file patch for gitlab projects.
date: 2023-06-18
template: project.html
about: https://gitlab.com/nofusscomputing/projects/ansible/git_configuration
---

This Ansible task file is responsible for removing any existing patch file, downloading a patch file, switching to a specified branch, checking if the patch is required, and applying the patch.


## Task 1: Remove Existing Patch File

- **Name**: Remove any existing patch file

- **Description**: Removes any existing patch file from the `/tmp` directory.

- **Module**: `ansible.builtin.file`

- **Arguments**:

  - `path`: The path of the patch file to remove.

  - `state`: Specifies the desired state of the patch file, which is "absent" to remove it.

- **Conditional**: The task is only executed when the `patch_url_download` variable is defined and `git_patch_filename` is not empty.

- **Tags**:

  - git

  - git_patch

  - git_patch_download


## Task 2: Download Patch

- **Name**: Download Patch

- **Description**: Downloads the patch file from the specified URL.

- **Module**: `ansible.builtin.uri`

- **Arguments**:

  - `url`: The URL of the patch file to download.

  - `method`: The HTTP method for the download request (GET).

  - `status_code`: The expected status code indicating a successful download (200).

  - `headers`: The headers to include in the request, including the `PRIVATE-TOKEN` for GitLab authentication.

  - `dest`: The destination path where the patch file will be saved.

- **Registers**: `git_patch_download`

- **Conditional**: The task is only executed when the `patch_url_download` variable is defined and `git_patch_filename` is not empty.

- **Tags**:

  - git

  - git_patch

  - git_patch_download


## Task 3: Switch to Branch

- **Name**: Switch to branch {{ git_branch_name }}

- **Description**: Switches to the specified branch in the Git repository.

- **Module**: `ansible.builtin.command`

- **Arguments**:

  - `cmd`: The Git command to execute for switching branches.

  - `chdir`: The directory where the Git repository is located.

- **Registers**: `git_patch_apply_branch_switch`

- **Conditional**: The task is only executed when `git_patch_filename` and `git_branch_name` are not empty.

- **Tags**:

  - git

  - git_patch

  - git_patch_apply


## Task 4: Check if Patch is Required

- **Name**: Check if Patch {{ git_patch_filename }} required

- **Description**: Checks if the patch is required by applying a dry run and checking the return code.

- **Module**: `ansible.builtin.command`

- **Arguments**:

  - `cmd`: The Git command to check if the patch is required.

  - `chdir`: The directory where the Git repository is located.

- **Registers**: `git_patch_apply_applicable`

- **Conditional**: The task is only executed when `git_patch_filename` and `git_branch_name` are not empty.

- **Tags**:

  - git

  - git_patch

  - git_patch_apply


## Task 5: Apply Patch

- **Name**: Apply Patch {{ git_patch_filename }}

- **Description**: Applies the patch to the Git repository.

- **Module**: `ansible.builtin.command`

- **Arguments**:

  - `cmd`: The Git command to apply the patch.

  - `chdir`: The directory where the Git repository is located.

- **Registers**: `git_patch_apply`

- **Conditional**: The task is only executed when the patch is applicable (`git_patch_apply_applicable.rc` is 0), `git_patch_filename` and `git_branch_name` are not empty.

- **Tags**:

  - git

  - git_patch

  - git_patch_apply


## Task 6: Clear Task Variables

- **Name**: Clear task variables

- **Description**: Resets the task-specific variables to their default values.

- **Module**: `ansible.builtin.set_fact`

- **Arguments**:

  - `task_git_patch_download`: Sets the `task_git_patch_download` variable to `false`.

  - `task_git_patch_apply`: Sets the `task_git_patch_apply` variable to `false`.

  - `git_patch_filename`: Resets the `git_patch_filename` variable.

  - `git_branch_name`: Resets the `git_branch_name` variable.

- **Tags**: None


## Variables

The following variables can be customized in this task file:

```yaml
patch_url_download: "URL_OF_PATCH_FILE"
gitlab_api_token: "GITLAB_API_TOKEN"
git_patch_filename: "PATCH_FILENAME"
git_branch_name: "BRANCH_NAME"
```

- `patch_url_download`: The URL of the patch file to download.
- `gitlab_api_token`: The API token for GitLab authentication.
- `git_patch_filename`: The filename of the patch file.
- `git_branch_name`: The name of the Git branch.


## Tags

The tasks in this task file are tagged with the following tags:

- git

- git_patch

- git_patch_download

- git_patch_apply

## Usage

To use this task file, include it in your Ansible playbook or task list. Customize the variables and modify the placeholder tasks as needed.

```yaml
- name: Apply Git Patch
  hosts: your_hosts
  tasks:
    - name: Include Git Patch Tasks
      ansible.builtin.include_tasks:
        file: git/patch.yaml
```

Make sure to set the necessary variables (`patch_url_download`, `gitlab_api_token`, `git_patch_filename`, `git_branch_name`) according to your environment before running the playbook.
