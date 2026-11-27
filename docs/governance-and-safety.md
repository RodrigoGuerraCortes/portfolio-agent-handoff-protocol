# Governance and safety

AHP implements engineering workflow controls, not a certification of enterprise AI governance.

## Authorization boundaries

- Human authorization is bound to the exact chain digest.
- Commit gates check target branch, allowed files, readiness and recorded validation requirements.
- Commit, push and deployment are distinct permissions; linear chain v1 does not grant push/deploy authority.
- Same-scope conflicts and unexpected target changes require explicit resolution.
- Scoped Git transport aims to preserve unrelated work and avoids destructive rewrites.

## Risk-adaptive QA

| Level | Intended scope |
| --- | --- |
| Q0 | Documentation, research and decisions |
| Q1 | Focused isolated code changes |
| Q2 | Cross-module, database, API and contract changes |
| Q3 | Critical changes, independent review and applicable human gates |

The default work-strict profile preserves separate approvals. The opt-in personal-fast profile composes compatible existing operations for authorized lower-risk work. It is not a general reduction of critical QA.

The runtime supports recording development methods such as TDD and skill evidence. Some declarations are optional or warnings-only; their existence is not proof of actual tool invocation or historical RED evidence.

## Security scope

The protocol prohibits credentials, personal data and proprietary source files in handoffs. Text scanning is heuristic and warning-based, not comprehensive data loss prevention. Human review remains necessary. Workflow gates constrain supported CLI operations; they do not sandbox arbitrary external agent actions.
