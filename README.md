# Require Docs Update Action

A lightweight, zero-dependency composite GitHub Action that alerts contributors if they submit code changes without accompanying documentation updates.

## Usage

Add the following workflow file to your project under `.github/workflows/docs-check.yml`:

```yaml
name: Documentation Check

on:
  pull_request:
    types: [opened, synchronize]

jobs:
  check-docs:
    runs-on: ubuntu-latest
    steps:
      - name: Verify Docs Updated
        uses: mokshitknowsyoursecret-png/require-docs-action@v1.0.0
        with:
          github-token: ${{ secrets.GITHUB_TOKEN }}
