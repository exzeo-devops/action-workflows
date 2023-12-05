## Example usage

```
name: Assume Role

on: [push]

jobs:
  example:
    runs-on: ubuntu-latest

    # This is required to get id-token for OIDC provider
    permissions:
      id-token: write
      contents: read    

    steps:
      - name: Checkout repo
        uses: actions/checkout@v3

      - name: Assume Role
        uses: exzeo-devops/action-workflows/.github/actions/aws-assume-role@main
        with:
          role-arn: "arn:aws:iam::123456789012:role/customRole"
          audience: "test"

```