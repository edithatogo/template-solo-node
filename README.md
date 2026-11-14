# Solo-maintainer Node project template

[![CI](../../actions/workflows/ci.yml/badge.svg)](../../actions/workflows/ci.yml) [![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE) [![Citation](https://img.shields.io/badge/citation-CFF-blue.svg)](CITATION.cff)

A private Node 24 project baseline with reusable CI, real coverage, and Renovate.

## Status

This repository is designed for one maintainer. Automated checks are required;
no second reviewer, CODEOWNERS approval, team membership, or mandatory human
approval is introduced.

## Usage

Choose **Use this template** to create a Node project, then follow the
[adoption checklist](BOOTSTRAP.md). The initial runnable example is the smoke
test in `test/smoke.test.js`. The package is marked private and has no
application entry point until the project supplies one.

1. Replace `replace-me` in `package.json` and update the lockfile with the
   documented Node/npm toolchain.
2. Run `npm ci` to install from `package-lock.json`.
3. Run `npm test` to execute the Node test runner and generate c8 coverage.

## Development

See [CONTRIBUTING.md](CONTRIBUTING.md) for setup and validation commands, and
[BOOTSTRAP.md](BOOTSTRAP.md) for the adoption checklist.

The pinned shared CI installs from the lockfile and runs the Node test runner
through c8. It is configured to upload coverage through Codecov OIDC. Verify
provider activation and an actual upload in each generated repository.

## Versioning

`package.json` is authoritative. The starter is private; add release automation only if it becomes a published package.

## Logging

A library must not configure global logging. Applications and services should use a structured logger such as Pino at their entry point.

## Security

Follow [SECURITY.md](SECURITY.md) for private reporting and the safe contact
fallback if GitHub's **Report a vulnerability** option is unavailable. Do not
include credentials, sensitive source data or exploit details in public issues.

## Citation

See [CITATION.cff](CITATION.cff). Release-specific versions and identifiers are
added only when the release exists.

## License

Repository-authored starter material is MIT licensed; see [LICENSE](LICENSE).
Record third-party and source-data rights separately.
