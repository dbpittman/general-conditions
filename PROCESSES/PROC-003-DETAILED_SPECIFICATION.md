# Process: Detailed Specification

## Purpose

This process defines how the agent elaborates an approved approach proposal into component-level specifications with testable acceptance criteria. The user has approved the structure. The agent now works through each component, resolving design decisions and producing specifications precise enough to build against.

This is iterative. The agent proposes specifics, the user confirms or redirects, and the specification becomes progressively more detailed. In construction, this is design development: the architect and owner refine the approved concept into specific systems, materials, and details.

**Deliverables:**
- SPECIFICATIONS/SPEC-XXX-[component_name].md (one per component)
- 01-3000 Submittals (updated — component-level submittals added for this component)

---

## When This Process Applies

- 01-3000 Submittals is approved (PROC-002 complete)
- A component is next in the approved sequence
- The component has design decisions that require user input before building

## When This Process Does Not Apply

- The component is fully specified by the user or a prior process
- The component is trivial and can be specified inline during execution
- The user has explicitly authorized the agent to make all design decisions for this component

---

## Prerequisites

From PROC-002:

1. 01-3000 with approved component sequence and review gates
2. 01-6000 with approved technology stack
3. 01-5000 with project-level work restrictions
4. DRAWINGS/ with architecture and reference material
5. Component dependencies mapped

---

## Phase 1: Elaborate the Component

**Actor: Agent**

Take one component from the approved sequence (01-3000) and define what it must do at a level sufficient to build and test.

**Rules:**

1. Define scope boundaries — what this component does and explicitly what it does not do
2. Define interfaces — how this component connects to other components, external systems, and the user
3. Define acceptance criteria — specific, testable conditions that must be true when the component is complete. Every criterion must be verifiable without subjective judgment
4. Identify design decisions that require user input. Present each decision with the options, tradeoffs, and the agent's recommendation
5. Identify design decisions the agent can make without user input. State the decision and rationale. The user can override but shouldn't need to review every technical choice
6. Reference the relevant GC clauses that apply to this component (quality standards from GC-03.7, security requirements from GC-09, etc.)

**Failure mode:** Agent produces acceptance criteria that are vague ("system should be fast") or untestable ("good user experience"). Or agent makes design decisions that should be the user's without surfacing them.

---

## Phase 2: Identify What the Agent Doesn't Know

**Actor: Agent**

**Rules:**

1. Explicitly list assumptions the specification depends on that haven't been validated
2. Identify technical questions that require research or prototyping before the specification can be finalized
3. Identify questions that require user input — business rules, preferences, priorities
4. Do not write a specification around unknowns. Flag them, resolve them, then specify. A specification that says "TBD" is not a specification
5. If resolving an unknown requires a prototype or spike, define the spike as a prerequisite task with its own acceptance criteria

**Failure mode:** Agent writes a specification that implicitly assumes answers to unresolved questions. The assumptions surface as defects during execution.

---

## Phase 3: Draft the Specification

**Actor: Agent**

Produce a SPECIFICATIONS/SPEC-XXX-[component_name].md file.

**Required content:**

1. **Scope** — what this component does and its boundaries
2. **Acceptance criteria** — specific, testable conditions (pass/fail)
3. **Interfaces** — connections to other components and external systems
4. **Constraints** — limits that apply to this component (references 01-5000 and GC-09)
5. **Dependencies** — what must exist before this component can be built
6. **Assumptions** — what the specification assumes to be true
7. **Design decisions** — agent decisions (documented) and user decisions (recorded)
8. **Open items** — questions that must be resolved before or during execution
9. **Submittals** — intermediate review points for this component's execution. Based on the component's complexity, risk, and dependency relationships, define what the agent must submit for review and when. Add these to the component-level submittals section of 01-3000

**Rules:**

1. The specification must be self-contained. An agent (or a different agent) should be able to build the component from this document plus the General Conditions and Division 01 without requiring conversation history
2. Acceptance criteria are pass/fail. If a criterion requires judgment, it is not specific enough
3. Constraints include both technical constraints and any relevant restrictions from 01-5000
4. Add any project-specific terms to 01-2000 Definitions

**Failure mode:** Specification requires reading the entire conversation history to understand. Or specification is a requirements list without enough context to build against.

---

## Phase 4: User Review

**Actor: User**

The user reviews the draft specification and either:

1. **Approves** — the specification is baselined and the agent may proceed to PROC-004 (Execution Instructions)
2. **Modifies** — the user changes requirements, acceptance criteria, or scope. The agent revises and resubmits
3. **Asks questions** — the user needs clarification on what a criterion means or why a decision was made
4. **Identifies missing requirements** — the user realizes something is needed that the specification doesn't cover. This is a specification addition, not a change order (the specification isn't baselined yet)

**Rules:**

1. Approval baselines the specification. Changes after this point are change orders (PROC-009)
2. If the user modifies scope in a way that affects the approach proposal (adds components, changes dependencies, alters sequence), 01-3000 must be updated per PROC-009
3. The user is approving what will be built and how it will be tested. The agent owns how it will be built

**Failure mode:** Agent treats the specification as final and resists changes discovered during PROC-004. Or agent modifies the baselined specification without surfacing the change.

---

## Phase 5: Repeat for Next Component

The agent takes the next component in the approved sequence (01-3000) and repeats from Phase 1. Components may be specified in parallel if they are independent.

Detailed specification of later components may reveal that earlier specifications need revision. This is normal. Revisions to baselined specifications are change orders (PROC-009).

---

## Transition to PROC-004

Upon approval, the SPEC-XXX file becomes the governing document for that component's execution. The agent proceeds to PROC-004 (Execution Instructions) to plan implementation, producing the component-level entries in 01-4000 (Quality) and completing 01-6000 (development practices).
