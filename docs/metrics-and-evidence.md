# Metrics and evidence

## Repository inventory — November 27, 2026

Read-only GitHub tree inspection of the protocol's default branch and the canonical handoff repository's default branch returned complete (non-truncated) trees.

| Metric | Count | Definition |
| --- | ---: | --- |
| Archived execution Markdown files | 548 | Paths matching history/executions/*.md at any scope depth |
| Chain manifest files | 44 | Paths ending in execution-chain.toml |
| Python package modules | 39 | Python files directly inside the package |
| Test modules | 49 | tests/test_*.py files |

These are file counts, not unique successful executions, authorized chains, passing tests or current deployments. Duplicate historical records or draft manifests are not excluded by these filters. Other branches and local-only artifacts are outside the snapshot.

## Historical operational baseline — October 7, 2026

The original protocol documentation records a post-fast-path metrics baseline:

| Metric | Value |
| --- | ---: |
| Discovered handoffs | 15 |
| Total execution records | 247 |
| Completed | 231 |
| Cancelled | 7 |
| Blocked | 2 |
| Other or non-terminal | 7 |

The baseline includes personal and work scopes and is presented only in aggregate. It is a different measurement from the November tree inventory and should not be used to compute a growth or completion rate between the two dates.

## Observability and limitations

The reporting documentation dated October 30 records 25 discovered handoffs and 410 archived files; only one archive carried an explicit completion timestamp. It also reports zero measured token usage records in that snapshot. No verified reduction in cost, token consumption or delivery time is claimed.

Selected historical test results are reported separately in [case studies](real-world-case-studies.md). They belong to individual executions and were not independently rerun.

## Evidence provenance

Protocol README, packaging metadata, orchestration and runtime contracts, QA and security documentation, chain and commit-gate source, metrics baseline and reporting documentation, and selected archived personal-project executions. Raw private records and employer details are excluded.
