---
title: Gitlab repository management from code
description: How to use No Fuss Computings Ansible role git configuration; to setup your gitlab repository from config as code.
date: 2023-05-26
template: project.html
about: https://gitlab.com/nofusscomputing/projects/ansible/git_configuration
---

!!! Note
    This documentation is still a work in progress


Like the [Github Repository](github.md) featureof this ansible role, you can manage the full lifecycle of your Gitlab repository. Running this role from the CLI includes the gitlab management, however if you wish to manage your Gitlab repositories only, use the `--tags` arg with a value of `gitlab`


## Docs ToDo

- notate name is for the human readable name for the repo
- notate path is for the url name of the repository, if not specified will use `name` adjusting it to lower case and the spaces replaced with an underscore `_`.


## Ansible Task: Update GitLab Group Labels

This task updates GitLab group labels by including a separate task file called [`gitlab/labels.yaml`](gitlab_labels.md). The task loops through a list of groups and their associated labels, provided by the variable `role_git_conf.gitlab.groups`. For each group, it passes the necessary variables to the included task file.


### Configuration

To use this task, make sure you have the following configurations set in your playbook:

- `role_git_conf.gitlab.groups`: A list of groups and their associated labels. Each group should have the following properties:

  - `path`: The path of the group.

  - `labels`: A list of labels to be created or updated within the group. Each label should have a name, color, and description.


### Task Variables

The task uses the following variables:

- `group_labels` (required): The labels to be created or updated within the group.

- `group_path` (required): The path of the GitLab group.

- `gitlab_api_token` (required): Your personal access token for authenticating with the GitLab API.


### Tags

This task does not have any specific tags assigned to it.

### Limitations

- Proper authentication and security measures should be in place, such as protecting sensitive information like access tokens and securing communication with the GitLab server.


## Ansible Task: Update GitLab Project Labels

This task updates GitLab project labels by including a separate task file called [`gitlab/labels.yaml`](gitlab_labels.md). The task loops through a list of projects and their associated labels, provided by the variable `role_git_conf.gitlab.projects`. For each project, it passes the necessary variables to the included task file.


### Configuration

To use this task, make sure you have the following configurations set in your playbook:

- `role_git_conf.gitlab.projects`: A list of projects and their associated labels. Each project should have the following properties:

    - `group`: The path of the group that contains the project.

    - `name`: The name of the project.

    - `labels`: A list of labels to be created or updated within the project. Each label should have a name, color, and description.


### Task Variables

The task uses the following variables:

- `project_labels` (required): The labels to be created or updated within the project.

- `project_path` (required): The path of the GitLab project in the format `group/name`.

- `gitlab_api_token` (required): Your personal access token for authenticating with the GitLab API.


### Tags

This task does not have any specific tags assigned to it.

### Limitations

- Proper authentication and security measures should be in place, such as protecting sensitive information like access tokens and securing communication with the GitLab server.

Please review and update the configurations according to your specific environment and requirements.