## 0.5.0 (2023-06-19)

### Bug Fixes

- **ci**: [c10ce0a9](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/commit/c10ce0a94704f99a1af2335aacb140a4fb0df2ab) - multiple to get integration testing working [ [!102](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/merge_requests/102) ]
- **ci**: [48f34f63](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/commit/48f34f63d635aefb9a365066a51fc11d6d2672d2) - added missing file [ [#19](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/issues/19) [!112](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/merge_requests/112) ]
- **gitlab_issue_patch**: [9e8f71f8](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/commit/9e8f71f8c9cafdb22ed1a95d342902be43502670) - pause for 5 seconds for gitlab api [ [#19](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/issues/19) ]
- **gitlab_issue_patch**: [df2968e1](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/commit/df2968e1937eba0d8bc04ee4c8ded152235da58e) - corrected task variable run [ [#19](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/issues/19) ]
- **docs**: [aec31ea9](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/commit/aec31ea9dd5e20df4a5975d5377ba7986eac6ee5) - correct the navigation for gitlab

### Code Refactor

- **gitlab_issue_patch**: [581d2601](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/commit/581d2601a72572b92b9d0e69dd3fd55630c0566d) - moved repo_root var global [ [#19](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/issues/19) ]
- **gitlab_issue_patch**: [971faac4](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/commit/971faac4cb8ea82632c84c0b9bcd8bfefcc1b2d9) - stopped logging not-required and added task output [ [#19](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/issues/19) ]
- **git**: [b4ff2622](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/commit/b4ff26222ab4edd17e9169bddcbc068b78341760) - renamed task ensure branch exist -> show current [ [#19](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/issues/19) ]
- **gitlab_projects**: [f8271d94](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/commit/f8271d948cc6d645eaa973392a26ba43ebb6fd64) - notate why no log [ [#19](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/issues/19) ]
- **gitlab_notes**: [20dc8d54](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/commit/20dc8d5432b95db03bce27c9f44c5b87c4be982c) - group related tasks for filtering [ [#19](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/issues/19) ]
- **issue**: [a51184ef](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/commit/a51184efbee85132157d7a55a676aefce38c1742) - group related tasks for filtering [ [#19](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/issues/19) ]
- **issue_patches**: [723b6b11](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/commit/723b6b11d9bec351198b42ad2c4ed313c2b0452e) - adjust logic so it works as intended [ [#19](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/issues/19) ]
- [9e18e81e](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/commit/9e18e81e41de79d69c930b9821db7b332b37f55d) - adjust the git var [ [#18](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/issues/18) ]

### Continious Integration

- **automation**: [70cd3d5b](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/commit/70cd3d5b9e76f891e64ee7ea3d6a16fe252d730e) - updated config file with mr patch labels [ [#19](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/issues/19) ]

### Documentaton / Guides

- [6ac26e08](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/commit/6ac26e08b35417754b8949a4edddd28cd0e4bb8f) - countless code review suggested fixes. [ [!112](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/merge_requests/112) ]
- **gitlab_issue_patches**: [6ee6b221](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/commit/6ee6b221007ab28be8e326b884bd3b2b0ede32ac) - remaining docs for the tasks and automation [ [#19](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/issues/19) ]
- [4b94495b](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/commit/4b94495bc6471b16db272f6b160e0dee05869354) - update navigation structure [ [#19](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/issues/19) ]
- **gitlab**: [bcc0e9fa](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/commit/bcc0e9fab9f8a478b365066fb6b1b650f383cd26) - task file issue patches [ [#19](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/issues/19) ]
- **gitlab**: [b67f2311](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/commit/b67f23110f33dfd1fa6c5e9fcf4ba0ab4dd7af36) - task file projects [ [#19](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/issues/19) ]
- **gitlab**: [d50740db](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/commit/d50740db83137fb8cae68ed48957bfe8bf9bfe16) - task file notes [ [#19](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/issues/19) ]
- **gitlab**: [8e35bf83](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/commit/8e35bf837c886ab6b84a64bac9eb94d84327b61a) - task file issues [ [#19](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/issues/19) ]
- [803dd4fc](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/commit/803dd4fc8e74a2e88ef70d3400dd9ffa576a234e) - remove wrong wording
- **gitlab**: [630db299](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/commit/630db2999fdc62045734b62c2c0a384143d6e561) - manage gitlab group/project labels [ [#18](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/issues/18) ]

### Features

- **gitlab_issue_patch**: [7b514d25](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/commit/7b514d25a435615b002f2a28cc27aeaf8c05aaac) - remove patch that failes git apply --check [ [#19](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/issues/19) ]
- **gitlab_issue_patches**: [6fdf3f98](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/commit/6fdf3f9871ca76dd2141a0959bb4c8f89dbe86ea) - Added support for running in gitlab CD/CI environment [ [#19](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/issues/19) ]
- **automation**: [b339b9df](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/commit/b339b9dfa8c60d1ab0207eb4a7e60c063057a04a) - add automation for fetching issue patch files and creating a merge request. [ [#19](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/issues/19) ]
- **gitlab_issue_patches**: [375959f3](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/commit/375959f3238d8099892a16cc9478e20820dc5481) - Add patch comment user membership to metadata [ [#19](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/issues/19) ]
- **gitlab**: [2e1850e8](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/commit/2e1850e8f4e7c9a49b71cb79f038df82506ef568) - fetch project membership, inlcuding inherited [ [#19](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/issues/19) ]
- **gitlab**: [e0d5c50d](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/commit/e0d5c50d1475b8419eddc5423f9f96d26e28d6f4) - comment on merge request [ [#19](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/issues/19) ]
- **gitlab**: [e6ada4c2](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/commit/e6ada4c25bf67bee15cbd2fca0079a533f02e86a) - edit comment under issue [ [#19](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/issues/19) ]
- **gitlab**: [9fbf02c2](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/commit/9fbf02c2beacf4875461494ddb3dbb5efa07c11f) - add comment to issue [ [#19](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/issues/19) ]
- **gitlab**: [3a36572c](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/commit/3a36572cebfa291cd487b62f18e764d747b433b0) - reply to discussion [ [#19](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/issues/19) ]
- **gitlab**: [3420fde8](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/commit/3420fde8988a8702233464e0f975e3a18528c20d) - ability to fetch issue related MR [ [#19](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/issues/19) ]
- **gitlab**: [a2c64ed9](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/commit/a2c64ed9cf063f4d3178c76c5969e063a7de4a96) - Create a Merge Request if one doesn't already exist [ [#19](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/issues/19) ]
- **repository**: [5a742262](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/commit/5a7422627f03768cf5fcaef1997670fb7e50f1e4) - push branch [ [#19](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/issues/19) ]
- **repository**: [c11c046d](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/commit/c11c046d8770db7df13c39d6be7ca024118915ea) - check if local branch exists [ [#19](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/issues/19) ]
- **repository**: [97ceea0f](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/commit/97ceea0f95973fb15552b79ce8893522197c09c7) - create branch if not on remote [ [#19](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/issues/19) ]
- **repository**: [57199547](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/commit/571995475f642b23710d4db8d48ae86caea9f8bc) - set git user details for local repository [ [#19](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/issues/19) ]
- **repository**: [3337f6ce](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/commit/3337f6ce62565d8e7b424f0517a573bd77475260) - Clone a repository [ [#19](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/issues/19) ]
- **patch**: [70421bd0](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/commit/70421bd062455077013a207919fd188cbf8b2d28) - apply a patch file to a local branch [ [#19](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/issues/19) ]
- **patch**: [02f9e899](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/commit/02f9e899a5457e5caae07307f507e18097c2ab3e) - download patch file from url [ [#19](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/issues/19) ]
- **gitlab**: [93c06340](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/commit/93c063404d83c7fb245d28eb5824fb41f4bbf6c3) - task file issue patches [ [#19](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/issues/19) ]
- **gitlab**: [a8a9c9d7](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/commit/a8a9c9d723b469f17c8467ac3716301052c06658) - task file projects [ [#19](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/issues/19) ]
- **gitlab**: [c572d47d](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/commit/c572d47de3c670c155c6fca11f7c5bbfdef3ccc4) - task file notes [ [#19](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/issues/19) ]
- **gitlab**: [1cf31f90](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/commit/1cf31f90d67cabc5db1ba75e7ed5e978a38bec60) - task file issues [ [#19](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/issues/19) ]
- **gitlab**: [5dc13785](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/commit/5dc13785a439266c11b0e2fefe570cecd82a1f5d) - manage gitlab group/project labels [ [#18](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/issues/18) ]

## 0.4.0 (2023-06-15)

### Bug Fixes

- **submodule**: [d161ae40](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/commit/d161ae40aa5208a4cd8c3156cc8d8555fd98e93c) - don't push branch if there are no changes [ [!94](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/merge_requests/94) [#19](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/issues/19) ]
- **submodule**: [75b2d6c5](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/commit/75b2d6c5155909a307ba2fb93796abc8df7e7506) - debug item don't change [ [!87](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/merge_requests/87) ]
- **submodule**: [76dd7451](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/commit/76dd7451dee28d9a80c4ee2b379faf9bba53b74b) - correct workflow for git submodule update [ [!87](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/merge_requests/87) ]
- **submodule**: [2167217a](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/commit/2167217a9091ca59bfb84fbfb32a16cda9ad2702) - correct workflow for git submodule update [ [!79](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/merge_requests/79) [!55](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/merge_requests/55) ]
- **submodule**: [caa7acee](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/commit/caa7aceec15464c00ea307023535d2794903e081) - if no approval required enable merging [ [!79](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/merge_requests/79) [!40](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/merge_requests/40) ]
- **submodule**: [2e8961d4](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/commit/2e8961d4d1a50c3eea63d301bc8b6f1a5749e8c7) - check if user can approve [ [!78](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/merge_requests/78) ]

### Code Refactor

- **submodule**: [e7dfcfee](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/commit/e7dfcfee03ab03a066a0afb8a78c99f625142df3) - default to empty jina value [ [!78](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/merge_requests/78) ]

### Features

- **submodule**: [d7e721a8](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/commit/d7e721a815537975abf28c2a4e33b4193f5f5a82) - debug output git status prior to commit [ [!79](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/merge_requests/79) ]
- **submodule**: [d9b29cea](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/commit/d9b29cea0b627c27a5a610bc6ec838876ff465cd) - additional debug output [ [!78](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/merge_requests/78) ]

## 0.4.0rc2 (2023-06-07)

### Bug Fixes

- **submlodule**: [e0e7a4af](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/commit/e0e7a4af8b3915e2bc233617e7f230a7d6f177df) - commit changes state changed when changed [ [!76](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/merge_requests/76) [#17](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/issues/17) ]
- **submlodule**: [a04e509e](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/commit/a04e509eccbd055571ef3cc6e3d4cfd2d4699602) - on new branch init submodule [ [!76](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/merge_requests/76) [#17](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/issues/17) ]
- **submlodule**: [b9a43416](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/commit/b9a434165dfa56ade41f10c792ac24cfad469413) - only update for update step [ [!76](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/merge_requests/76) [#17](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/issues/17) ]
- **submlodule**: [b2e36b34](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/commit/b2e36b34e3482d374f37caf48e64223824656ab7) - existing branch init submodule [ [!76](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/merge_requests/76) [#17](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/issues/17) ]
- **submodule**: [ea7447ee](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/commit/ea7447eec3ebb89c87083490e36334668d77b166) - use module path, not name [ [!75](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/merge_requests/75) ]
- **submodule**: [4757090b](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/commit/4757090b74c337901e9511b0d0fca20d3751807a) - use correct var for checking approal user [ [!74](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/merge_requests/74) ]

### Documentaton / Guides

- **submlodule**: [852df76f](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/commit/852df76f9e46c5d7bef0916fa201c78654ad9e5f) - updated intro blurb [ [!76](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/merge_requests/76) [#17](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/issues/17) ]
- [523d7e02](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/commit/523d7e025fa9ed1e0d697f22c88cb9273cc11673) - title/description metadata update [ [!10](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/merge_requests/10) [#10](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/issues/10) ]
- **home**: [4248880f](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/commit/4248880f00868ccd93bfa5abd0fb7f267ee6dd3a) - added features and expanded intro [ [!10](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/merge_requests/10) [#10](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/issues/10) ]
- **gitlab**: [3068c708](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/commit/3068c708ea3df730ac8672ffc08a3cb806efcb0a) - added intro [ [!10](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/merge_requests/10) [#10](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/issues/10) ]
- **github**: [6c25196a](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/commit/6c25196ae3d90cadb1611fb1fceb2c14f1950960) - initial github page [ [!10](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/merge_requests/10) [#10](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/issues/10) ]
- **placeholders**: [1380d176](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/commit/1380d1762e947b91a7b1c7c4374fe6488b1a186d) - add external place holders for links [ [!10](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/merge_requests/10) [#10](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/issues/10) ]
- **index**: [bd18dc7a](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/commit/bd18dc7a71a3021333e5cd27ec0547d9cf218eff) - added tips pointing to role and ee repo [ [#10](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/issues/10) ]

## 0.4.0rc1 (2023-06-05)

### Bug Fixes

- **gitlab**: [d5ba76e9](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/commit/d5ba76e9ffad43a6a423fdfe356f277ad0f6ee16) - correct creation path variable expansion [ [!67](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/merge_requests/67) ]
- **submodule**: [0da3f29a](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/commit/0da3f29a9f318201cb4e2f1862b43305113a2e79) - use .gitmodules to fetch path [ [!67](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/merge_requests/67) ]
- **submodule**: [31a00693](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/commit/31a006936f2a25c918356e96180d2000b5ac2000) - look for approvers in the correct location [ [!67](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/merge_requests/67) [!15](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/merge_requests/15) ]

### Features

- **submodule**: [5dfe8444](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/commit/5dfe84443955248e425d68963bd0185a99e568d2) - oadjust MR title to reflect specified module name [ [!67](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/merge_requests/67) ]
- **submodule**: [e294e27d](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/commit/e294e27d10526418c2794eb5fea8cc3a79f94818) - output failed mr comment api call [ [!67](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/merge_requests/67) ]

## 0.4.0rc0 (2023-06-03)

### Bug Fixes

- **submodule**: [94d4d449](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/commit/94d4d449c77dd9cdd18773413ab1991691b54db6) - correct failed var in specified module [ [!66](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/merge_requests/66) ]
- **submodule**: [a32e168c](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/commit/a32e168cdae093fe2301bc64e6e452b3f9318bff) - dont shallow clone [ [!66](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/merge_requests/66) ]
- **submodule**: [0339db37](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/commit/0339db37d33654b67d52138e7c06ed3aadebbf2d) - dont shallow clone [ [!63](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/merge_requests/63) ]
- **submodule**: [6fb0dab5](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/commit/6fb0dab5d957fae56fa19d9c6c13ae6cbaed6b8c) - use correct var in when clause [ [!63](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/merge_requests/63) ]
- **submodule**: [2bdbb303](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/commit/2bdbb303fba037cd7890bf8bf6ddeaec33bfba63) - ensure var expansion for specified correct [ [!62](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/merge_requests/62) [!48](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/merge_requests/48) ]
- **submodule**: [0439bb65](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/commit/0439bb65085ffcffa5800d26b832d866b34e43b7) - ensure existing mr changed [ [!60](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/merge_requests/60) [#16](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/issues/16) ]
- **ci**: [e118e7ee](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/commit/e118e7eec301a16684e0f539d8ada88bf2b9f916) - ensure unit test doesn't run on git tag [ [!55](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/merge_requests/55) [#15](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/issues/15) ]

### Code Refactor

- **submodule**: [a41793b0](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/commit/a41793b0e0d3ed2f55f65280f90d16dfd101691b) - use strong typing for vars [ [!62](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/merge_requests/62) [!48](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/merge_requests/48) ]
- **submodule**: [05fa3c26](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/commit/05fa3c263503855e12857169c691a7e1934aa3dd) - mr comment non-reqd vars set to empty [ [!62](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/merge_requests/62) [!48](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/merge_requests/48) ]

### Features

- **submodule**: [de2576f7](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/commit/de2576f7c4261f6a934ef2243cde623c85869c8a) - enable specifying module name to update [ [!60](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/merge_requests/60) [#16](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/issues/16) ]
- **ci**: [5825b40b](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/commit/5825b40bf3fa7a682ede6c2978982904989809ab) - update ansible-role git submodules [ [!55](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/merge_requests/55) [#6](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/issues/6) ]
- **gitlab**: [29279f72](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/commit/29279f72665c3d428df4bc873fbcadea5f9c5b9c) - ability to configure pages [ [!55](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/merge_requests/55) [#6](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/issues/6) ]
- **gitlab**: [6d46f6fa](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/commit/6d46f6fa9a267ebb66e2a094c18bd3607e29ada0) - path derived from name in lowercase no spaces [ [!55](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/merge_requests/55) [#7](https://gitlab.com/nofusscomputing/projects/ansible/git_configuration/-/issues/7) ]

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
