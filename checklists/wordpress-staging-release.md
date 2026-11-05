# WordPress staging and release checklist

Use this with your actual host's documented staging, backup and restore procedures. Define what moves to production and what must remain there. A staging copy is not automatically isolated, and restoring a database can overwrite newer production work.

## Prepare and rehearse

Keep the copied web runtime and scheduled jobs stopped until access restrictions and external-side-effect isolation are in place; only then start staging checks.

- [ ] Assign a release owner, change window and rollback decision maker.
- [ ] Record the files/database being copied and remove unnecessary personal data.
- [ ] Restrict staging access; do not rely on a search-index setting as access control.
- [ ] Disable or sandbox payments, outgoing email, scheduled jobs and external webhooks.
- [ ] Record production backup location and evidence of a restore rehearsal.

| Check | Expected result | Evidence / owner | Go / stop |
|---|---|---|---|
| Login, forms and critical content | | | |
| Theme/plugin/runtime compatibility | | | |
| External integrations in test mode | | | |
| Production data changed since copy | | | |
| File/config/database deployment scope | | | |
| Rollback trigger and data reconciliation | | | |
| Post-release checks and staging cleanup | | | |

## Fictional example — not a product test

A shop tests a theme change on a protected copy. Production receives new orders during review. The team plans a file-only release and stops a proposed full database overwrite until order preservation is resolved. This invented decision is not proof that any host supports selective deployment or that a restore has succeeded.

## Limits and sources

Reviewed 2026-11-06: [WordPress backup guidance](https://developer.wordpress.org/advanced-administration/security/backup/). Preserve both necessary files and data, and validate your deployment-specific recovery method. This template does not provide a universal migration command or claim staging is included with a server image. After an actual release, use the [monitoring response worksheet](../worksheets/monitoring-response.md) to record detection, notification and recovery responsibility.
