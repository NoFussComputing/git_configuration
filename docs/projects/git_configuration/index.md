---
title: Configure Git from code
description: How to use No Fuss Computings Ansible role git configuration; to setup your git repositories in Gitlab and Github from config as code.
date: 2023-05-26
template: project.html
about: https://gitlab.com/nofusscomputing/projects/ansible/git_configuration
---

!!! Note
    This documentation is still a work in progress

!!! Tip
    When using our [Ansible Execution Environment Docker Container](../execution_environment/index.md) `nofusscomputing/ansible-ee` this role is included as part of that containers build.

!!! Tip
    This role is also included in our [Ansible Roles](../ansible-roles/index.md) git repository.


This Ansible role has been designed to enable you to place git related settings as infrastructure as code. Usage is designed to establish and maintain Gitlab and Github repositories for their lifecycle. Running this role with the required variables, will conduct every task within the role. to filter to either Gitlab or Github, use ansible with `--tags` `gitlab` or `github` respectively. this role, even with the use of tags is designed to run again and again, as if there are no changes, nothing will be changed.


## Features

Regardless of the repository type Gitlab/Github, the features are intended to use a common configuration layout with the role designed to interperate this to each different system.

**Common to both Gitlab/Github**

- Create a repository

- Configure repository settings

- repository Creation

    - Templated `README.md`
    - Templated `LICENSE`

- Topics management - *Currently only for Gitlab, Github planned*

**Gitlab Only**

- Avatar - *(currently only supporting adding on repository creation)*

- [Git submodule update](submodule.md) - Update a repositories `git submodule` *(Github planned)*

- *Gitlab runner management - Planned feature [GL-#3](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/issues/3)*

- *Label management at project and group level - Planned feature*

- Pipeline Cleanup *(under development)*

- *Protected tags management- Planned feature [GL-#2](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/issues/2)*

- *Scheduled pipeline management - Planned feature [GL-#9](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/issues/9)*
