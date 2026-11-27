# Engineering challenges

## 1. Context loss between agents
Conversation history is not a reliable execution ledger. AHP separates the current stage, explicit next action and archived evidence in a Git-backed handoff repository. This enables resumable work without requiring the entire conversation. The trade-off is synchronization and schema maintenance.

## 2. Authorization drift
A multi-stage plan can change after approval. Complete bundle validation and digest-bound human authorization tie permission to the exact ordered plan. File allowlists and separate side-effect approvals narrow the execution boundary.

## 3. Concurrent state updates and repository drift
Multiple clients can touch shared handoff state. Scoped freshness, publication and opt-in workspace locks are designed to preserve unrelated work and block same-scope conflicts. Expected HEAD checks and explicit acceptance handle revision drift. These mechanisms do not establish distributed exactly-once execution.

## 4. Workflow overhead
Uniform review and commit-only stages can add unnecessary handoffs. Risk-adaptive QA, same-execution corrective updates and an explicit personal-fast profile reuse existing gates without removing critical reviews.

## 5. Measurement without false precision
Daily and weekly reports derive from canonical artifacts and Git history instead of a second database. They distinguish measured, estimated and unavailable evidence. Missing timestamps and sparse provider records limit cycle-time and cost analysis.

## 6. Operational continuity
The owner has reported friction around publishing acceptance state and resuming automatic chains when an executor is unavailable. These are lessons for a future redesign, not resolved guarantees. A stronger architecture would make state transitions transactional or recoverable and distinguish capability detection from successful execution.
