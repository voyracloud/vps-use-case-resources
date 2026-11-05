# Egress path validation checklist

Use an authorized destination to observe one configuration change at a time. An IP lookup describes the request reaching that lookup service; it does not prove every application follows the same route.

## Before changing anything

- [ ] Record OS, client versions, current routes, proxy/VPN layers and bypass rules.
- [ ] Confirm an independent management/recovery path and the person responsible.
- [ ] Define the expected path separately from the observed result.
- [ ] Use a controlled target; do not publish credentials or identifying network records.

| Traffic case | Expected path | Baseline | Changed configuration | Restored configuration / evidence |
|---|---|---|---|---|
| Application IPv4 TCP | | | | |
| Application IPv6 | | | | |
| DNS resolution | | | | |
| UDP, if required | | | | |
| SSH / management | | | | |
| Private-network access | | | | |
| Reply to incoming connection | | | | |
| Container or background process | | | | |

Name the tested process and target in each result. Write “not tested” when evidence is absent. A failed request can be DNS, authentication, routing, or destination behavior; preserve the error before drawing a conclusion.

## Fictional example — not a product test

A team sketches `application → outbound proxy → approved endpoint` and `visitor → reverse proxy → web application`. It realizes the second path is an incoming website service, not an alternative exit. Its first planned test covers one IPv4 client; IPv6 and containers remain untested. No measured route is supplied by this example.

## Limits and sources

Reviewed 2026-11-06: [Cloud VPS documentation](https://docs.voyracloud.com/docs/servers/cloud-vps). VoyraCloud's instance configuration has supported Linux prerequisites and IPv4 scope; SSH, private traffic and incoming replies retain their original paths, IPv6 is excluded, and HTTP proxies cover TCP. Recovery on failure is attempted, not guaranteed. Windows does not support this platform configuration. Those documented expectations still require environment-specific verification.
