# IP location investigation worksheet

Use this when a service displays an unexpected country or city. Separate device location, observed public exit, database estimates, and application behavior. An address label is not GPS evidence or proof of where a person lives.

## Capture the discrepancy

| Field | Your evidence |
|---|---|
| UTC time, client and active network/proxy | |
| Requested location, if any; order/reference kept private | |
| Observed exit IPv4/IPv6; lookup method | |
| Database A name, date/version, country/city, uncertainty | |
| Database B name, date/version, country/city, uncertainty | |
| Application result, language/account/cookie influences | |
| Same exit confirmed across comparisons? | |
| Correction destination, evidence sent, ticket and follow-up | |

Repeat comparisons using the same exit and timeframe. If a rotating exit changes between requests, mark the comparison as inconclusive. Avoid sending account credentials, browsing history, or unrelated personal information with a correction request.

## Fictional example — not a product test

A tester labels an exit “A.” Database One reports City North; Database Two reports only the expected country. A storefront shows a different language. The record separates the database disagreement from the storefront preference and asks which source the storefront uses. It does not declare the purchased location wrong solely from the language setting.

## Limits and sources

Reviewed 2026-11-06: [MaxMind's explanation of discrepancies](https://www.maxmind.com/en/geoip/understanding-ip-geolocation-discrepancies) and [correction process](https://www.maxmind.com/en/geoip-data-correction-request). Corrections may not propagate immediately or change another service's decision. ASN registration, geolocation, connectivity and destination acceptance are different observations. A lookup is not a complete proxy test; use the [egress checklist](../checklists/egress-path-validation.md) when routing is uncertain.
