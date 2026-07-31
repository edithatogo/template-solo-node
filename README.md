# Solo-maintainer Node project template

[![CI](../../actions/workflows/ci.yml/badge.svg)](../../actions/workflows/ci.yml) [![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE) [![Citation](https://img.shields.io/badge/citation-CFF-blue.svg)](CITATION.cff)

A private Node 24 project baseline with reusable CI, real coverage, and Renovate.

## Status

This repository is designed for one maintainer. Automated checks are required;
no second reviewer, CODEOWNERS approval, team membership, or mandatory human
approval is introduced.

## Start here

1. Replace `replace-me` in `package.json`.
2. Run `npm ci`.
3. Run `npm test`.

## Development

CI uses the lockfile, runs the Node test runner through c8, and uploads real coverage through Codecov OIDC.

## Versioning

`package.json` is authoritative. The starter is private; add release automation only if it becomes a published package.

## Logging

A library must not configure global logging. Applications and services should use a structured logger such as Pino at their entry point.

## Security

Report vulnerabilities privately through GitHub Security Advisories. See
[SECURITY.md](SECURITY.md); do not disclose credentials or sensitive source data
in a public issue.

## Citation

See [CITATION.cff](CITATION.cff). Release-specific versions and identifiers are
added only when the release exists.

## License

Repository-authored starter material is MIT licensed; see [LICENSE](LICENSE).
Record third-party and source-data rights separately.