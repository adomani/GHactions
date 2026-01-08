# GHactions

Personal GitHub actions

# Validate PR titles

```yaml
name: Validate PR title (using reusable workflow)

on:
  pull_request:
    types: [opened, edited, reopened, synchronize]

jobs:
  call-reusable:
    uses: your-org/your-repo/.github/workflows/reusable-validate-pr-title.yml@main
    with:
      prefixes: 'feat:,fix:,docs:' # customize per repo, comma-separated list
      case_insensitive: true       # optional, default `true`
      comment_on_failure: true     # optional, default `true`
```
