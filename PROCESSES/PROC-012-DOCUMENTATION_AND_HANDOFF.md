# Process: Documentation and Handoff

## Purpose

This process defines how the agent packages completed work for the user to own and operate independently. The work is not done when the code runs. It is done when the user can maintain it without the agent.

In construction, this is closeout: the contractor delivers as-built drawings, operation manuals, warranties, and maintenance guidance. The building is handed over in a state the owner can maintain.

---

## When This Process Applies

- Substantial completion (PROC-011) is confirmed and punch list is resolved
- Work is being handed off to the user
- Work is being handed off to a different agent (GC-01.4)
- Work is being terminated before completion (GC-07.1)

## When This Process Does Not Apply

- Intermediate delivery of a component that will continue to be developed (PROC-006)
- Substantial completion notification (PROC-011) — closeout follows substantial completion, it doesn't replace it

---

## Phase 1: Compile the Deliverable Package

**Actor: Agent**

Per GC-05 Section 5.5.2 and GC-12 Section 12.1.2:

**Required content:**

1. **The complete deliverable** in its final state — all code, configuration, and assets
2. **Documentation** as required by Division 01 (01-7000):
   - Setup and usage instructions
   - Architecture overview
   - API documentation (if applicable)
   - Configuration reference
   - Deployment guide
3. **A summary of all scope changes** from the original specification — what was changed, when, and why. This is the as-built record
4. **A list of all accepted deviations** — where the deliverable does not conform to the specification and was accepted by the user
5. **Maintenance and operational notes:**
   - Known limitations and edge cases
   - Technical debt identified during execution (GC-09.5) and recommended remediation
   - Dependencies that will need updating and approximate cadence
   - Monitoring recommendations (GC-11.3)
   - Scaling considerations if applicable

**Rules:**

1. Documentation must be written for the person who will maintain this, not the person who built it. Assume the reader does not have the conversation history
2. All dependencies must be declared and pinned to versions
3. All environment requirements must be documented
4. All credentials and access requirements must be documented (the requirements, not the credentials themselves)
5. If configuration is required, it must be externalized and documented, not buried in code

**Failure mode:** Agent delivers working code with no documentation. User cannot deploy, configure, maintain, or troubleshoot it without re-engaging the agent.

---

## Phase 2: Verify Handoff Readiness

**Actor: Agent**

Per GC-12 Section 12.1.1, certify readiness when:

1. Substantial completion has been confirmed (PROC-011)
2. All tests pass acceptance criteria
3. All required documentation has been provided
4. No critical or high-severity deficiencies remain open
5. The user can operate the deliverable independently

**The independence test:** Could the user (or a different agent, or a competent developer) take this package and operate, modify, and maintain the deliverable without any information that exists only in conversation history? If no, the handoff package is incomplete.

---

## Phase 3: User Review

**Actor: User**

Per GC-12 Section 12.1.3, the user reviews the package and either:

1. **Accepts** — the deliverable is accepted. The warranty period begins
2. **Identifies gaps** — specific conditions not met, with reference to the specification or Division 01 closeout requirements. The agent addresses the gaps and resubmits

---

## Phase 4: Warranty

Per GC-12 Section 12.3:

1. For a defined period after final delivery (specified in Division 01, or 30 days if not specified), the agent corrects defects without additional resource cost
2. **Warranty covers:** defects that existed at delivery but were not discovered during review; functionality that does not perform as specified under normal conditions
3. **Warranty does not cover:** accepted deviations; damage from user modifications; failure from conditions outside the specification; new requirements (these are new scope)
4. The distinction between a defect (warranty) and a new requirement (new scope) is determined by the specification. If the specification required it and it doesn't work, it's a defect. If the specification didn't require it, it's new scope

---

## Phase 5: Acceptance Finality

Per GC-13 Section 13.2:

After final delivery and warranty expiration:

1. The scope for revisiting completed work is limited
2. Work required after this point is new scope governed by a new specification
3. This exists to prevent endless rework cycles. Both parties accept the delivered state as project conclusion

**Exceptions:** Fraud, defects that could not reasonably have been discovered during warranty, and governing constraint violations.

---

## Handoff to Another Agent

Per GC-01 Section 1.4, when work transfers to a different agent:

1. **Summary of work completed** — what was built, its current state, what works
2. **Summary of work remaining** — what is not yet done, including punch list and backlog items
3. **All active specifications and context** — the receiving agent gets the full specification package, not a conversation summary
4. **Open clarification requests** and their status
5. **Known issues and risks** — what the receiving agent needs to watch for
6. **The project's decision history** — key decisions made during execution and their rationale, so the receiving agent doesn't re-litigate settled questions

**Rules:**

1. The receiving agent reviews the handoff and confirms understanding before proceeding (GC-01.4.3)
2. The user is responsible for ensuring the receiving agent has access to all specification documents (GC-01.4.4)

---

## Terminated Work

Per GC-07 Section 7.1, when work is terminated before completion:

1. Stop work immediately
2. Preserve all work in a usable state
3. Provide the handoff package with honest status: what works, what doesn't, what was in progress, what wasn't started
4. The goal is to leave the work in the most usable state possible, even if termination is abrupt

This is not a failure state requiring a lesser standard of documentation. Terminated work gets the same handoff quality as completed work — the user needs it more, not less.
