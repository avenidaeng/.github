# Avenida Organization — `.github` Repository

This repository contains organization-wide GitHub configuration files that are automatically applied to all repositories in the **avenidaeng** organization.

## What's Included

### Community Health Files

These files are inherited by all repositories that don't have their own versions:

| File                                       | Purpose                                     |
| ------------------------------------------ | ------------------------------------------- |
| [CONTRIBUTING.md](./CONTRIBUTING.md)       | Contribution guidelines                     |
| [CODE_OF_CONDUCT.md](./CODE_OF_CONDUCT.md) | Community code of conduct                   |
| [SECURITY.md](./SECURITY.md)               | Security policy and vulnerability reporting |
| [SUPPORT.md](./SUPPORT.md)                 | How to get help                             |

### Issue & PR Templates

| File                                                                       | Purpose                      |
| -------------------------------------------------------------------------- | ---------------------------- |
| [PULL_REQUEST_TEMPLATE.md](./PULL_REQUEST_TEMPLATE.md)                     | Default PR template          |
| [ISSUE_TEMPLATE/bug_report.yml](./ISSUE_TEMPLATE/bug_report.yml)           | Bug report form              |
| [ISSUE_TEMPLATE/feature_request.yml](./ISSUE_TEMPLATE/feature_request.yml) | Feature request form         |
| [ISSUE_TEMPLATE/config.yml](./ISSUE_TEMPLATE/config.yml)                   | Issue template configuration |

### Organization Profile

| File                                     | Purpose                             |
| ---------------------------------------- | ----------------------------------- |
| [profile/README.md](./profile/README.md) | Organization landing page on GitHub |

### Reusable Workflows

Located in `.github/workflows/`:

| Workflow                   | Purpose                          |
| -------------------------- | -------------------------------- |
| `reusable-nextjs-ci.yml`   | CI for Next.js applications      |
| `reusable-packages-ci.yml` | CI for TypeScript packages       |
| `reusable-release.yml`     | Release workflow with Changesets |

#### Using Reusable Workflows

In your repository's workflow file:

```yaml
name: CI

on:
  push:
    branches: [main]
  pull_request:
    branches: [main]

jobs:
  ci:
    uses: avenidaeng/.github/.github/workflows/reusable-nextjs-ci.yml@main
    with:
      node-version: "22"
    secrets: inherit
```

## Repository Structure

```
.github/
├── profile/
│   └── README.md              # Organization landing page
├── ISSUE_TEMPLATE/
│   ├── bug_report.yml         # Bug report form
│   ├── feature_request.yml    # Feature request form
│   └── config.yml             # Template configuration
├── .github/
│   └── workflows/
│       ├── reusable-nextjs-ci.yml
│       ├── reusable-packages-ci.yml
│       └── reusable-release.yml
├── CONTRIBUTING.md
├── CODE_OF_CONDUCT.md
├── SECURITY.md
├── SUPPORT.md
├── PULL_REQUEST_TEMPLATE.md
└── README.md                  # This file
```

## Overriding Defaults

Any repository can override these defaults by creating their own versions of these files in their `.github/` folder.

## Related Repositories

- [avenidaeng](https://github.com/avenidaeng/avenidaeng) — Workspace configuration with Copilot instructions
- [avenida-web](https://github.com/avenidaeng/avenida-web) — Main web application
- [avenida-site](https://github.com/avenidaeng/avenida-site) — Marketing website
- [avenida-packages](https://github.com/avenidaeng/avenida-packages) — Shared TypeScript packages
- [avenida-extension](https://github.com/avenidaeng/avenida-extension) — Browser extension
- [avenida-infra](https://github.com/avenidaeng/avenida-infra) — Database infrastructure
