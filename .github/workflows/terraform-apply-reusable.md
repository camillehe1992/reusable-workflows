# Terraform Apply Reusable Workflow

The reusable workflow is used to apply terraform scripts to AWS environment.

[terraform-apply-reusable.yaml](terraform-apply-reusable.yaml)

## Parameters

### Inputs

- `environment`: `Required` Environment to run against.
- `nickname`: `Required` Nickname of the project. Must be lowercase chars.
- `packages-directory`: `Optional` Where terraform script to build the packages (zip files).
- `tf-version`: `Optional` Terraform version. Default value `1.8.0`.
- `working-directory`: `Required` Terraform working directory.

### Outputs

- N/A

## Usage

```yaml
build:
  uses: camillehe1992/reusable-workflows/.github/workflows/terraform-apply-reusable.yaml@main
  secrets: inherit
  with:
    environment: barfoo
    nickname: bar
    working-directory: foo
```
