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


## Configuration

This yaml file contains all of the configuration settings that are used for this role. In short, it's an ansible variable file.

``` yaml title="vars.yaml" linenums="yes"

role_git_conf:
  gitlab:                                                              # Mandatory if you wish to manage Gitlab Configuration
    api_token_owner:                                                   # Mandatory, Gitlab API Key with project/group access as the owner
    api_token:                                                         # Mandatory, Gitlab API key for developer access

    auto_merge: true                                                   # Optional, default=false            # used in .nfc_automation.yaml
    default_branch: development                                        # Optional, default=development      # used in .nfc_automation.yaml
    merge_request:
      patch_labels: '~"code review::not started"'                      # Mandatory for patches automation   # used in .nfc_automation.yaml
    mr_labels: ~"type::automation" ~"impact::0" ~"priority::0"         # Optional, default=none             # used in .nfc_automation.yaml
    submodule_branch: "development"                                    # Optional, default=development      # used in .nfc_automation.yaml

    groups:                                                            # Optional, manage these groups
      - name: No Fuss Computing                                        # Mandatory, human readable name of the group
        path: nofusscomputing                                          # Optional, the path the group will be under
        labels:                                                        # Optional, all fields Mandatory
          - name: "label2"
            color: "#00FF00"
            description: "This is label 2"
            state: present                                             # Optional. default present


    projects:                                                          # This key will be removed in the future in favour of `repositories`
      - name: "Ansible Playbooks"
        labels:                                                        # Optional, all fields Mandatory
          - name: "label20"
            color: "#00FF00"
            description: "This is label 2"
            state: absent                                              # Optional. default present
        group: nofusscomputing/projects/ansible


    repositories:
      - api_url: "https://gitlab.com"                                    # This key will be removed in the future
        api_token_owner:                                                 # This key will be removed in the future
        api_token:                                                       # This key will be removed in the future
        projects:                                                        # This key will be removed in the future, with the projects list moving under `repositories`

          - name: "Ansible Playbooks"                                    # Mandatory, the human readable name of the repository
            path: ansible_playbooks                                      # Optional, default is derived from name in lowercase and spaces replaced with `_`
            labels:                                                      # Optional, all fields Mandatory
              - name: "label20"
                color: "#00FF00"
                description: "This is label 2"
                state: present                                           # Optional. default present
            avatar:                                                      # Optional, the url to the avatar
            branches:                                                    # Optional, if not specified, won't create branches
              - name: master
                merge_access_levels: "maintainer"                        # Optional, default=maintainer
                push_access_level: "maintainer"                          # Optional, default=none
              - name: development
                merge_access_levels: "developer"                         # Optional, default=maintainer
                push_access_level: "maintainer"                          # Optional, default=none
                ref_branch: master                                       # Optional, default master
            builds_access_level: enabled                                 # Optional, default disabled
            container_registry_access_level: enabled                     # Optional, default disabled
            description: "Ansible Playbooks"                             # Optional, default is blank
            environments_access_level: enabled                           # Optional, default disabled
            security_and_compliance_access_level: enabled                # Optional, default disabled
            packages_enabled: false                                      # Optional, default false
            group: nofusscomputing/projects/ansible                      # Mandatory, where the project belongs
            licence:                                                     # Optional, default is blank
              name: 'mit'                                                # optional, [mit, apache-2.0] default 'Copyright All Rights Reserved'
            releases_access_level: enabled                               # Optional, default disabled
            topics:                                                      # Optional, default=none
              - Ansible
              - "Ansible Tower"
              - Automation
              - AWX
              - Playbooks
            visibility: public                                           # Optional, default=private
            pages_access_level: public                                   # Optional, default disabled
            readme:                                                      # Optional, default is blank
              title: "the readme title"                                  # Mandatory
              manage: true
              auto_merge: true                                           # optional, default=false
              status: active
              badges: true
              mirror:                                                    # Optional, all fields Mandatory
                provider: github
                path: NofussComputing/ansible_playbooks
                web_url: url to the github repo

```