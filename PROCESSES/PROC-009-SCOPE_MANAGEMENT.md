# Process: Scope Management

## Purpose

This process defines how changes to baselined specifications are handled during execution. Requirements change. The system must accommodate change, not resist it. But changes must be acknowledged, their impact assessed, and the revised scope agreed upon.

In construction, this distinguishes Change Orders (agreed changes) from Change Directives (directed changes). Different types of change require different processes.

**Deliverable:** Amendments to SPEC-XXX files and Division 01 documents (01-3000, 01-5000, 01-6000 as affected)

---

## When This Process Applies

- The user requests a change to a baselined SPEC-XXX
- The agent discovers that a baselined specification needs revision
- Work already completed must be modified due to new information
- The approach proposal structure (reflected in 01-3000) needs to change

## When This Process Does Not Apply

- The specification hasn't been baselined yet — changes during PROC-003 are part of specification development, not scope management
- The user is providing a clarification that doesn't change scope (PROC-005)
- The agent is encountering unexpected conditions that may or may not require a scope change (PROC-010 — which may escalate to this process)

---

## Step 1: Recognize the Change

**Actor: Agent**

The hardest part of scope management is recognizing that a change has occurred.

**Indicators that a user statement is a scope change, not a clarification:**

1. It adds a requirement not in the SPEC-XXX
2. It removes or modifies a requirement that is in the SPEC-XXX
3. It changes acceptance criteria
4. It introduces a new component or eliminates a planned one (affects 01-3000)
5. It changes the priority, sequence, or dependencies between components (affects 01-3000)

**Indicators that a user statement is a clarification, not a scope change:**

1. It resolves ambiguity in the existing SPEC-XXX
2. It provides information the specification assumed but didn't state
3. The SPEC-XXX can be read to include the user's intent without modification

**Rules:**

1. When uncertain, treat it as a scope change. The cost of over-documenting a change is low. The cost of silently absorbing a scope change is high
2. The agent must name the change. "That would be a change to SPEC-001 Section 3, which currently requires X. You're asking for Y instead. Let me assess the impact." This is not bureaucracy — it is the mechanism that prevents scope creep

**Failure mode:** Agent absorbs scope changes silently, leading to work that doesn't match any documented specification. Or agent treats every user comment as a scope change, frustrating the user.

---

## Step 2: Classify the Change

**Actor: Agent, confirmed by User**

**Change Order** — agreed scope change:

- The change can be evaluated before proceeding
- Impact assessment is valuable because it affects planning, other components, or completed work
- The user benefits from understanding the impact before committing

**Change Directive** — directed change, proceed immediately:

- Urgency prevents waiting for impact assessment
- The change is clearly minor with limited blast radius
- The user explicitly directs the agent to proceed without assessment

**Rules:**

1. Default to Change Order. Change Directives are the exception
2. The user determines urgency, not the agent. If the agent believes impact assessment is important, it should say so — but the user decides
3. A Change Directive becomes a Change Order when the impact assessment is complete (GC-06.3.5)

---

## Step 3: Assess Impact (Change Order)

**Actor: Agent**

Per GC-06 Section 6.2.2:

1. **Description** — what is being changed, referencing the specific SPEC-XXX section
2. **Impact on completed work** — does anything already built need to be modified or discarded?
3. **Impact on remaining work** — does this change the sequence, dependencies, or complexity of upcoming components? (affects 01-3000)
4. **Impact on the approach** — does the structural design need revision?
5. **Options** — if there are multiple ways to implement the change, present them with tradeoffs

**Rules:**

1. The impact assessment must be honest. Do not minimize impact to avoid pushback, and do not exaggerate impact to discourage the change
2. If impact assessment requires significant effort, tell the user how long it will take. The user may decide the change isn't worth the assessment cost
3. Include the option of not making the change. The user should understand what they keep by not changing

---

## Step 4: User Decision

**Actor: User**

The user reviews the impact assessment and either:

1. **Approves** — the change is authorized. The agent updates the specifications and Division 01 documents
2. **Modifies** — the user adjusts the change based on the impact assessment
3. **Withdraws** — the user decides the change isn't worth the impact. The original specification stands
4. **Converts to directive** — the user decides to proceed without full assessment

---

## Step 5: Update Documents

**Actor: Agent**

1. Amend the affected SPEC-XXX file(s) — the updated specification becomes the new baseline
2. Update 01-3000 if the component sequence, review gates, or submittal schedule changed
3. Update 01-5000 if work restrictions changed
4. Update 01-6000 if technology stack or practices changed
5. Update DRAWINGS/ if reference material is affected
6. Record the change in 01-7000 Closeout scope change history
7. Modify completed work if the change requires it

**Rules:**

1. Future work is evaluated against the updated specification, not the original
2. Changes to 01-3000 (structural changes) should be reviewed per PROC-002 Phase 9

---

## Step 6: Execute (Change Directive)

**Actor: Agent**

Per GC-06 Section 6.3:

1. Proceed with the change immediately
2. Concurrently assess the impact
3. Report the impact assessment at the earliest opportunity
4. Update documents per Step 5 when assessment is complete
5. The directive becomes a Change Order when the assessment is acknowledged

**Rules:**

1. The agent complies with the directive even if it suspects the impact is significant. The user has accepted this risk
2. If the impact assessment reveals that the directive has broken something critical, notify the user immediately
