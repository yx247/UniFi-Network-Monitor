# Security Notes

## Permissions

- `network`: required to reach the user-configured local UniFi controller.
- `dataNode`: required for user-scoped config/auth/cache storage.

`networkDomains` is `["*"]` because the controller host is user-configurable. The
runtime client independently enforces that every request targets exactly the
configured gateway origin (scheme + host + port), rejects absolute/protocol-
relative paths, and implements GET only. A static host allow-list cannot represent
every user’s local controller.

## Credential handling

- The saved key is injected by Sun-Panel data-node template replacement; the app
  never embeds a key and masks credential-looking values in diagnostics.
- No cookie/session reuse, no TLS verification bypass, no private CA included.
- The app never reads the controller’s enriched WAN configuration containing
  PPPoE credentials.

## Read-only boundary

No reboot, WAN switch, active speedtest, firmware update, PoE control, firewall,
DHCP, DNS, VPN or other write operation is implemented. Only GET requests are
issued.

## Reporting

Report security issues to the project maintainer through the distribution channel
where you obtained the app. Do not include real API keys, private IPs, MAC
addresses, SSIDs or controller certificates in reports.
