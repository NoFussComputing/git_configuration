---
title: Notes Task file
description: How to use No Fuss Computings Ansible role git configuration; task file to fetch gitlab issue notes.
date: 2023-06-17
template: project.html
about: https://gitlab.com/nofusscomputing/projects/ansible/git_configuration
---

This Ansible task file is used to manage GitLab issue notes. It provides tasks for finding existing issue notes and retrieving information about them using the GitLab API.


## Task 1: Find Existing Issue Notes

- **Name**: Find Existing Issue Notes

- **Description**: Sends a GET request to the GitLab API to retrieve existing notes for a specific issue.

- **Variables**:

  - `gitlab_server_url`: The URL of the GitLab server.

  - `project_path`: The path to the GitLab project.

  - `issue_iid`: The ID of the issue.

  - `gitlab_api_token`: The private token for authenticating the API request.

- **Tags**: gitlab, gitlab_issues, gitlab_issues_notes, gitlab_issues_notes_fetch


## Task 2: Set Existing Issue Notes as Facts

- **Name**: Fact gitlab_issues_notes_fetch clean

- **Description**: Appends the fetched GitLab issue notes to the `gitlab_issue_notes_existing` fact, if any.

- **Variables**:

  - `gitlab_issue_notes_existing`: A list that holds the existing GitLab issue notes.

  - `gitlab_issues_notes_fetch.json`: The JSON response received from the GitLab API.

- **Tags**: None


## Variables

The following variables can be customized to suit your GitLab environment:

- `gitlab_server_url`: The URL of the GitLab server.

- `project_path`: The path to the GitLab project.

- `issue_iid`: The ID of the specific issue.

- `gitlab_api_token`: The private token for authenticating the API requests.


## Tags

This task file uses the following tags for organizing tasks:

- `gitlab`: Tasks related to GitLab integration.

- `gitlab_issues`: Tasks related to managing GitLab issues.

- `gitlab_issues_notes`: Tasks related to managing GitLab issue notes.

- `gitlab_issues_notes_fetch`: Task for fetching GitLab issue notes.


## Usage

1. Set the appropriate values for the variables mentioned above.

2. Include this task file in your Ansible playbook or task list.

3. Run the Ansible playbook or task.


## Example Playbook

Here's an example playbook that includes the "notes.yaml" task file:

```yaml
- name: Manage GitLab Issue Notes
  hosts: localhost
  gather_facts: false
  tasks:
    - name: Include GitLab Issue Notes Tasks
      include_tasks: notes.yaml
      vars:
        gitlab_server_url: "https://gitlab.example.com"
        project_path: "group/project"
        issue_iid: 123
        gitlab_api_token: "your_gitlab_api_token"
```

Make sure to replace the values of the variables with your actual GitLab server URL, project path, issue ID, and API token.

!!! Note
    Ensure that you have Ansible installed and the required modules available for execution.
