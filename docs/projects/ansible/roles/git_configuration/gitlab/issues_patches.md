---
title: Issue Patches Task file
description: How to use No Fuss Computings Ansible role git configuration; to search for gitlab issues that have patch files attached and return the details for them.
date: 2023-06-17
template: project.html
about: https://gitlab.com/nofusscomputing/projects/ansible/git_configuration
---

This Ansible task file is used to fetch GitLab issues with patches, retrieve project details, fetch GitLab notes, filter and store notes with patch files, and set up facts related to patch files. It includes multiple tasks and includes other task files for specific operations.


## Task 1: Fetch GitLab Issues with Patch

- **Name**: Fetch GitLab issues with patch

- **Description**: Includes the `gitlab/issues.yaml` task file to fetch GitLab issues.

- **Tags**: `gitlab_issues_fetch`


## Task 2: Fetch Project Details

- **Name**: Fetch Project details

- **Description**: Includes the `gitlab/projects.yaml` task file to fetch project details from GitLab.

- **Tags**: `gitlab_project_fetch`


## Task 3: Fetch GitLab Notes

- **Name**: Fetch GitLab notes

- **Description**: Includes the `gitlab/notes.yaml` task file to fetch notes from GitLab issues.

- **Variables**:

  - `project_path`: The path of the project in GitLab.

- **Loop**: Loops over the `gitlab_issues_existing` list.

- **Loop Control**:

  - `loop_var`: task_item

- **Tags**: `gitlab_issues_notes_fetch`


## Task 4: Only Keep Notes with Patch Files

- **Name**: Only Keep Notes with patch files

- **Description**: Filters and stores notes that contain patch files in the `gitlab_issues_notes_patches` list.

- **Loop**: Loops over the `gitlab_issue_notes_existing` list.

- **Loop Control**:

  - `loop_var`: item

- **When**:

  - Ensures the note is not a system note.

  - Checks if the note body contains a patch file using a regular expression.

- **Tags**: None


## Task 5: Setup Fact for Patch Files

- **Name**: Setup fact for patch files

- **Description**: Sets up the `gitlab_issue_patch_files` fact with information about patch files extracted from notes.

- **Loop**: Loops over the `gitlab_issues_notes_patches` list.

- **Loop Control**:

  - `loop_var`: item

- **No Log**: Disables logging for data manipulation.

- **Tags**: None


## Task 6: Clean Facts No Longer Required

- **Name**: Clean facts no longer required

- **Description**: Clears the facts that are no longer required for subsequent tasks.

- **Variables**:

  - `gitlab_issues_existing`: An empty list to clear the existing GitLab issues.

  - `gitlab_issue_notes_existing`: An empty list to clear the existing GitLab issue notes.

  - `gitlab_issues_notes_patches`: An empty list to clear the GitLab notes with patch files.

- **No Log**: Disables logging for data manipulation.

- **Tags**: None


## Variables

Customize the following variables according to your GitLab environment:

```yaml
gitlab_api_token: "YOUR_GITLAB_API_TOKEN"
project_path: "YOUR_PROJECT_PATH"
```


## Tags

This task file uses the following tags for organizing tasks:

- `gitlab`: Tasks related to GitLab integration.

- `gitlab_issues_fetch`: Task for fetching GitLab issues.

- `gitlab_project_fetch`: Task for fetching GitLab project details.

- `gitlab_issues_notes_fetch`: Task for fetching GitLab notes.


## Usage

1. Set the appropriate values for the variables mentioned above (`gitlab_api_token` and `project_path`).

2. Include this task file in your Ansible playbook or task list.

3. Run the Ansible playbook or task.

!!! Note
    Ensure that you have Ansible installed and the required modules available for execution.
