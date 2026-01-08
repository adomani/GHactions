# GHactions

Personal GitHub actions

# Validate PR titles

```yaml
name: Validate PR title

on:
  pull_request:
    types: [opened, edited, reopened, synchronize]

jobs:
  validate-title:
    uses: adomani/GHactions/.github/workflows/validate_pr_title.yaml@validate_pr_title
    with:
      prefixes: 'feat:,fix:,docs:' # customize per repo, comma-separated list
      case_insensitive: true       # optional, default `true`
      comment_on_failure: true     # optional, default `true`
```
