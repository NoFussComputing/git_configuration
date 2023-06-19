---
title: Manage GitLab Group and Project Labels
description: How to use No Fuss Computings Ansible role git configuration; to manage project or group labels.
date: 2023-06-16
template: project.html
about: https://gitlab.com/nofusscomputing/projects/ansible/git_configuration
---

This Ansible task file is used for managing GitLab group and project labels. It includes tasks for creating, fetching, and deleting labels within a GitLab group and project. The tasks interact with the GitLab API using the `ansible.builtin.uri` module.


## Prerequisites

Before using this task file, make sure you have the following:

- Ansible installed on the machine where you plan to execute this task file.

- Access to a GitLab server and a personal access token with appropriate permissions to manage group and project labels.

- The GitLab group and project paths where you want to manage the labels.


## Configuration

To use this task file, you need to set the following variables in a separate YAML file (e.g., `labels_config.yaml`):

```yaml
gitlab_server_url: https://your-gitlab-server.com
gitlab_api_token: your-personal-access-token
group_path: your-group-path
group_labels:
  - name: label1
    color: #FF0000
    description: First label
  - name: label2
    color: #00FF00
    description: Second label
project_path: your-project-path
project_labels:
  - name: label3
    color: #0000FF
    description: Third label
fetch: true
```

Make sure to replace the values with your actual GitLab server URL, personal access token, group and project paths, and label configurations. The `group_labels` variable is a list of labels to be created or deleted within the group, and the `project_labels` variable is a list of labels to be created or deleted within the project. Each label should have a name, color, and description.


## Usage

To execute the task file, run the following command:

```bash
ansible-playbook -i localhost gitlab_labels.yaml
```


## Task File Description

The task file consists of the following tasks:

1. **Create Gitlab Group Labels**: This task creates GitLab group labels based on the provided configurations.

2. **Fetch Gitlab Group Labels**: This task fetches the existing GitLab group labels.

3. **Delete Gitlab Group Labels**: This task deletes GitLab group labels based on the provided configurations.

4. **Create Gitlab Project Labels**: This task creates GitLab project labels based on the provided configurations.

5. **Fetch Gitlab Project Labels**: This task fetches the existing GitLab project labels.

6. **Delete Gitlab Project Labels**: This task deletes GitLab project labels based on the provided configurations.


## Task Variables

The task file uses the following variables:

- `gitlab_server_url` (required): The URL of your GitLab server.

- `gitlab_api_token` (required): Your personal access token for authenticating with the GitLab API.

- `group_path` (required): The path of the GitLab group where the group labels will be managed.

- `group_labels` (required): A list of labels to be created or deleted within the group. Each label should have a name, color, and description.

- `project_path` (required): The path of the GitLab project where the project labels will be managed.

- `project_labels` (required): A list of labels to be created or deleted within the project. Each label should have a name, color, and description.

- `fetch` (optional): A flag indicating whether to fetch the existing group and project labels. Set it to `true` to enable fetching.


## Tags

The tasks within the task file are tagged for better control during execution:

- `gitlab`:

    The main tag for all tasks related to GitLab.

- `gitlab_labels`: The tag for tasks related to managing GitLab labels.

- `gitlab_labels_create`: The tag for tasks related to creating GitLab labels.

- `gitlab_labels_delete`: The tag for tasks related to deleting GitLab labels.

- `gitlab_labels_group`: The tag for tasks related to managing GitLab group labels.

- `gitlab_labels_group_create`: The tag specifically for the task that creates GitLab group labels.

- `gitlab_labels_group_delete`: The tag specifically for the task that deletes GitLab group labels.

- `gitlab_labels_project`: The tag for tasks related to managing GitLab project labels.

- `gitlab_labels_project_create`: The tag specifically for the task that creates GitLab project labels.

- `gitlab_labels_project_delete`: The tag specifically for the task that deletes GitLab project labels.


## Limitations

- This task file uses the `ansible.builtin.uri` module to interact with the GitLab API since there is no built-in GitLab module available. Ensure that the `ansible.builtin.uri` module is installed on your Ansible environment.

- Proper authentication and security measures should be in place, such as protecting sensitive information like access tokens and securing communication with the GitLab server.

Please review and update the configuration variables according to your specific environment and requirements.