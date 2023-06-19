---
title: Projects Task file
description: How to use No Fuss Computings Ansible role git configuration; task file to fetch gitlab project.
date: 2023-06-17
template: project.html
about: https://gitlab.com/nofusscomputing/projects/ansible/git_configuration
---

This Ansible task file is used to fetch information about a single project from GitLab. It includes tasks for sending a GET request to the GitLab API and retrieving project details.


## Task 1: Fetch a Single Project

- **Name**: Fetch a single project

- **Description**: Sends a GET request to the GitLab API to retrieve information about a specific project.

- **Variables**:

  - `gitlab_server_url`: The URL of the GitLab server.

  - `project_path`: The path to the GitLab project.

  - `gitlab_api_token`: The private token for authenticating the API request.

- **Tags**: gitlab, gitlab_project, gitlab_project_fetch


## Task 2: Set Fetched Project Information as Facts

- **Name**: Fact gitlab_project_fetch clean

- **Description**: Stores the fetched GitLab project information in the `gitlab_existing_project` and `gitlab_project_url` facts, if any.

- **Variables**:

  - `gitlab_existing_project`: The existing GitLab project details.

  - `gitlab_project_fetch.json`: The JSON response received from the GitLab API.

  - `gitlab_project_url`: The web URL of the GitLab project.

- **Tags**: None


## Variables

Customize the following variables according to your GitLab environment:

- `gitlab_server_url`: The URL of the GitLab server.

- `project_path`: The path to the GitLab project.

- `gitlab_api_token`: The private token for authenticating the API requests.


## Tags

This task file uses the following tags for organizing tasks:

- `gitlab`: Tasks related to GitLab integration.

- `gitlab_project`: Tasks related to managing GitLab projects.

- `gitlab_project_fetch`: Task for fetching GitLab project details.


## Usage

1. Set the appropriate values for the variables mentioned above.

2. Include this task file in your Ansible playbook or task list.

3. Run the Ansible playbook or task.


## Example Playbook

Here's an example playbook that includes the "projects.yaml" task file:

```yaml
- name: Manage GitLab Projects
  hosts: localhost
  gather_facts: false
  tasks:
    - name: Include GitLab Project Tasks
      include_tasks: projects.yaml
      vars:
        gitlab_server_url: "https://gitlab.example.com"
        project_path: "group/project"
        gitlab_api_token: "your_gitlab_api_token"
```

Replace the values of the variables with your actual GitLab server URL, project path, and API token.

!!! Note
    Ensure that you have Ansible installed and the required modules available for execution.
