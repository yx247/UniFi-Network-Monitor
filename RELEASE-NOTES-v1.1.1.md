# UniFi Network Monitor v1.1.1

Read-only UniFi monitoring for Sun-Panel V2 PRO.

## Highlights

- Dual-WAN runtime with real packet loss, daily/monthly traffic, 7-day quality
  history and failover markers from the local controller’s console-equivalent
  aggregated dashboard.
- Seven widget sizes, configurable modules, client/port/speedtest details.
- Switch temperature/satisfaction/fan, AP top-level satisfaction/radio counters.
- Strict missing-data semantics: no fabricated zeros, availability is not packet
  loss, downtime is not failover.
- GET-only, no telemetry or developer upload, no extra Docker/database/backend.
- Neutral public identity; no real network data, screenshots, credentials or
  private certificates in the package.

## Install

See `INSTALL.md`. The app starts with no gateway/API key and does not connect until
you enter your own values.

## Package

- File: `unifi-network-monitor-1.1.1.zip`
- SHA-256: `d356301c209ebbff5e30b92efd1bfbede5064c7c29c1827f117f31a5bb5ad65c`

## Known limitations

- VPN online count: not available from the tested REST endpoint.
- SFP+ DDM optical diagnostics: not exposed by the tested controller/port firmware;
  only module presence is shown.
- AP temperature: not provided by the tested APs.
- No 60-minute soak was performed for the public build.

## License

MIT.
