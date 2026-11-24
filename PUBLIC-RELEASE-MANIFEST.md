# Public Release Manifest

This directory is the **only approved public set** for the v1.1.1 distribution.
It is deliberately separate from the private development/acceptance workspace.

## Approved public files

- `unifi-network-monitor-1.1.1.zip` — installable package
- `README.md` — public description/install/security summary
- `PRIVACY.md` — privacy notice
- `SECURITY.md` — security notes
- `CHANGELOG.md` — public changelog
- `LICENSE` — MIT
- `THIRD-PARTY.md` — third-party notices
- `SHA256SUMS` — checksums
- `PUBLIC-RELEASE-MANIFEST.md` — this file

## Not approved for public release

Everything outside this directory is private, including:

- `evidence/` (real screenshots, real network/device/client data)
- `docs/ACCEPTANCE*.md`, `docs/TEST-REPORT.md`, `docs/RESEARCH-v1.1.1.md`
- `docs/ucg-unifi.pem`, `docs/INSTALL.md`, `docs/ROLLBACK.md`,
  `docs/TROUBLESHOOTING.md`, `docs/CAPABILITY-MATRIX.md`, `docs/API.md`
- `.playwright-mcp/`, browser captures, console logs and network traces
- the private Git repository/history, tags, author email and deleted-file objects
- private source tree and test fixtures unless separately re-audited and a fresh,
  scrubbed history is created
- v1.0.0/v1.1.0 private packages and archives

## Screenshot policy

No screenshots are in this public kit. All current screenshots are private evidence
containing real home-network data. Store screenshots must be produced with
simulated/demo data and labeled as demos before publication.
