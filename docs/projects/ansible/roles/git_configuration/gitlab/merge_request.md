---
title: Merge Request Task file
description: How to use No Fuss Computings Ansible role git configuration; task file merge request for gitlab projects.
date: 2023-06-18
template: project.html
about: https://gitlab.com/nofusscomputing/projects/ansible/git_configuration
---

This Ansible task file performs actions related to checking and creating merge requests on GitLab. It checks for an existing merge request, creates a new merge request if the conditions are met, and displays the merge requests. Finally, it clears the task-related variables.


## Task: Check for existing Merge Request

- **Name**: Check for existing Merge Request

- **Description**: Checks if there is an existing merge request for the specified source and target branches.

- **Module**: `ansible.builtin.uri`

- **Arguments**:

  - `url`: The URL to fetch merge requests from the GitLab API.

  - `method`: GET

  - `body_format`: json

  - `return_content`: true

  - `headers`: Includes the `PRIVATE-TOKEN` header with the GitLab API token.

- **Registers**: `gitlab_merge_request_existing`

- **Failed When**: The condition `'never' == 'fail'` is evaluated.

- **Changed When**: The length of `gitlab_merge_request_existing.json` is greater than 0.

- **Conditional**: The task is executed when the `source_branch` variable is defined.

- **Tags**:

  - `gitlab`

  - `gitlab_merge_request`

  - `gitlab_merge_request_create`

  - `gitlab_merge_request_existing`


## Task: Set fact for existing Merge Request

- **Name**: Set fact for existing Merge Request

- **Description**: Adds the existing merge request data to the `merge_requests` variable.

- **Module**: `ansible.builtin.set_fact`

- **Arguments**:

  - `merge_requests`: Appends `gitlab_merge_request_existing.json` parsed as YAML to the existing `merge_requests` list.

- **Conditional**: The `gitlab_merge_request_existing.json` variable is not empty.

- **Tags**: None


## Task: Create Merge Request

- **Name**: Create Merge Request for {source_branch}

- **Description**: Creates a new merge request for the specified source and target branches.

- **Module**: `ansible.builtin.uri`

- **Arguments**:

  - `url`: The URL to create a merge request in the GitLab API.

  - `method`: POST

  - `body_format`: json

  - `status_code`: [200, 201]

  - `return_content`: true

  - `headers`: Includes the `PRIVATE-TOKEN` header with the GitLab API token.

- **Registers**: `gitlab_merge_request_create`

- **Conditional**: The task is executed when the following conditions are met:

  - `gitlab_merge_request_existing.changed` is false

  - `gitlab_merge_request_description` is not empty

  - `gitlab_merge_request_title` is not empty

- **Changed When**: The length of `gitlab_merge_request_create.json` is greater than 0.

- **Tags**:

  - `gitlab`

  - `gitlab_merge_request`

  - `gitlab_merge_request_create`


## Task: Set fact for created Merge Request

- **Name**: Set fact for created Merge Request

- **Description**: Adds the created merge request data to the `merge_requests` variable.

- **Module**: `ansible.builtin.set_fact`

- **Arguments**:

  - `merge_requests`: Appends `gitlab_merge_request_create.json` parsed as YAML to the existing `merge_requests` list.

- **Conditional**: The `gitlab_merge_request_create.json` variable is not empty.

- **Tags**: None


## Task: Display Merge Request

- **Name**: Display Merge Request

- **Description**: Displays the contents of the `merge_requests` variable.

- **Module**: `ansible.builtin.debug`

- **Arguments**:

  - `msg`: The value of the `merge_requests` variable.

- **Tags**: None


## Task: Clear task variables

- **Name**: Clear task variables

- **Description**: Clears the task-related variables.

- **Module**: `ansible.builtin.set_fact`

- **Arguments**:

  - `gitlab_merge_request_create`: false

  - `gitlab_merge_request_title`: ''

  - `gitlab_merge_request_description`: ''

- **Tags**: None


## Variables

The following variables can be customized in this task file:

```yaml
project_path: ""
source_branch: ""
default_branch: ""
gitlab_api_token: ""
gitlab_merge_request_title: ""
gitlab_merge_request_description: ""
merge_request_remove_remove_source_branch: true
```

- `project_path`: The path of the project in the GitLab repository.

- `source_branch`: The name of the source branch for the merge request.

- `default_branch`: The name of the target branch for the merge request.

- `gitlab_api_token`: The API token used for authentication with the GitLab API.

- `gitlab_merge_request_title`: The title of the merge request to create.

- `gitlab_merge_request_description`: The description of the merge request to create.

- `merge_request_remove_remove_source_branch`: Specifies whether to remove the source branch after merging (default: true).


## Tags

The tasks in this task file are tagged with the following tags:

- `gitlab`

- `gitlab_merge_request`

- `gitlab_merge_request_create`

- `gitlab_merge_request_existing`


## Usage

To use this Ansible task file, you can include it in your playbook or role and provide values for the required variables. Here's an example of how you can use this task file:

1. Create a playbook (e.g., `your_playbook.yaml`) and define the necessary variables:

```yaml
---

- hosts: your_hosts
  vars:
    project_path: "your_project"
    source_branch: "your_source_branch"
    default_branch: "your_target_branch"
    gitlab_api_token: "your_token"
    gitlab_merge_request_title: "your_merge_request_title"
    gitlab_merge_request_description: "your_merge_request_description"
  
  tasks:
    - include_tasks: path/to/task_file.yaml
```

2. Create a separate file for the task file (e.g., `task_file.yaml`) and copy the content of the task file into it.

3. Run the playbook:

```shell
ansible-playbook your_playbook.yaml
```

Make sure to replace the placeholder values (`project_path`, `source_branch`, `default_branch`, `gitlab_api_token`, `gitlab_merge_request_title`, `gitlab_merge_request_description`) with the appropriate values for your setup.

Note: You may need to adjust the playbook structure and additional tasks based on your specific requirements and the tasks you want to execute.
