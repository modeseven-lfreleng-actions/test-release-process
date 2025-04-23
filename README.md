<!--
# SPDX-License-Identifier: Apache-2.0
# SPDX-FileCopyrightText: 2025 The Linux Foundation
-->

# Test Release Process

Repository that automatically raises trivial changes on a schedule. Uses the
[release-drafter](https://github.com/release-drafter/release-drafter/actions)
action to generate draft releases. A workflow runs every morning on a
schedule, generating a new tagged release with an incremented patch/version
number.

## test-release-process

##  Notes

While creating releases, tests the following actions:

- lfreleng-actions/tag-push-verify-action
- lfreleng-actions/tag-validate-semantic-action
- lfreleng-actions/tag-validate-calver-action
- lfreleng-actions/draft-release-promote-action
