<!--
# SPDX-License-Identifier: Apache-2.0
# SPDX-FileCopyrightText: 2025 The Linux Foundation
-->

# Test Release Process

Repository that automatically raises trivial changes on a schedule. Uses the
[release-drafter](https://github.com/release-drafter/release-drafter/actions)
action to generate draft releases. A workflow runs every morning on a
schedule, generating a new pull request containing the current date. If a
pull request already exists, it gets updated, so duplicates are not created.
Manual invocation of the workflow (using workflow_dispatch) will also create a
pull request. Test the release process by pushing a semantic tag. Pushed tags
get tested for semantic versioning compliance, and if successful the draft
release gets promoted.

## test-release-process

## Notes

While creating releases, tests the following actions:

- lfreleng-actions/tag-push-verify-action
- lfreleng-actions/tag-validate-semantic-action
- lfreleng-actions/draft-release-promote-action

Could potentially also test:

- lfreleng-actions/tag-validate-calver-action
