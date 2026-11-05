# VPS Use Case Resources

Vendor-neutral worksheets and checklists for choosing servers and proxies, checking outbound paths, and recording operational responsibilities.

Copy a Markdown file, fill in your requirements, and keep the evidence behind your decision. These are editable review tools, not deployment scripts. Worked examples are fictional and do not represent tested products or customer results.

## Choose by task

| Your task | Resource |
|---|---|
| Decide whether you need a server, a proxy, or neither | [Server or proxy selection](worksheets/server-or-proxy-selection.md) |
| Compare hosting requirements and maintenance responsibility | [Hosting decision](worksheets/hosting-decision.md) |
| Check client protocols, authentication and DNS behavior | [Proxy client compatibility](worksheets/proxy-client-compatibility.md) |
| Record which traffic changes after a proxy configuration | [Egress path validation](checklists/egress-path-validation.md) |
| Observe session changes or a fixed-IP allocation | [Session and IP observation](worksheets/session-ip-observation.md) |
| Investigate conflicting IP location results | [IP location investigation](worksheets/ip-location-investigation.md) |
| Match comparable offers before acting on price changes | [Price monitoring record](worksheets/price-monitoring-record.md) |
| Compare workflow usage units and operating costs | [Workflow usage and cost](worksheets/workflow-usage-counting.md) |
| Define inputs, exceptions and human intervention | [Automation handoff](worksheets/automation-handoff.md) |
| Record authorized regional ad and landing-page observations | [Ad observation](worksheets/ad-verification-observation.md) |
| Select browser tools and separately validate extracted fields | [Browser and extraction validation](worksheets/browser-extraction-validation.md) |
| Review remote desktop access, application needs and recovery | [Remote access review](checklists/remote-access-review.md) |
| Prepare a WordPress staging release and rollback decision | [WordPress staging release](checklists/wordpress-staging-release.md) |
| Assign monitoring, notification and recovery responsibility | [Monitoring response](worksheets/monitoring-response.md) |

## Use a resource

1. Describe one task and select the relevant table. A managed service or no infrastructure change may be the right outcome.
2. Record requirements, current documentation, versions, dates and unresolved questions. Keep expected behavior separate from observations.
3. Assign an owner and validate changes in an authorized environment with a recovery route. Remove credentials and identifying customer details before sharing records.

A completed table is a decision or observation record, not proof of security, availability, compliance, or destination acceptance. Compatibility and service terms can change; confirm them for your actual client and provider. See [changes](CHANGELOG.md) for repository updates.

## Maintainer

Maintained by [VoyraCloud](https://www.voyracloud.com/). The resources are intended to work across providers and tools; no purchase is required. Report a documentation issue with the relevant file, version and sanitized evidence. Do not post credentials or private customer data.

## License

Repository materials are available under the [MIT License](LICENSE). Linked articles and third-party materials retain their own terms; this license does not relicense them.

## 中文摘要

面向主机与代理选型、出口检查、自动化和运维责任的中立表格与清单，可按 MIT 许可复制修改。案例均为虚构示例，不代表产品实测；使用前请核对实际环境、版本与服务条款。
