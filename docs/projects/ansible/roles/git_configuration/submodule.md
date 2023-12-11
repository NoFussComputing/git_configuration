---
title: Automated repository git submodule updating
description: How to use No Fuss Computings Ansible role git configuration tagged task, git submodules to update your repositories git submodules.
date: 2023-05-26
template: project.html
about: https://gitlab.com/nofusscomputing/projects/ansible/git_configuration
---

!!! Note
    This documentation is still a work in progress

This task is designed to automate the updating of your repositories git submodules. Currently it supports being run from CLI or within the Gitlab CI/CD environment. To specifically run this group of tasks define the tag `--tags submodule`. Another feature of this role, even though we try to compensate/correct errors during the play, is that if any task fails for whatever reason-Run the play again to resolve.


## Required Variables

| Name | default | description |
|:---:| :---|:---|
| `submodule_name` | *not defined* | ***Optional** If specified and matches the name of a git submodule, will **Only** update that module.* |
| `submodule_branch` | *not defined* | ***Required** Branch to use for the git submodules.* |
| `default_branch` | *not defined* | ***Required** Repositories default branch.* |
| `mr_labels` | *not defined* | ***Required** Labels to add to the merge request, if created.* |
| `auto_merge` | `false` | ***Optional** If the job should automerge the merge request if created.* |

To run this task use `ansible-playbook {playbook name that uses git_configuration role}.yaml --tags submodule` ensure you set the requird variables with `--extra-args` or define them in your playbook.


When this automation is run from within the Gitlab CD/CI environment the following variables are used and automagically gathered from the environmental variables. most are self explanatory, with `CI` (boolean) being used as the variable to detect the Gitlab CD/CI environment:

- `CI_PROJECT_PATH`

- `GIT_COMMIT_TOKEN`

- `CI_PROJECT_DIR`

- `CI_JOB_ID`

- `CI_JOB_URL`

- `CI`

## Gitlab CI/CD Usage

This task has also been designed to work within the Gitlab CI/CD environment. The task auto detects this. However you must have a configuration file within the root of your repository for this to work. The required variables as listed above, must be specified within the `.yaml` file under the path `role_git_conf.gitlab`. Please refer to the [Gitlab config documentation](gitlab.md#Configuration) for further information.

Example Configuration file. 

``` yaml title=".nfc_automation.yaml" linenums="1"
---

role_git_conf:
  gitlab:
    submodule_branch: "development"
    default_branch: development
    mr_labels: ~"type::automation" ~"impact::0" ~"priority::0"
    auto_merge: true

```

!!! Notice
    if the config file `.nfc_automation.yaml` does not exist, the job will not run.

    Not specifying the required variables will cause the job to fail.

!!! tip
    Using our [gitlab-ci Project](../../../gitlab-ci/index.md) will enable you to either have this job automagically available or pre defined for you to create the job.


## Docs ToDo

- link the gitlab-ci automated task (auto-generated one)

- document the workflow
