# AGENTS.md

## Repository map

- `package.json`: package identity, Node engine, test script and private-publication flag.
- `package-lock.json`: resolved dependencies; update it with intended manifest changes.
- `test/smoke.test.js`: Node test-runner starter.
- `.github/workflows/ci.yml`: pinned shared Node CI caller.

## Development and validation

Read [CONTRIBUTING.md](CONTRIBUTING.md) for the required setup, exact local
commands and evidence requirements. After `npm ci`, run `npm test`; preserve the separate hosted coverage gate.
`package.json` is the version authority. The starter is private; publishing requires a deliberate package/release decision.

## Operating model

This repository is maintained by one developer. Automated review, tests and
security gates replace mandatory human approvals. Do not add CODEOWNERS approval
requirements, team assignments or a second-maintainer dependency. Use a focused
branch and reviewable pull request; preserve unrelated and unmerged work.

## Boundaries

Never commit credentials or sensitive data. Keep generated files reproducible.
Prefer one authoritative configuration and link to it from tool-specific files.
Preserve existing release, data, credential and privacy gates. An unavailable
check is not a pass, and a configured provider is not evidence of its execution.

Use [BOOTSTRAP.md](BOOTSTRAP.md) for adoption decisions. Keep the applicability
declarations in `.github/community-bootstrap.json` aligned with actual project
configuration; they do not substitute for observed GitHub settings.
