# Remote access and recovery review

Separate the machine hosting your work, the network path reaching it, and the protocol controlling its desktop. RDP provides remote interaction; a VPN supplies a network connection. They can be used together, but neither label alone proves safe access or recoverability.

## Record before changing access

| Area | Requirement / evidence / owner |
|---|---|
| Windows version, application and .NET runtime requirements | |
| Named users, administrator rights and applicable licenses | |
| Approved entry path and allowed sources | |
| Authentication controls at each supported access layer | |
| Updates, logs, account removal and review date | |
| Backup scope, restore evidence and recovery owner | |
| Independent console/recovery route and access credentials location | |
| Change window, rollback trigger and person available | |

- [ ] Confirm recovery access before tightening the current connection.
- [ ] Record which account performs daily work and which administers the server.
- [ ] Verify the application starts as intended after a controlled restart.
- [ ] Recheck access and log evidence after an approved change.

Do not disable firewall controls or accept an unexpected certificate merely to restore access; verify the endpoint through the approved recovery path.

## Fictional example — not a product test

A team plans a Windows-hosted .NET service. It records RDP for administration, a separate service identity, and a runtime version to verify. Before changing allowed sources, the operator confirms an independent recovery route. The application and restore process remain “not tested”; this example claims no deployed service or successful security audit.

## Limits and sources

Reviewed 2026-11-06: [VoyraCloud Windows documentation](https://docs.voyracloud.com/docs/servers/windows-vps). Windows application proxy settings are separate from remote desktop access; VoyraCloud's Linux instance proxy configuration does not apply to Windows. Do not assume multi-user licensing, software compatibility, a VPN service, or multifactor controls are bundled. This checklist supports review, not a security certification. Use the [hosting worksheet](../worksheets/hosting-decision.md) for ongoing responsibility.
