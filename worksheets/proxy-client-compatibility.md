# Proxy client compatibility worksheet

Check the exact client and authentication mechanism before changing settings. A protocol name alone does not establish compatibility. Keep credentials out of screenshots, copied URLs, and shared logs.

## Record one connection path

| Check | Requirement / observed evidence |
|---|---|
| Client, OS, version and controlling policy | |
| Target URL scheme; proxy connection scheme | |
| Proxy protocol and authentication method | |
| Configuration source: app, OS, policy, extension | |
| Hostname resolved locally or at proxy; evidence | |
| TCP/UDP requirement and actual client support | |
| Bypass rules and other enabled proxy/VPN layers | |
| Sanitized error, responding layer, timestamp | |
| Restore method and owner | |

## Interpret the layers

An HTTPS destination and an HTTPS connection to a proxy are different properties. Check both. HTTP 407 is a proxy authentication response; SOCKS authentication failures are not inherently HTTP 407. Establish the protocol and responding layer before changing credentials.

Chrome's native SOCKS5 implementation does not support authentication or UDP, and resolves target names through the proxy. Do not assume all SOCKS clients behave identically. Chrome also ignores credentials embedded in manual proxy settings; an extension is not automatic proof of a working authentication bridge.

## Fictional example — not a product test

A team records “Chrome native SOCKS5 + username/password endpoint.” Documentation reveals a compatibility mismatch before any request is attempted. The outcome is “select and validate a compatible client,” not “credentials rejected” or “provider unavailable.” No working browser configuration is claimed.

## Limits and sources

Reviewed 2026-11-06: [Chromium proxy behavior](https://chromium.googlesource.com/chromium/src/+/HEAD/net/docs/proxy.md), [HTTP 407](https://developer.mozilla.org/en-US/docs/Web/HTTP/Reference/Status/407). VoyraCloud's [rotating service](https://docs.voyracloud.com/docs/proxies/rotating-residential) documents HTTP/SOCKS5; [static ISP](https://docs.voyracloud.com/docs/proxies/static-isp) and [datacenter](https://docs.voyracloud.com/docs/proxies/datacenter) document SOCKS5 credentials. These are documentation boundaries, not tested client combinations. Use the [egress checklist](../checklists/egress-path-validation.md) for subsequent observations.
