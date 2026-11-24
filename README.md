# UniFi Network Monitor for Sun-Panel V2 PRO

A read-only UniFi monitoring micro-app for Sun-Panel V2 PRO. It shows dual-WAN
runtime, gateway/switch/AP health, wired/wireless clients and a topology view.

**Version:** 1.1.1
**Micro-app ID:** `unifi-network-monitor`
**Package:** `unifi-network-monitor-1.1.1.zip`
**SHA-256:** `d356301c209ebbff5e30b92efd1bfbede5064c7c29c1827f117f31a5bb5ad65c`

> This public distribution contains **no real network data, credentials, device
> names, screenshots or private certificates**. Screenshots are intentionally not
> shipped in this kit; generate store screenshots with simulated/demo data only.
> This package is built from the audited v1.1.1 source with a neutral app identity.

## Features

- Dual-WAN discovery without array-order assumptions; operator/ASN and active-WAN
  matching from controller data.
- Read-only WAN runtime: rates, latency, availability, packet loss, daily/monthly
  traffic, 7-day quality history and failover markers.
- Gateway, switch, AP and client details; port STP/errors/drops/PoE; SFP module
  presence; all historical speedtests.
- Seven widget sizes and configurable card modules; share one store/poller between
  widget and detail windows.
- GET-only requests through Sun-Panel network passthrough. No extra Docker,
  database, backend service, telemetry or developer-server upload.
- Missing values stay missing (`—/未获取`); availability is not used as packet
  loss, downtime is not used as failover count, and browser-side sampling is not
  used as calendar traffic.

## Requirements

- Sun-Panel V2 PRO with micro-app SDK 1.0.19.
- A local UniFi controller reachable from the Sun-Panel container.
- A user-created local UniFi API key (UniFi Network → Integrations).
- TLS trust for a self-signed controller certificate, if applicable.

## Install

1. Sun-Panel → Micro-app management → Developer mode → Local install.
2. Upload `unifi-network-monitor-1.1.1.zip`.
3. Open the app settings and enter **your own** controller URL (scheme + host +
   HTTPS port; no path/userinfo) and **your own** API key.
4. Add the widget and configure modules/size.

The package has no default gateway or API key. Other installations do not inherit
the developer’s Sun-Panel data nodes, cache or settings; the app ID is a neutral,
independent namespace. The default placeholder `https://unifi.local` is only a
form hint — no connection is made until you save your own host and key.

## Documentation

- [Installation](INSTALL.md)
- [Features](FEATURES.md)
- [Privacy notice](PRIVACY.md)
- [Security notes](SECURITY.md)
- [Changelog](CHANGELOG.md)
- [v1.1.1 release notes](RELEASE-NOTES-v1.1.1.md)

## Security / privacy

See [PRIVACY.md](PRIVACY.md) and [SECURITY.md](SECURITY.md).

- No analytics, telemetry, tracking, crash reporting or developer endpoint.
- No external request other than the user-configured UniFi gateway origin.
- API keys are stored only in Sun-Panel user-scoped `unifiAuth` data node and are
  injected by host template replacement; they are never bundled or logged.
- The app implements GET only; it does not restart devices, switch WAN, run
  speedtests or change UniFi configuration.
- The app does not ship a private certificate or trust override.

## Limitations

- VPN online count: not available from the tested REST endpoint (`/stat/vpn` 404;
  health reports only `vpn: unknown`). No count is fabricated.
- SFP+ DDM optical power/temperature/voltage: not exposed by the tested
  controller/port firmware; only `sfp_found` is shown. No DDM values are fabricated.
- AP temperature: not provided by the tested APs.
- The controller's aggregated-dashboard endpoint is an internal console contract;
  missing fields degrade to “not available”.
- No 60-minute soak was performed for the public build.

## License

MIT; see [LICENSE](LICENSE) and [THIRD-PARTY.md](THIRD-PARTY.md).

## Verification

```bash
shasum -a 256 unifi-network-monitor-1.1.1.zip
unzip -l unifi-network-monitor-1.1.1.zip
```

Expected SHA-256:
`d356301c209ebbff5e30b92efd1bfbede5064c7c29c1827f117f31a5bb5ad65c`
