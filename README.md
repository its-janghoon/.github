# its-janghoon/.github

Default community files and shared workflows for every repository under
[its-janghoon](https://github.com/its-janghoon). A repository that has its own copy of a file
uses that one instead.

| File | What it is |
|---|---|
| [CONTRIBUTING.md](CONTRIBUTING.md) | Branches, commits and pull requests |
| [SECURITY.md](SECURITY.md) | How to report a vulnerability privately |
| [CODE_OF_CONDUCT.md](CODE_OF_CONDUCT.md) | How we talk to each other |
| [.github/pull_request_template.md](.github/pull_request_template.md) | The four sections every pull request fills in |
| [.github/ISSUE_TEMPLATE](.github/ISSUE_TEMPLATE) | Bug and feature forms |
| [.github/workflows/pr-policy.yml](.github/workflows/pr-policy.yml) | Reusable: open-PR cap and self-review gate |
| [.github/workflows/gitflow.yml](.github/workflows/gitflow.yml) | Reusable: `<type>/<slug>` branch names, and `main` back-merged into `develop` |
| [profile/README.md](profile/README.md) | About me |

## Using the shared workflows

Add these two files to a repository.

`.github/workflows/pr-policy.yml`:

```yaml
name: PR policy
on:
  pull_request_target:
    types: [opened, reopened, review_requested]
permissions:
  pull-requests: write
jobs:
  policy:
    uses: its-janghoon/.github/.github/workflows/pr-policy.yml@main
```

`.github/workflows/gitflow.yml`:

```yaml
name: gitflow
on:
  pull_request:
    types: [opened, reopened, edited, synchronize]
  push:
    branches: [main]
  workflow_dispatch:
permissions:
  contents: write
  pull-requests: write
jobs:
  gitflow:
    uses: its-janghoon/.github/.github/workflows/gitflow.yml@main
```

A repository without a `develop` branch only gets the branch-name check; the back-merge job
notices there is nothing to merge into and passes.
