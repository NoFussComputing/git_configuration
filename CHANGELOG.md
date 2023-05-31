## 0.3.0 (2023-05-31)

### Bug Fixes

- **submodule**: [2d2bca67](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/commit/2d2bca6703df611bb95c1b8a971fadf1fb10c3bb) - only set MR approval facts if an mr exists [ [!22](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/merge_requests/22) ]
- **submodule**: [d1ba66bb](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/commit/d1ba66bb916678852c2814cb03e8255d18ac77b2) - only create MR when there is a branch [ [!22](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/merge_requests/22) ]
- **submodule**: [99c4ec4b](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/commit/99c4ec4be2fb2128dff2e4f2b119cf23af178d7c) - add pause so that when merging gitlab has caught up [ [!22](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/merge_requests/22) ]
- **submodule**: [df0a497e](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/commit/df0a497edea9a3014a0e7771f07a3a3cbde8efb0) - generate MR comment logic failed [ [!22](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/merge_requests/22) ]
- **submodule**: [2ca3e54e](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/commit/2ca3e54e8471496f4873b3023f9437486f0197aa) - comment logic updated to rely on changes [ [!22](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/merge_requests/22) [#13](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/issues/13) ]
- **submodule**: [db644d8b](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/commit/db644d8b2926ae269696915de8fee7af3f9aa4c0) - new MR set correct notes URL [ [!22](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/merge_requests/22) ]
- **submodule**: [cb75bab4](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/commit/cb75bab4f3500d94ea589f075bdb836bc266bd14) - always check for existing MR [ [!21](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/merge_requests/21) [#11](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/issues/11) ]

### Code Refactor

- **submodule**: [1f0d0fb4](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/commit/1f0d0fb48d2e9fa321207d2b644e7b9c0f3d525e) - adjust logic to clone to empty dir [ [!22](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/merge_requests/22) ]
- **submodule**: [217d50cd](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/commit/217d50cdf4685f8e256a3779bc650d24b80b09be) - debug output make nice [ [!22](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/merge_requests/22) ]

### Features

- **submodule**: [1e6c6bae](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/commit/1e6c6baef2e817b8ba6e7e85f90e113702077583) - on merge, allow all valid status returns [ [!22](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/merge_requests/22) [#12](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/issues/12) ]
- **submodule**: [0e838d9b](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/commit/0e838d9ba9afb663c67cac7f64a4943f54460eb7) - comment with debug info on failed merge [ [!22](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/merge_requests/22) [#12](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/issues/12) ]
- **submodule**: [025b4a87](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/commit/025b4a87e37fcd4b975a8d724995a3cdfc630288) - comment approval status [ [!22](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/merge_requests/22) [#12](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/issues/12) ]
- **submodule**: [9618c39e](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/commit/9618c39ebb0bf12a96b230887615b99a80c99c18) - auto approval of MR if able [ [!22](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/merge_requests/22) [#12](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/issues/12) ]
- **submodule**: [8109cbf8](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/commit/8109cbf827b01dbeb9ae1934fc3d84b17c273333) - debug output for tasks and var creation [ [!22](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/merge_requests/22) [#12](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/issues/12) ]
- **submodule**: [a01f7d49](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/commit/a01f7d49b36e2c2bce8ab1c7d986c0b4a8042e9c) - debug output mr comment task [ [!22](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/merge_requests/22) ]
- **submodule**: [589cb510](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/commit/589cb5101987b27f67c8219395ce8fee36d6dc8a) - add icons to mr [ [!22](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/merge_requests/22) [#13](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/issues/13) [#14](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/issues/14) ]
- **submodule**: [ca0779e5](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/commit/ca0779e5216bc84f8ddea7919f31ab5eb443cc9d) - add job details to mr comment and description [ [!22](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/merge_requests/22) ]
- **submodule**: [4f2005ee](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/commit/4f2005ee7d150b9aba7a3c8424828e7fa68421ff) - create MR when description exists and no MR if exists [ [!22](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/merge_requests/22) ]
- **submodule**: [b7d34206](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/commit/b7d34206f93b9da618e317ea9075daaf84758ccf) - create mr description when no existing mr [ [!22](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/merge_requests/22) ]
- **ci**: [65ab15a5](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/commit/65ab15a54649aa984f01ccc400d823b292a9c8b0) - add automation config [ [!22](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/merge_requests/22) ]
- **submodule**: [a0d406d6](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/commit/a0d406d6a0b2efab3f321fc43567df0cae2833be) - output MR details [ [!22](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/merge_requests/22) [#14](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/issues/14) ]
- **submodule**: [5a8b89a5](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/commit/5a8b89a5e8caeb4a3cceecca815b5910a80a70e5) - set to never fail checking for existing MR [ [!22](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/merge_requests/22) [#14](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/issues/14) ]

## 0.2.0 (2023-05-28)

### Bug Fixes

- **submodule**: [3db6a4b9](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/commit/3db6a4b98200f03e3b8f6c0cf0de8611121ddeef) - must use default branch for change checking [ [!18](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/merge_requests/18) ]
- **submodule**: [5c71a5e1](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/commit/5c71a5e19b3757e86a09aa72a3904151b173594a) - gitlab expansion use correct variables [ [!17](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/merge_requests/17) ]
- **submodule**: [a9da88b4](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/commit/a9da88b4e0d309f45c3a99c89cd34502e4e2de94) - specify remote on branch creation [ [!15](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/merge_requests/15) [#77](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/issues/77) [!14](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/merge_requests/14) ]
- **submodule**: [d2f65de2](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/commit/d2f65de2ab78a08643a0ca6ec7dea7d8d4300625) - add missing variable repo_root [ [!13](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/merge_requests/13) ]

### Code Refactor

- [c6e3e639](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/commit/c6e3e6394541132d8a3e2aea2a019a66825106d8) - fix linting errors [ [!18](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/merge_requests/18) ]

### Documentaton / Guides

- **submodule**: [c5c99ff6](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/commit/c5c99ff6c286535fb6d0fe25d08d9a6b98c3c147) - detail how tasks work in gitlab [ [!18](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/merge_requests/18) ]

### Features

- **ci**: [ad03f001](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/commit/ad03f001458d65181aef4dc373cb12bdb4057d54) - use ci repo automagic template for job creation [ [!18](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/merge_requests/18) ]
- **submodule**: [1843fda8](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/commit/1843fda83fa27c8aebec237c653c4520726a6314) - fetch branches [ [!16](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/merge_requests/16) [#77](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/issues/77) [!14](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/merge_requests/14) ]
- **submodule**: [bcd6c05f](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/commit/bcd6c05f52bea7a0999cfeceab8577e9c50eb9fb) - list available branches for debugging [ [!15](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/merge_requests/15) [#77](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/issues/77) [!14](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/merge_requests/14) ]
- **submodule**: [54a9d588](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/commit/54a9d588c2250076de053d4ba1d8e8e655e5811e) - read config from repossitory root [ [!14](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/merge_requests/14) [#8](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/issues/8) [!29](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/merge_requests/29) [!1](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/merge_requests/1) [#1](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/issues/1) [#25](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/issues/25) [#26](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/issues/26) ]

## 0.2.0rc0 (2023-05-26)

### Bug Fixes

- **readme**: [3299df15](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/commit/3299df159a6a439caac9cd86536f657875154f34) - typo in dev brnach badge [ [!12](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/merge_requests/12) ]

### Continious Integration

- **docs**: [092fa67f](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/commit/092fa67fa86d5947629d5b06c053cc3fcad2f07d) - add CI job to build docs ready for website [ [!12](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/merge_requests/12) [#5](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/issues/5) ]
- [6f83c0bb](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/commit/6f83c0bbbfe3203d7d4889f87e2774bd39132cf9) - update to current HEAD [ [!12](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/merge_requests/12) ]

### Documentaton / Guides

- **website**: [a57e6215](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/commit/a57e6215a74f6f37a5e006304519aaf3ca7ccb25) - fix repo url [ [!12](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/merge_requests/12) ]
- [a1b232ec](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/commit/a1b232ecb9cfcd592174a5a64abc696d055031cd) - initial creation of docs [ [!12](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/merge_requests/12) [#5](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/issues/5) ]
- **readme**: [5953eb5f](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/commit/5953eb5fc3589e954a48abba67a1c16278eb849c) - fix type in dev badge [ [!11](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/merge_requests/11) ]

### Features

- **git_submodule**: [86700c11](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/commit/86700c11cf24deb65848cc2766665ff5b93fbe4a) - added logic to detect gitlab CI and use [ [!12](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/merge_requests/12) [#5](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/issues/5) ]
- **git_submodule**: [081aa135](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/commit/081aa135a154d4fcd674684e15054ed6776ad568) - initial git submodule auto update [ [!12](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/merge_requests/12) [#5](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/issues/5) ]
- **ci**: [bae73fb2](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/commit/bae73fb22840fd391ba17354e71690580db40d2f) - use gitlab-ci template from nfc [ [!12](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/merge_requests/12) ]

## 0.1.0 (2023-05-15)

### Continious Integration

- [cc08e6f6](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/commit/cc08e6f6af570ca5b2ec9562f6ef1cf10620b45e) - update gitlab-ci sub module to current commit [ [!4](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/merge_requests/4) [!17](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/merge_requests/17) ]

## 0.1.0rc2 (2023-05-15)

### Continious Integration

- [cdf925d3](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/commit/cdf925d38ecb9a20b373d2c1f9c9928d514c4e3c) - update to include fixes [ [!22](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/merge_requests/22) [!8](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/merge_requests/8) [!22](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/merge_requests/22) ]

## 0.1.0rc1 (2023-05-14)

### Documentaton / Guides

- **readme**: [d2129f88](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/commit/d2129f88423f4f8ad47871fdef344c9641885528) - add a blurb [ [!7](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/merge_requests/7) ]
- **readme**: [973acaff](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/commit/973acaffed5bb460878b2796caf2652abf1f044c) - use correct title [ [!7](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/merge_requests/7) ]

## 0.1.0rc0 (2023-05-14)

### Bug Fixes

- **gitlab**: [318a4c3b](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/commit/318a4c3ba14863215bc3e3ad3904ca088b15b765) - typo in variable name to enable packages [ [!1](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/merge_requests/1) ]
- **github**: [2fd39afe](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/commit/2fd39afed5824375700803582bc798e723e6fcfa) - removed conflicting repository visibilty tag [ [!1](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/merge_requests/1) ]

### Code Refactor

- [8131cbef](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/commit/8131cbef6c43b9b935fa07001c1499d6d7c12153) - testing ci release [ [!6](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/merge_requests/6) ]
- **readme**: [f46c009c](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/commit/f46c009cf12490ae7135bdd57100f13c7ce01fac) - adjusting task flow and small fixes [ [!1](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/merge_requests/1) ]
- [a98ee5f6](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/commit/a98ee5f6776324706ad02ad835ca9fd1ad6d6364) - added incomplete readme management [ [!1](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/merge_requests/1) ]

### Continious Integration

- [5b2627b4](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/commit/5b2627b428d13bf2ede2121c506363393b8227e0) - run linter on git tag [ [!6](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/merge_requests/6) ]
- [8f36571a](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/commit/8f36571a515082dec987339052763dd50542c1e7) - update to current restructure head [ [!5](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/merge_requests/5) [#1](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/issues/1) ]
- [cf974d2b](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/commit/cf974d2bb0fcecc30a05de8d6c0030c0fb0ecc25) - update to new restructure [ [!1](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/merge_requests/1) ]
- [654e850c](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/commit/654e850c5ae61e3a420f4d9d34cc0777d5bb6882) - adding gitlab-ci project and initial jobs [ [!1](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/merge_requests/1) ]
- [6957ff2b](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/commit/6957ff2bb62b61042a0b9133c9855aad9d592539) - dummy ci job [ [!3](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/merge_requests/3) ]

### Documentaton / Guides

- **readme**: [3c18ebe4](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/commit/3c18ebe49c85e25d22dde567c79331468aea1bc5) - Updated Repository README

### Features

- **gitlab**: [fd92cd87](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/commit/fd92cd87a24f049859cf2e40a716459508e7c43d) - ci-cd job cleanup for both cli and gitlab-ci [ [!1](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/merge_requests/1) ]
- **gitlab**: [29f24ac2](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/commit/29f24ac218713f2e85e537f47503da306082dddd) - added initial ci jobs cleanup task [ [!1](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/merge_requests/1) ]
- **gitlab**: [e2c39825](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/commit/e2c39825877965805d27feebaa251b5366b38cbe) - seperated api tokon to owner/user [ [!1](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/merge_requests/1) ]
- **ci**: [8cebdc88](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/commit/8cebdc88f4d8f0367c73151399700c04514d1c31) - sync repo to github [ [!1](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/merge_requests/1) ]

## 0.0.1 (2023-05-04)
