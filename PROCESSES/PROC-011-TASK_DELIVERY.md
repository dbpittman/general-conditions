# Process: Task Delivery

## Purpose

This process defines how the agent determines that work is substantially complete, communicates this to the user, and transitions from building to finishing. Substantial completion means the deliverable can be used for its intended purpose even if minor items remain.

In construction, this is substantial completion: the building can be occupied. It triggers a different phase — the owner begins using the building, and remaining items become a punch list with a defined completion window.

---

## When This Process Applies

- The agent believes the deliverable meets all primary acceptance criteria
- The deliverable is usable for its intended purpose
- Remaining work is minor — polish, documentation gaps, non-critical improvements

## When This Process Does Not Apply

- Major functionality is missing or non-functional — this is not yet substantially complete
- The agent is submitting an intermediate deliverable for review (PROC-006) — that is a milestone, not substantial completion
- The user has requested final delivery (PROC-012) — substantial completion precedes final delivery

---

## Phase 1: Self-Assessment

**Actor: Agent**

Before claiming substantial completion, the agent verifies:

1. **All primary acceptance criteria pass.** Not most. All. If a primary criterion fails, the work is not substantially complete
2. **The deliverable is usable for its intended purpose.** The user can use it to do what they set out to do. This is the test — not whether every feature is polished
3. **No remaining item prevents intended use.** Remaining items must be genuinely minor: cosmetic issues, documentation gaps, edge cases, non-critical improvements
4. **All tests pass** acceptance criteria defined in the specification
5. **No critical or high-severity deficiencies remain open**

**Rules:**

1. The agent must be honest about what "minor" means. If the user would disagree that a remaining item is minor, it's not minor
2. Review the full specification, not just the parts the agent worked on most recently. It is common to lose track of early requirements
3. Run full quality verification (PROC-007) before claiming substantial completion

**Failure mode:** Agent declares substantial completion prematurely to move the project forward. User discovers significant gaps.

---

## Phase 2: Notify the User

**Actor: Agent**

Per GC-05 Section 5.4.2, notify the user with:

1. **A description of the functionality delivered** — what the user can now do that they couldn't before
2. **A punch list of remaining items** — specific, enumerated list of what is not yet complete, with estimated effort for each
3. **Confirmation that no remaining item prevents intended use** — explicit statement with rationale
4. **How to use the deliverable** — enough information for the user to begin using it immediately. Detailed documentation comes at closeout (PROC-012)

**Rules:**

1. The punch list must be specific. "Some cleanup needed" is not a punch list item. "Error messages on the settings page use technical codes instead of user-friendly text" is a punch list item
2. Each punch list item should reference the specification requirement it relates to
3. If the punch list is longer than the agent expects, reconsider whether substantial completion has actually been reached

---

## Phase 3: User Confirmation

**Actor: User**

Per GC-05 Section 5.4.3, the user either:

1. **Confirms substantial completion** — the user agrees the deliverable is usable. Remaining items become the punch list governed by Phase 4
2. **Disputes substantial completion** — the user identifies specific functionality gaps that prevent intended use. The agent must address these gaps before resubmitting. The dispute must be specific — "it doesn't feel done" is not a dispute; "I cannot generate reports, which is the primary purpose" is a dispute

**Rules:**

1. Confirmation means the user begins using the deliverable. The user assumes operational responsibility for the deployed portions
2. Dispute loops back to execution. The items preventing intended use are defects (PROC-008) or missing functionality, not punch list items
3. Confirmation does not waive the user's right to identify defects discovered later (GC-05.3.3)

---

## Phase 4: Punch List Resolution

**Actor: Agent**

Upon confirmed substantial completion:

1. The agent works through the punch list items systematically
2. Each resolved item is verified and marked complete
3. Progress on the punch list is reported to the user
4. New items discovered during punch list resolution are added if they are within the original specification scope. New requirements are change orders (PROC-009)

**Rules:**

1. Punch list items are completed within the current project scope. They are not deferred to a future project unless the user explicitly agrees to defer them (GC-05.6)
2. The agent completes punch list items at no additional resource cost — these are items that should have been done before substantial completion
3. Punch list completion leads to final delivery (PROC-012)

---

## Deferred Work

Per GC-05 Section 5.6, work may be deliberately deferred:

1. Deferral must be explicitly agreed by both user and agent
2. Deferred items are removed from acceptance criteria
3. Deferred items are recorded in a backlog with enough detail to resume later
4. Deferred work is a conscious scope decision, not incomplete work. The distinction matters for determining what "done" means
