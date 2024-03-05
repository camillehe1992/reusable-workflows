# Starter Reusable Workflow

The reusable workflow is used ...

[starter-reusable.yaml](starter-reusable.yaml)

## Parameters

### Inputs

- `input1`: `Required` the description of input1.
- `input2`: `Optional` the description of input2.

### Outputs

- `output1`: the description of output1.

## Usage

```yaml
build:
  uses: camillehe1992/reusable-workflows/.github/workflows/terraform-destroy-reusable.yaml@main
  with:
    input1: foo
    input2: bar

```
