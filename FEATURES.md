# Features

## Monitoring

- Automatic discovery of UniFi gateways, switches, APs, WANs and online clients;
  no hard-coded device inventory.
- Dual/multi-WAN identity by interface, not array index; operator, ASN, active WAN,
  IPv4/IPv6 presence and negotiated link speed.
- WAN rates, latency, availability, 5-minute packet loss, daily/monthly
  upload/download/total traffic, 7-day quality history and failover markers.
- Gateway CPU/memory/load/temperature/storage/ports/PoE.
- Switch ports, STP/errors/drops/PoE details, general temperature, satisfaction,
  fan/overheat and client counts.
- AP radios: channel/width/utilization/retries/power, top-level satisfaction,
  client counts and radio packet/retry counters.
- Client list and a dedicated detail window: address, VLAN/network, uplink/port,
  PHY link versus live throughput, signal/noise, channel, retries and timestamps.
- Port detail modal and all historical speedtest records with filtering and
  pagination.
- Topology with all reported clients, uplink port/speed and an explicit
  unknown-uplink group.

## Widget

- Seven sizes: 1×1, 1×2, 2×1, 2×2, 2×4, 1×full and 4×4.
- Selectable modules; space-insufficient hint (`+N`) instead of silent loss.
- Shared store and polling between widget and detail windows; no duplicate poller.
- IP masking and client-name hiding; WAN ASN hidden by default.
- Light/dark/auto theme.

## Data semantics

- Missing values remain missing (`—` / “not available”); never converted to zero.
- Availability is not used as packet loss.
- Downtime count is not used as failover count.
- Browser-side sampling is not used as calendar traffic.
- Calendar traffic uses the controller's daily/monthly boundary and is scoped to
  WAN traffic, not LAN-local traffic.

## Security boundary

- GET-only against the user-configured controller.
- No telemetry, analytics, developer upload, hidden remote calls or extra service.
- API key is stored in Sun-Panel user-scoped data nodes and injected by the host;
  it is never bundled in the app.
- No reboot, WAN switch, active speedtest, firmware update, PoE control or other
  write operation.

## Known limitations

- VPN online count: not available from the tested REST endpoint; no count shown.
- SFP+ DDM: controller/port firmware did not expose optical diagnostics; only
  module presence is shown.
- AP temperature: not provided by the tested APs.
- The controller aggregated-dashboard endpoint is an internal console contract;
  missing fields degrade gracefully.
