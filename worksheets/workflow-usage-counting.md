# Workflow usage and cost worksheet

Compare the same business result before comparing plans. Keep business events, workflow executions, module operations, credits, API tokens and infrastructure costs in separate columns. None is a universal unit of work.

## Describe one representative workflow

| Input or cost driver | Assumption | Measurement / current rule and date |
|---|---|---|
| Incoming events and completed business outcomes | | |
| Branches, records per event and loop iterations | | |
| Retries, failed runs and replay policy | | |
| n8n edition/deployment and applicable execution rules | | |
| Make modules and applicable credit rules | | |
| External API/token charges, separate from platform billing | | |
| Hosting, storage, backups and network transfer | | |
| License, upgrades, recovery and operator responsibility | | |
| Currency, billing period, included quota and overage | | |

Estimate each platform independently using its current rules, then document a small measured pilot if authorized. Record failed and partially successful work; do not count a repeated write as a second useful outcome. Optional proxies belong only in workflows that need them.

## Fictional example — not a product test

Ten incoming leads each need validation and one CRM write; two require review. The team lists ten inputs and eight intended successful writes. It leaves billable n8n executions and Make credits unresolved until deployment and module behavior are checked. “Ten leads” is not automatically “ten credits” or a product benchmark. Self-hosting also needs a backup and upgrade owner.

## Limits and sources

Reviewed 2026-11-06: [Make credit rules](https://help.make.com/credits), [n8n hosting responsibilities](https://docs.n8n.io/hosting/). AI modules can have additional usage dimensions; self-hosted editions have their own license and infrastructure conditions. This worksheet contains no live quote, fixed unit conversion, or claim that either platform is cheaper. Pair it with the [automation handoff worksheet](automation-handoff.md).
