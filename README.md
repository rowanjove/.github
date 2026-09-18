# RowanJove / .github

Shared organization configuration, community health templates, and reusable GitHub Actions workflows for repositories under `@rowanjove`.

---

## What's Inside

- **`profile/`**: Fallback profile configuration and organization intro.
- **`CONTRIBUTING.md`**: Global engineering standards, Conventional Commits policy, and PR workflow.
- **`SECURITY.md`**: Security vulnerability reporting and version support guidelines.
- **`CODE_OF_CONDUCT.md`**: Standard contributor code of conduct.
- **`.github/ISSUE_TEMPLATE/`**: Standard issue forms for reproducible bug reports and feature proposals.
- **`.github/PULL_REQUEST_TEMPLATE.md`**: Unified checklist for code review and verification.
- **`.github/workflows/`**:
  - `rust-ci.yml`: Cargo check, clippy, format, and test on Windows.
  - `tauri-windows.yml`: Windows desktop build for Tauri applications.
  - `python-ci.yml`: Ruff linting and Pytest runner.
  - `node-ci.yml`: TypeScript/Node/Extension lint and test runner.
  - `release-windows.yml`: Windows release packaging and SHA256 checksum generator.
  - `security-audit.yml`: Multi-ecosystem security vulnerability scanner.

---

## How to Use Reusable Workflows

In any `@rowanjove` repository, add a minimal workflow calling the shared workflow:

```yaml
name: CI

on:
  push:
    branches: [main]
  pull_request:

jobs:
  ci:
    uses: rowanjove/.github/.github/workflows/rust-ci.yml@main
```
