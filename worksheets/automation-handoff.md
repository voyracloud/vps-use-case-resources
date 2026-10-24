# Automation handoff worksheet

Define what a recurring task should do, what it must not do, and who handles exceptions before selecting an automation tool. This is a planning worksheet, not an executable workflow or a claim of savings.

## 1. Capture the current process

| Question | Your answer |
|---|---|
| Which business outcome is required? | |
| What starts the task, and how often? | |
| Which authorized sources provide the inputs? | |
| What is the intended output and destination? | |
| Which fields are sensitive or unnecessary? | |
| Who currently checks correctness? | |
| Which repeated steps cause errors or delays? | |
| Is improving the manual process sufficient? | |

## 2. Describe the handoffs

| Step | Input and owner | Rule / output | Exception | Human responsible |
|---|---|---|---|---|
| Collect | | | | |
| Validate | | | | |
| Match or deduplicate | | | | |
| Prepare result | | | | |
| Review and approve | | | | |
| Send or save | | | | |

Define what constitutes a duplicate for this task; do not delete records simply because names match. Distinguish preparing a message from authorization to send it.

## 3. Plan a small pilot

- Use authorized test data or clearly labeled synthetic records.
- Specify the expected output for an ordinary case, missing input, conflicting input, and repeated delivery.
- Identify actions that could contact someone, change a business record, or create a charge; keep them out of the first dry run unless separately approved.
- Decide how to pause the process and resume the manual workflow.
- Name the reviewer and acceptance criteria before running the pilot.
- Record observed outcomes and unresolved errors. Do not replace measurements with estimated savings.

| Case | Expected result | Observed result | Review / next action |
|---|---|---|---|
| Ordinary input | | | |
| Required field missing | | | |
| Conflicting data | | | |
| Same input arrives again | | | |
| Destination unavailable | | | |

## 4. Choose an operating model

Record who owns access, credentials, workflow changes, execution failures, backups, and recovery. Compare a managed tool with self-hosting only after these requirements are clear. Product billing units are not interchangeable; calculate each candidate against the same documented workflow.

**Fictional example:** a team collects inquiry forms and assigns leads. The pilot creates a review list from synthetic entries; a human approves assignments. It does not email prospects or write to the production CRM. A separate weekly-report workflow would also need reporting definitions, missing-data rules, and approval of any AI-generated summary.

Reviewed: 2026-10-24. No workflow was run for this worksheet.
