# Session and fixed-IP observation worksheet

Use this to distinguish a requested session policy from the address actually observed. Define the observation window and allowed changes before collecting samples. Only test destinations you are authorized to access.

## Session definition

| Field | Your record |
|---|---|
| Provider, product, documented mode and source date | |
| Session identifier alias; connection reuse behavior | |
| Requested interval and observation duration | |
| Allocated IP term / renewal date, if applicable | |
| Client version, target and sampling interval | |
| Expected change; stop condition; owner | |

| UTC timestamp | Request / connection alias | Session alias | Exit alias | Result / error | Reconnect or configuration change |
|---|---|---|---|---|---|
| | | | | | |

Keep raw IPs in a private record when needed; use consistent aliases in shared material. Record failed observations as well as successful ones. Do not silently replace a changed address with a new session and call the sequence stable.

## Fictional example — not a product test

Session S1 produces exit alias A at two imagined checkpoints, then B after a reconnect. The analyst records “address changed after reconnect in this hypothetical sequence.” The conclusion is neither “sticky always fails” nor “a fixed duration was guaranteed.” A separate fixed-IP subscription record would track allocation and renewal, not reuse this session assumption.

## Limits and sources

Reviewed 2026-11-06: [rotation modes](https://docs.voyracloud.com/docs/proxies/rotating-residential) describe a new IP per new connection and best-effort sticky behavior. [Static ISP terms](https://docs.voyracloud.com/docs/proxies/static-isp) describe a fixed allocation during its term, retained on renewal and released at expiry. Neither a short observation nor a session label establishes long-term availability, platform acceptance, or account safety.
