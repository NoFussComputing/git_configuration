---
title: Create and Configure a Gitlab repository from code
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
