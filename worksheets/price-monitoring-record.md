# Price monitoring record

Use one row per comparable product offer. Start with product matching and authorized data access; choosing a server or proxy comes later, only if the task requires it. A public API, licensed feed, managed service, or manual review may be sufficient.

## Define and record a comparison

| Field | Your record |
|---|---|
| Source URL/feed and permitted access method | |
| Product identifier, variant, size, quantity, condition | |
| Seller, region, currency and observation timestamp | |
| Displayed amount, tax basis, shipping, discounts | |
| Stock status and delivery conditions | |
| Previous comparable observation and evidence | |
| Difference requiring human review | |
| Reviewer, action and confidence / unresolved issue | |

Define a collection interval and stop conditions. Keep the original observation distinct from a normalized comparison. Do not mix tax-inclusive and tax-exclusive offers or treat a missing value as zero. Use a second check before changing your own prices.

## Fictional example — not a product test

A shop compares two advertised offers for a 500 ml item. One includes delivery and the other excludes it. The reviewer marks the pair “not yet comparable” and asks for delivery terms. No automatic repricing follows. These invented observations demonstrate a matching error, not measured savings or a collection result.

## Limits and sources

Reviewed 2026-11-06: [Prisync's description of competitor price monitoring](https://prisync.com/competitor-price-tracking/) identifies product, channel and stock context; this template is an independent record format, not an endorsement. Respect access terms and avoid collecting unnecessary personal data. Failed access is not permission to evade restrictions. Use the [automation handoff worksheet](automation-handoff.md) to assign exception handling; a changed IP does not correct a mismatched SKU.
