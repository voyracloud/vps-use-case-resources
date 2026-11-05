# Browser tool selection and extraction validation

Use two separate decisions: how to operate a browser, and how to verify the fields obtained from an authorized page. A working browser session does not establish extraction accuracy; accurate fields do not prove a tool is maintainable.

## A. Select the execution approach

| Requirement | Code framework | Low-code tool | Managed execution |
|---|---|---|---|
| Required browser, OS and interactions | | | |
| Scheduling, secrets and permitted access | | | |
| Debugging, evidence retention and handoff | | | |
| Upgrade/recovery owner and portability | | | |
| Unverified compatibility or trial result | | | |

## B. Validate the extracted fields

| Page/version reference | Field and expected type | Source evidence | Returned value | Pass / discrepancy / human decision |
|---|---|---|---|---|
| | | | | |

Define required fields, missing-value handling, units and acceptance criteria before comparing rule-based extraction, model extraction, or a hybrid. Preserve source evidence and failures; do not let plausible text substitute for a value absent from the page.

## Fictional example — not a product test

A team chooses a code framework because an operator can maintain it. In a separate invented extraction exercise, the model returns “available” although the sample page says “notify me.” The field fails review despite the browser loading correctly. The team records an explicit missing/unknown rule rather than changing the network exit.

## Limits and sources

Reviewed 2026-11-06: [Zyte structured extraction documentation](https://docs.zyte.com/zyte-api/usage/extract/index.html). The tables are a review format, not a ranking or benchmark. Record model, prompt, schema and tool versions with any real experiment. No tool is asserted compatible with a particular hosting product. Use the [automation handoff worksheet](automation-handoff.md) for human intervention and the [client compatibility worksheet](proxy-client-compatibility.md) only when an authorized task needs a proxy.
