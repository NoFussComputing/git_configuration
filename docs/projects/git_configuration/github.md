---
title: Github repository management from code
description: How to use No Fuss Computings Ansible role git configuration; to setup your github repository from config as code.
date: 2023-06-05
template: project.html
about: https://gitlab.com/nofusscomputing/projects/ansible/git_configuration
---

!!! Note
    This documentation is still a work in progress


Like the [Gitlab Repository](gitlab.md) feature of this ansible role, you can manage the full lifecycle of your Github repository. Running this role from the CLI includes the github management, however if you wish to manage your Github repositories only, use the `--tags` arg with a value of `github`


## Docs ToDo

- expand


## Configuration

``` yaml title="vars.yaml" linenums="yes"

role_git_conf:

  github: # Mandatory if you wish to manage Github Configuration

    - api_url: "https://github.com"
      api_token:                              # Mandatory, Github API Key with organisation/group access as the owner
      projects:                               # Mandatory, list of repositories to manage
        - name: ansible_playbooks             # Mandatory, name of repository
            organization: NoFussComputing     # Mandatory, where the project will be created/located
            description: ""                   # Optional, default=none
            private: true                     # Optional, default=true
            users:                            # Optional, list of users to give access
              - name: nfc-robot               # Mandatory, Github username for use
                permission: maintain          # Mandatory, permission level to grant user

```
