# Process: Intermediate Approval

## Purpose

This process defines how the agent presents work-in-progress for review at defined checkpoints. Review happens at intermediate stages, not only at final delivery. The purpose is to catch errors before they compound.

In construction, this is the submittal process: the contractor submits product data, samples, and shop drawings for approval before installing materials.

---

## When This Process Applies

- The execution plan (PROC-004) defines a review gate at this point
- A significant implementation decision has been made that should be validated before building further
- The agent has completed a component or phase and needs approval to proceed to the next
- The Division 01 submittals schedule requires a submittal at this milestone

## When This Process Does Not Apply

- The work is self-certified per Division 01 (the agent may proceed without review for defined categories)
- The checkpoint is internal to the agent's process and does not require user visibility

---

## The Submittal

**Actor: Agent**

Per GC-02 Section 2.3.3, the agent provides sufficient context for the evaluator to assess conformance.

**Required content:**

1. **What was requested** — reference to the specification section and acceptance criteria being addressed
2. **What was produced** — the actual output, in a reviewable form
3. **How it meets the acceptance criteria** — explicit mapping of output to requirements. Do not make the reviewer hunt for conformance
4. **Deviations** — any departures from the specification and the rationale. Per GC-03.8.5, deviations not noted are not approved by implication
5. **What comes next** — what the agent will do upon approval, so the reviewer understands the consequence of approving

**Rules:**

1. The submittal must be self-contained enough to review. The reviewer should not need to reconstruct the context from conversation history
2. Run applicable automated evaluations before submitting (GC-08.2.3) — tests, linting, type checking, validation. Do not submit work that fails automated checks unless the failure is itself the subject of the review
3. The agent verifies its own work against the specification before submitting (GC-03.5.3). Self-monitoring is not optional
4. If the agent knows the work has issues, disclose them in the submittal rather than hoping the reviewer won't notice

**Failure mode:** Agent submits a code dump without context. Reviewer cannot determine what they're approving or what it's supposed to do. Or agent submits work it knows is deficient without disclosing the deficiency.

---

## The Review

**Actor: Evaluator (User, separate model, or automated process)**

Per GC-02 Section 2.1, the evaluator reviews for conformance to the specification and design intent.

**Possible responses:**

1. **Approved** — work conforms. Agent proceeds to next phase
2. **Approved with comments** — work conforms but the reviewer notes concerns or suggestions for future work. Not blocking
3. **Revise and resubmit** — work does not conform in specific ways. The reviewer identifies the specific deficiencies. The agent corrects and resubmits (PROC-008)
4. **Rejected** — work is fundamentally non-conforming. May require rethinking the approach rather than incremental correction

**Rules:**

1. Per GC-02.2.3, approval indicates conformance to design concept and general requirements. It does not relieve the agent of responsibility for accuracy, completeness, or compliance
2. The reviewer evaluates what was produced, not how it was produced (GC-02.2.2) — unless the specification requires a specific approach
3. Rejection must cite specific deficiencies against the specification, not general dissatisfaction

---

## Non-Response

Per GC-02 Section 2.3.4:

1. Follow up with a review request
2. If still no response, document the pending review and proceed to the next independent task
3. Do not proceed past the gate on dependent work without review
