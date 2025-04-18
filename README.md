<!--
# SPDX-License-Identifier: Apache-2.0
# SPDX-FileCopyrightText: 2025 The Linux Foundation
-->

# 📦 Verify Build Artefacts with Twine

Checks validity of Python build artefacts; call before package publishing.

## python-twine-check-action

## Usage Example

<!-- markdownlint-disable MD046 -->

```yaml
  - name: "Verify Python build artefacts with Twine"
    uses: lfreleng-actions/python-twine-check-action@main
```

<!-- markdownlint-enable MD046 -->

## Inputs

<!-- markdownlint-disable MD013 -->

| Variable Name | Required | Default | Description                           |
| ------------- | -------- | ------- | ------------------------------------- |
| PATH_PREFIX   | False    |         | Path/directory to Python project code |
| PATH          | False    | dist    | Path to Python build artefacts        |

<!-- markdownlint-enable MD013 -->

## Outputs

This action has no outputs, but will exit with an error if artefact
validation fails.

## Notes

When calling this action separate from a build job, ensure build products are
available by using upload/download artefacts.

## Action Output Example

```console
Run lfreleng-actions/python-twine-check-action@main
Run # Verify Python build artefacts with Twine
osc_github_devops-0.1.28.dev1-py3-none-any.whl
osc_github_devops-0.1.28.dev1.tar.gz
Files in specified directory/path: 2
Installing: twine
Running: twine check dist/*
Checking dist/osc_github_devops-0.1.28.dev1-py3-none-any.whl: PASSED
Checking dist/osc_github_devops-0.1.28.dev1.tar.gz: PASSED
Verified Python build artefacts with Twine ✅
```
