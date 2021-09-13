# ROS Modified Packages

## Inputs

- base-branch
  - A branch typically set to base in a pull request.

## Outputs

- packages
  - Modified package names (space-separated).

## Sample Workflow Steps

```yaml
- uses: actions/checkout@v2
   with:
      fetch-depth: 0

- uses: tier4/github-actions/ros-modified-packages@sandbox
   id: modified-packages
   with:
      base-branch: origin/main

- shell: bash
   run: echo packages = ${{ steps.modified-packages.outputs.packages }}
```
