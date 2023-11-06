## Example usage

```
name: Deploy Serverless

on: [push]

jobs:
  deploy:
    runs-on: ubuntu-latest

    # This is required to get id-token for OIDC provider
    permissions:
      id-token: write
      contents: read    

    steps:
      - name: Checkout repo
        uses: actions/checkout@v3

      - name: Deploy Serverless
        uses: exzeo-devops/action-workflows/.github/actions/deploy-serverless@main
        with:
          role-arn: "arn:aws:iam::123456789012:role/customRole"
          audience: "test"

```