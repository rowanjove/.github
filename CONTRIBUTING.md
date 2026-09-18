# Contributing to RowanJove Projects

Thank you for your interest in contributing to RowanJove's open-source projects.

We build **local-first software for personal computing** with a strong emphasis on reliability, quiet technology, and long-term maintainability.

---

## Core Principles

1. **Local-first**: User data belongs on the user's local disk in standard, transparent formats (SQLite, Markdown, JSON). Telemetry and remote dependencies should be strictly opt-in or avoided.
2. **Maintenance depth > Repository count**: We prioritize stability, clean architecture, automated tests, and clear error recovery over cosmetic additions.
3. **Facts over buzzwords**: Documentation and PR descriptions should focus on technical trade-offs, reproducible benchmarks, and concrete functionality rather than hype.

---

## Commit Guidelines

All repositories adhere to [Conventional Commits](https://www.conventionalcommits.org/):

```text
<type>(<optional scope>): <description>

[optional body]

[optional footer(s)]
```

Common types:
- `feat`: A new feature
- `fix`: A bug fix
- `refactor`: Code change that neither fixes a bug nor adds a feature
- `perf`: Performance improvement
- `docs`: Documentation updates
- `test`: Adding or correcting tests
- `chore`: Tooling, dependency, or configuration changes

Examples:
- `feat(history): add incremental Chromium profile import`
- `fix(search): prevent stale FTS records after deletion`
- `refactor(storage): isolate WAL checkpoint handling`

---

## Pull Request Workflow

1. Fork the repository and create a feature branch (`git checkout -b feat/your-feature-name`).
2. Keep changes focused and minimal. Do not mix refactoring or styling with functional changes.
3. Ensure existing and newly added automated tests pass.
4. Verify code formatting and linting (e.g., `cargo clippy`, `ruff check`, `npm run lint`).
5. Open a Pull Request referencing any relevant issues.
