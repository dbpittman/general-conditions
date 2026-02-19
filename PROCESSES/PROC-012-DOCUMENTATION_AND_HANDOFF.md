# Process: Documentation and Handoff

## Purpose

This process defines how the agent packages completed work for the user to own and operate independently. The work is not done when the code runs. It is done when the user can maintain it without the agent.

In construction, this is closeout: the contractor delivers as-built drawings, operation manuals, warranties, and maintenance guidance. The building is handed over in a state the owner can maintain.

**Deliverable:** 01-7000 Closeout (completed — all documentation delivered, maintenance notes, warranty terms, acceptance record)

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

## Phase 1: Complete Documentation

**Actor: Agent**

Complete all documentation required by 01-7000:

1. README with setup and usage instructions
2. Architecture overview / system design document
3. API documentation (if applicable)
4. Database schema documentation (if applicable)
5. Deployment guide
6. Configuration reference
7. Troubleshooting guide
8. User guide / operational manual
9. Change log — compiled from PROC-009 change records

Check off each item in the 01-7000 Required Documentation section.

**Rules:**

1. Documentation must be written for the person who will maintain this, not the person who built it. Assume the reader does not have the conversation history
2. All dependencies must be declared and pinned to versions (per 01-6000)
3. All environment requirements must be documented
4. All credential requirements must be documented (the requirements, not the credentials themselves)

**Failure mode:** Agent delivers working code with no documentation. User cannot deploy, configure, maintain, or troubleshoot it without re-engaging the agent.

---

## Phase 2: Complete Maintenance Notes

**Actor: Agent**

Complete the maintenance notes section of 01-7000:

1. **Known limitations and edge cases** — what the user should be aware of
2. **Technical debt** — identified per GC-09.5 during execution. What workarounds exist, what remediation is recommended, and what priority
3. **Dependencies requiring updates** — which dependencies will need updating, approximate cadence, and any known upcoming breaking changes
4. **Monitoring recommendations** — per GC-11.3, what should be monitored and what alerts should exist
5. **Scaling considerations** — if applicable, what will need to change as usage grows

---

## Phase 3: Verify Handoff Readiness

**Actor: Agent**

Per GC-12 Section 12.1.1, certify readiness when:

1. Substantial completion has been confirmed (PROC-011)
2. All tests pass per 01-4000
3. All required documentation per 01-7000 has been provided
4. No critical or high-severity deficiencies remain open
5. The user can operate the deliverable independently

**The independence test:** Could the user (or a different agent, or a competent developer) take this package and operate, modify, and maintain the deliverable without any information that exists only in conversation history? If no, the handoff package is incomplete.

---

## Phase 4: User Review

**Actor: User**

Per GC-12 Section 12.1.3, the user reviews the completed 01-7000 package and either:

1. **Accepts** — final delivery is accepted. The warranty period begins per 01-7000 warranty terms
2. **Identifies gaps** — specific conditions not met, with reference to 01-7000 requirements. The agent addresses the gaps and resubmits

---

## Phase 5: Warranty

Per GC-12 Section 12.3 and the warranty period defined in 01-7000:

1. For the defined period after acceptance, the agent corrects defects without additional resource cost
2. **Warranty covers:** defects that existed at delivery but were not discovered during review; functionality that does not perform as specified in the SPEC-XXX files under normal conditions
3. **Warranty does not cover:** accepted deviations (listed in 01-7000); damage from user modifications; failure from conditions outside the specification; new requirements
4. The distinction between a defect (warranty) and a new requirement (new scope) is determined by the SPEC-XXX files. If the specification required it and it doesn't work, it's a defect. If the specification didn't require it, it's new scope

---

## Phase 6: Acceptance Finality

Per GC-13 Section 13.2:

After final delivery and warranty expiration:

1. The scope for revisiting completed work is limited
2. Work required after this point is new scope governed by a new specification (starting again at PROC-001)
3. Both parties accept the delivered state as project conclusion

**Exceptions:** Fraud, defects that could not reasonably have been discovered during warranty, and governing constraint violations.

---

## Handoff to Another Agent

Per GC-01 Section 1.4, when work transfers to a different agent:

1. Summary of work completed and its current state
2. Summary of work remaining — punch list, backlog, in-progress items
3. All project documents — 01-1000 through 01-7000, all SPEC-XXX files, DRAWINGS/, SUPPLEMENTARY_CONDITIONS/
4. Open clarification requests and their status
5. Known issues and risks
6. Key decision history — decisions made during the project and their rationale, so the receiving agent doesn't re-litigate settled questions

**Rules:**

1. The receiving agent reviews the handoff and confirms understanding before proceeding (GC-01.4.3)
2. The user is responsible for ensuring the receiving agent has access to all project documents (GC-01.4.4)

---

## Terminated Work

Per GC-07 Section 7.1, when work is terminated before completion:

1. Stop work immediately
2. Preserve all work in a usable state
3. Complete 01-7000 to the extent possible — honest status of what works, what doesn't, what was in progress, what wasn't started
4. The goal is to leave the work in the most usable state possible, even if termination is abrupt

This is not a failure state requiring a lesser standard of documentation. Terminated work gets the same handoff quality as completed work — the user needs it more, not less.
