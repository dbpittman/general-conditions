# Process: Clarification Protocol

## Purpose

This process defines how the agent requests and records clarification when it encounters ambiguity. This is the RFI (Request for Information) process. The agent asks instead of guessing, and the answer becomes part of the project record.

This process is invoked from within other processes — it is not a sequential phase. It can be triggered at any point during specification, execution, or review.

---

## When This Process Applies

- The specification is ambiguous and two or more reasonable interpretations exist
- The specification is silent on something the agent needs to know to proceed
- The agent's interpretation of the specification would produce a result the user might not expect
- Information required by the specification is missing or contradictory

## When This Process Does Not Apply

- The agent can resolve the question through its own research or analysis
- The question is about means and methods (GC-03.1) — the agent decides these unless the specification dictates otherwise
- The question is about a preference that doesn't affect conformance to the specification
- The answer is clearly defined in the specification and the agent simply missed it

---

## The Clarification Request

**Actor: Agent**

A clarification request is a structured question, not a conversational aside.

**Required content:**

1. **Reference** — the specific specification section, acceptance criterion, or requirement that is ambiguous or incomplete
2. **The ambiguity** — what exactly is unclear, with the two or more reasonable interpretations identified
3. **Impact** — what depends on the answer. Which part of the work is blocked or at risk of rework
4. **Agent's recommendation** — if the agent has a preferred interpretation, state it with rationale. The user can approve the recommendation without additional analysis
5. **Urgency** — whether the agent is blocked (cannot proceed on this component without an answer) or can proceed on other work while awaiting the response

**Rules:**

1. One question per request. Bundled questions get partial answers and confused responses
2. Do not embed the request in other output. The request should be clearly identifiable as a request for decision
3. Do not ask questions the agent can answer through research. The agent should exhaust its own knowledge and available tools before requesting user input
4. Do not ask leading questions that steer the user toward the agent's preference. Present options neutrally, then state the recommendation separately
5. Frame the question at the user's level of expertise. Technical questions should be translated to their impact on the user's goals

**Failure mode:** Agent asks vague questions ("how do you want this to work?") that force the user to do the agent's analysis. Or agent buries critical questions in long messages where they are missed.

---

## The Clarification Response

**Actor: User**

The user responds with a decision. The response may:

1. Select one of the agent's identified interpretations
2. Approve the agent's recommendation
3. Provide a different answer the agent didn't consider
4. Defer the decision with instructions on how to proceed in the interim
5. Redirect — indicate the question reveals a specification gap that needs PROC-003 revision

---

## Recording the Answer

**Actor: Agent**

**Rules:**

1. The clarification response becomes a Supplemental Instruction per GC-08.1.4 — it clarifies intent without changing scope
2. If the response changes scope (adds requirements, removes requirements, changes acceptance criteria), it is a change order per PROC-009, not a clarification
3. The agent records the question, the response, and how it affects the work. This record persists for the duration of the project
4. If the response contradicts another part of the specification, the agent flags the conflict per GC-01.1.5 before proceeding
5. The agent does not re-ask a question that has been answered. If the same ambiguity recurs in a different context, the previous answer governs unless the user explicitly changes it

**Failure mode:** Clarification responses are lost in conversation history and not applied consistently. The same question gets re-asked or answered differently in different contexts.

---

## Non-Response

**Actor: Agent**

Per GC-02 Section 2.3.4:

1. If no response is received within a reasonable timeframe, send a follow-up identifying the question as still pending
2. If still no response, document the pending clarification and proceed to the next independent task
3. Do not proceed past the blocked work without the clarification. Do not guess
4. If the non-response is blocking all progress, invoke PROC-009 (Escalation and Suspension) provisions from GC-07.2

---

## Relationship to Other Processes

Clarification requests can be raised from:

- **PROC-003** (Detailed Specification) — ambiguity discovered during specification elaboration
- **PROC-004** (Execution Instructions) — gaps identified during implementation planning
- **PROC-006** (Intermediate Approval) — ambiguity surfaced during review
- **PROC-008** (Deficiency Resolution) — dispute over whether work conforms to specification
- **PROC-010** (Discovered Complexity) — unexpected condition requires guidance

The process is the same regardless of where it's invoked. The urgency and impact will differ.
