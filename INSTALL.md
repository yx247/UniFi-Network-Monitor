# Installation

## Requirements

- Sun-Panel V2 PRO (micro-app SDK 1.0.19).
- A local UniFi Network controller reachable from the Sun-Panel container.
- A UniFi local API key created in **UniFi Network → Integrations**.
- For a self-signed controller certificate: add the certificate to the Sun-Panel
  container trust store and use the certificate hostname. Do not disable TLS
  verification.

## Install

1. Open Sun-Panel → **Micro-app management**.
2. Enter **Developer mode**.
3. Choose **Local install** and upload `unifi-network-monitor-1.1.1.zip`.
4. Add the **UniFi Network Monitor** widget and/or open its settings.
5. In settings enter **your own** controller URL (scheme + host + HTTPS port; no
   path, username or password) and **your own** API key.
6. Use **Test connection**, then **Save & apply**.
7. Add the widget to a home group and choose a supported size.

The app starts with no gateway, API key, device data or cache. It makes no network
request until a host and API key are saved.

## Recommended controller setup

- Create a dedicated local API key; give it a clear name and rotation date.
- Keep the key in the Sun-Panel user-scoped data node; do not put it in URLs,
  screenshots, tickets or source control.
- If your controller uses a self-signed certificate, trust that certificate in the
  Sun-Panel container. Never use a global TLS-verification bypass.

## Widget sizes

1×1, 1×2, 2×1, 2×2, 2×4, 1×full and 4×4. Use the widget settings to choose which
modules appear; when space is insufficient, a `+N` hint is shown instead of
silently dropping selected modules.

## Update / uninstall

- Update: install a newer package through the same local-install flow.
- Uninstall: Sun-Panel → Micro-app management → manage → uninstall.
- Remove the widget and, if desired, the app's user-scoped `unifiConfig`,
  `unifiAuth` and `unifiCache` data nodes.

## Troubleshooting

- **TLS / certificate error**: trust the controller certificate in the container;
  verify the hostname matches the certificate.
- **DNS**: use a hostname resolvable from the Sun-Panel container; an IP address
  works only if the controller certificate covers it.
- **401/403**: re-check the local API key and its permissions.
- **No WAN traffic/loss**: these fields come from the controller's aggregated
  dashboard; if the controller version does not expose them, they show “not
  available”.
- **VPN count / SFP DDM**: not available in the tested REST/port fields; no values
  are fabricated.
