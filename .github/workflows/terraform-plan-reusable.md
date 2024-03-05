# Terraform Plan Reusable Workflow

The reusable workflow is used to apply terraform scripts to AWS environment.

[terraform-plan-reusable.yaml](terraform-plan-reusable.yaml)

## Parameters

### Inputs

- `destroy`: `Optional` Whether to destroy resources. Default value `false`.
- `environment`: `Required` Environment to run against.
- `nickname`: `Required` Nickname of the project. Must be lowercase chars.
- `packages-directory`: `Optional` Where terraform script to build the packages (zip files).
- `tf-version`: `Optional` Terraform version. Default value `1.4.2`.
- `working-directory`: `Required` Terraform working directory.

### Outputs

- `exitcode`: The terraform plan exit code.

## Usage

```yaml
build:
  uses: camillehe1992/reusable-workflows/.github/workflows/terraform-plan-reusable.yaml@main
  secrets: inherit
  with:
    environment: barfoo
    nickname: bar
    packages-directory: foobar
    working-directory: foo
```
