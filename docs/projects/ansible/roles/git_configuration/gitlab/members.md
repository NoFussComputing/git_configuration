---
title: Members Task file
description: How to use No Fuss Computings Ansible role git configuration; task file members for gitlab projects.
date: 2023-06-18
template: project.html
about: https://gitlab.com/nofusscomputing/projects/ansible/git_configuration
---

This Ansible task file performs actions related to fetching and displaying GitLab project members. It includes tasks to set the GitLab members URL, fetch all project members, clean up the fetched data, and display the found project members. Additionally, there is a task to clear task-related variables.


## Task: build URL

- **Name**: build URL

- **Description**: Set the GitLab members URL based on the server URL and project path.

- **Module**: `ansible.builtin.set_fact`

- **Arguments**:

  - `gitlab_members_url`: The URL to fetch project members from the GitLab API.

- **Conditional**: The task is executed when the `project_path` variable is defined.

- **Tags**: None


## Task: Fetch All Project Members

- **Name**: Fetch All Project Members

- **Description**: Fetches all the project members from a GitLab project by making an API request.

- **Module**: `ansible.builtin.uri`

- **Arguments**:

  - `url`: The URL to fetch project members from the GitLab API.

  - `method`: GET

  - `body_format`: json

  - `status_code`: [200, 201]

  - `return_content`: true

  - `headers`: Includes the `PRIVATE-TOKEN` header with the GitLab API token.

- **Registers**: `gitlab_members_fetch_all`

- **Conditional**: The task is executed when the `project_path` variable is defined.

- **Tags**: 

  - `gitlab`

  - `gitlab_members`

  - `gitlab_members_fetch`

  - `gitlab_members_fetch_all`


## Task: Fact gitlab_members_fetch_all clean

- **Name**: Fact gitlab_members_fetch_all clean

- **Description**: Cleans up the `gitlab_members_fetch_all` variable by parsing it as YAML.

- **Module**: `ansible.builtin.set_fact`

- **Arguments**:

  - `gitlab_members_fetch_all`: The `gitlab_members_fetch_all.json` variable parsed as YAML.

- **Conditional**: The task is executed when the length of `gitlab_members_fetch_all.json` is greater than 0.

- **Tags**: None


## Task: Display found Project Members

- **Name**: Display found Project Members

- **Description**: Displays the contents of the `gitlab_members_fetch_all` variable.

- **Module**: `ansible.builtin.debug`

- **Arguments**:

  - `msg`: The value of `gitlab_members_fetch_all`.

- **Conditional**: The task is executed when the `task_gitlab_members_fetch_all` variable is true.

- **Tags**: None


## Task: Clear task variables

- **Name**: Clear task variables

- **Description**: Resets the values of `task_gitlab_members_fetch_all` and `gitlab_members_url` variables.

- **Module**: `ansible.builtin.set_fact`

- **Arguments**:

  - `task_gitlab_members_fetch_all`: false

  - `gitlab_members_url`: ''

- **Tags**: None


## Variables

The following variables can be customized in this task file:

```yaml
gitlab_server_url: "https://gitlab.example.com"
project_path: "your_project"
gitlab_api_token: "your_token"
```

- `gitlab_server_url`: The base URL of your GitLab server.
- `project_path`: The path of the GitLab project.
- `gitlab_api_token`: The API token for authenticating with the GitLab API.


## Tags

The tasks in this task file are tagged with the following tags:

- `gitlab`

- `gitlab_members`

- `gitlab_members_fetch`

- `gitlab_members_fetch_all`


## Usage

To use this Ansible task file, you can include it in your playbook or role and provide values for the required variables. Here's an example of how you can use this task file:

1. Create a playbook (e.g., `your_playbook.yaml`) and define the necessary variables:

```yaml
---

- hosts: your_hosts
  vars:
    gitlab_server_url: "https://gitlab.example.com"
    project_path: "your_project"
    gitlab_api_token: "your_token"
  
  tasks:
    - include_tasks: gitlab/members.yaml
```

2. Create a separate file for the task file (e.g., `task_file.yaml`) and copy the content of the task file into it.

3. Run the playbook:

```shell
ansible-playbook your_playbook.yaml
```

Make sure to replace the placeholder values (`gitlab_server_url`, `project_path`, `gitlab_api_token`) with the appropriate values for your setup.

Note: You may need to adjust the playbook structure and additional tasks based on your specific requirements and the tasks you want to execute.