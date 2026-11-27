# Agent orchestration

The documented operating model uses ChatGPT as external orchestrator, a human as the authority owner, and OpenCode as local execution agent. The runtime contract also addresses other execution clients, including Codex; equivalent practical compatibility has not been established.

| Actor | Responsibility |
| --- | --- |
| Orchestrator | Prepare complete execution or chain drafts and publish scoped handoff artifacts |
| Human | Approve exact chain digests, QA verdicts and additional side effects |
| Executor | Validate freshness, claim, implement, test, record evidence and close through native commands |

## Execution loop

```mermaid
sequenceDiagram
 participant O as Orchestrator
 participant H as Human
 participant S as Canonical Git state
 participant E as Executor
 O->>S: Publish validated draft bundle
 H->>S: Authorize exact chain digest
 E->>S: Refresh, validate and claim stage
 E->>E: Implement and test bounded work
 E->>S: Record evidence and check commit gate
 alt Required human decision
 E-->>H: Request decision
 H->>S: Record explicit feedback
 end
 E->>S: Close and archive stage
 E->>S: Advance if authorized
```

The CLI exposes bounded automatic next/resume/chain operations and optional dispatch, workstation bridge, review gateway and remote ingress. These are controlled mechanisms over canonical state, not a claim of unattended end-to-end reliability.

The orchestrator does not commit product code or generate its own human authorization. Remote work uses a repository-target abstraction rather than treating SSH destinations as local paths.
