---
title: Git repository management from code
description: How to use No Fuss Computings Ansible role git configuration; to setup your git repositories in Gitlab and Github from config as code.
date: 2023-05-26
template: project.html
about: https://gitlab.com/nofusscomputing/projects/ansible/git_configuration
---

This Ansible role has been designed to enable you to place git related settings as infrastructure as code. Usage is designed to establish and maintain Gitlab and Github repositories for their lifecycle. Running this role with the required variables, will conduct every task within the role. to filter to either Gitlab or Github, use ansible with `--tags` `gitlab` or `github` respectively. this role, even with the use of tags is designed to run again and again, as if there are no changes, nothing will be changed.

!!! Tip
    When using our [Ansible Execution Environment Docker Container](../../execution_environment/index.md) `nofusscomputing/ansible-ee` this role is included as part of that containers build. This role is also included in our [Ansible Roles](../index.md) git repository.


## Features

Regardless of the repository type Gitlab/Github, the features are intended to use a common configuration layout with the role designed to interperate this to each different system.


### Common to both Gitlab/Github




- **Automations:**

    - Repository Management

        *Create a repository and Adjust its settings*


### Gitlab features

- **Automations:**

    - [Git submodule update](submodule.md) - Update a repositories `git submodule` *(Github planned)*

    - [Merge Request from git patches found within an issue comment(s)](patches_from_gitlab_issues.md)

        *Searches issues within the specified project for any patch files and creates a Merge Request if the patch poster has developer or higher access to the project*

    - Pipeline Cleanup *(under development)*

        *Remove pipelines if they are not part of eith the master or development branch*

- [Label management at project and group level](gitlab/labels.md)


- Topics management - *Currently only for Gitlab, Github planned*

- AWX Webhook Artifacts

    > By using tag `gitlab_webhook` from an AWX / Ansible Automation Platform template and setting up the incoming webhook, this will receive the data from the webhook and save it as an artifact for further automations.


## Roadmap

Items within this list are here as a possible, actual, under deveopment or planned features:

- Avatar management for repository - *(currently only supporting adding on repository creation)*

- Cross-platform Development from Github to Gitlab

    *Automation that from a PR created on Github, creates a Gitlab MR from the PR patch, and if the pipeline suceeds merge it*

- Gitlab runner management - Planned feature *[GL-#3](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/issues/3)*

- Protected tags management- Planned feature *[GL-#2](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/issues/2)*

- *Scheduled pipeline management - Planned feature [GL-#9](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/issues/9)*


## Automation File

Some of the tasks within this role can be run from within the Gitlab CD/CI environment. For the configuration of such tasks, an automation file `.nfc_automation.yaml` is required in the root directory of the repository. The layout of this file is the same as an ansible vars file, however under a single key and formatted as a yaml of dictionaries/lists. Throughout the documentation you will find the required structure of this yaml, specifically if the automation/task can be run from Gitlab. see [Gitlab config documentation](gitlab.md#Configuration).



## Role Default Variables

This file is the default variables for any that can be used for a task.

``` yaml title="defaults/main.yaml" linenums="1"

--8<-- "defaults/main.yaml"

```