---
title: Issues Task file
description: How to use No Fuss Computings Ansible role git configuration; to search for gitlab issues.
date: 2023-06-17
template: project.html
about: https://gitlab.com/nofusscomputing/projects/ansible/git_configuration
---

This Ansible task file is used to manage GitLab issues. It provides tasks for building the GitLab issue URL, finding existing issues, and retrieving information about them using the GitLab API.


## Task 1: Build GitLab Issue URL

- **Name**: build URL

- **Description**: Builds the GitLab issue URL based on the provided project path and issue ID. If the issue ID is not defined, it retrieves all opened issues for the project.

- **Variables**:

  - `gitlab_server_url`: The URL of the GitLab server.

  - `project_path`: The path to the GitLab project.

  - `issue_iid` (optional): The ID of the specific issue.

- **Tags**: gitlab, gitlab_issues


## Task 2: Find Existing Issues

- **Name**: Find Existing Issue

- **Description**: Sends a GET request to the GitLab issue URL to retrieve information about existing issues.

- **Variables**:

  - `gitlab_issue_url`: The URL of the GitLab issue API.

  - `gitlab_api_token`: The private token for authenticating the API request.

- **Tags**: gitlab, gitlab_issues, gitlab_issues_fetch

## Task 3: Set Existing Issues as Facts

- **Name**: Fact gitlab_issues_fetch clean

- **Description**: Sets the `gitlab_issues_existing` fact with the fetched GitLab issues, if any.

- **Variables**:

  - `gitlab_issues_fetch.json`: The JSON response received from the GitLab API.

- **Tags**: None


## Variables

The following variables can be customized to suit your GitLab environment:

- `gitlab_server_url`: The URL of the GitLab server.

- `project_path` (optional): The path to the GitLab project.

- `issue_iid` (optional): The ID of a specific issue.

- `gitlab_api_token`: The private token for authenticating the API requests.


## Tags

This task file uses the following tags for organizing tasks:

- `gitlab`: Tasks related to GitLab integration.

- `gitlab_issues`: Tasks related to managing GitLab issues.

- `gitlab_issues_fetch`: Task for fetching GitLab issues.


## Usage

1. Set the appropriate values for the variables mentioned above.

2. Include this task file in your Ansible playbook or task list.

3. Run the Ansible playbook or task.


## Example Playbook

Here's an example playbook that includes the "issues.yaml" task file:

```yaml
- name: Manage GitLab Issues
  hosts: localhost
  gather_facts: false
  tasks:
    - name: Include GitLab Issues Tasks
      include_tasks: issues.yaml
      vars:
        gitlab_server_url: "https://gitlab.example.com"
        project_path: "group/project"
        gitlab_api_token: "your_gitlab_api_token"
```

Make sure to replace the values of the variables with your actual GitLab server URL, project path, and API token.

!!! Note
    Ensure that you have Ansible installed and the required modules available for execution.
