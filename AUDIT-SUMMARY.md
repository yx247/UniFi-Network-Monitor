# Public Release Privacy & Security Audit Summary

Version audited: **1.1.1**
Public package: `unifi-network-monitor-1.1.1.zip`
SHA-256: `d356301c209ebbff5e30b92efd1bfbede5064c7c29c1827f117f31a5bb5ad65c`

## Result

**The public kit in this directory is approved for public distribution / store
submission, subject to the screenshot requirement below.**

The package is a neutral rebuild of the audited v1.1.1 source:

- Neutral app ID `unifi-network-monitor`; neutral author `UniFi Monitor Contributors`.
- Five files only: `app.json`, `main.js`, `icon.png`, `zh-CN.json`, `en-US.json`.
- No API key/token/cookie/password/private key, no real IP/MAC/SSID/VLAN/device/
  client/traffic data, no private certificate, no developer-server URL.
- No source map, no screenshots, no test fixtures, no browser captures, no cache.
- No telemetry, analytics, tracking or hidden upload.
- GET-only; only the user-configured UniFi gateway origin is contacted.
- User-scoped config/auth/cache data nodes; neutral app ID means no inheritance of
  the developer’s Sun-Panel data nodes or cache.
- No default API key; the app does not connect until the user enters their own
  gateway URL and key.

## Screenshot requirement

This kit intentionally contains **no screenshots**. All current real screenshots
are private and must not be published. Before store submission, create new
screenshots using simulated/demo data and label them clearly as demonstrations.
Do not use the private `evidence/` images.

## Private material

The private development workspace (source, Git history, evidence, acceptance/
research/test reports, certificate and v1.0/v1.1 archives) is **not** approved for
public release. See `PUBLIC-RELEASE-MANIFEST.md` and the detailed private audit
report for the full prohibited list.

## Upload status

No file was uploaded to GitHub, a micro-app store or any third party. The fresh
public git repository has no remote.
