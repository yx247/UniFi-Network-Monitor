# Privacy Notice

UniFi Network Monitor is a local, read-only Sun-Panel micro-app.

## What it accesses

The app reads from the UniFi controller **that the user configures**. It does not
contact any developer, analytics, advertising or third-party server. It has no
telemetry, tracking, crash reporting, beacon or hidden upload.

The app reads: controller/site/device identity and health, WAN statistics, switch/
AP/port/radio statistics, client identity/connection statistics and historical
speedtests. It does not read PPPoE credentials or the controller’s enriched WAN
configuration.

## Credentials and local storage

- The gateway URL and preferences are stored in the Sun-Panel user-scoped
  `unifiConfig` data node.
- The local API key is stored in the Sun-Panel user-scoped `unifiAuth` data node.
- Snapshot/history cache is stored in the Sun-Panel user-scoped `unifiCache` node.
- Credentials are not included in the installation ZIP, source tree, logs,
  diagnostics or this public kit.
- Other users of the app do not inherit the developer’s data nodes, cache or
  settings. The public app uses an independent app ID.

## User controls

- IP masking is enabled by default; client-name hiding is available.
- WAN ASN is hidden by default.
- The user can clear the API key, diagnostics and cache from settings.
- No data is sent to the developer; uninstalling the micro-app and deleting the
  user-scoped data nodes removes its local data.

## Screenshots and demos

This public kit intentionally includes **no screenshots**. Existing development
evidence contains real home-network data and is not approved for publication.
Any store screenshot must be generated with simulated/demo data and clearly
labelled as a demonstration, never as real monitoring data.

## Public package

The public package contains only compiled app assets, locales, icon, manifest,
license and this notice. It has no real IP/MAC/SSID/device/client/history data,
no API key/token/cookie/password, no private certificate and no developer-server
address.
