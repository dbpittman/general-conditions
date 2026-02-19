# Process: Execution Instructions

## Purpose

This process defines how the agent translates an approved specification into a concrete execution plan — the step-by-step approach to building the component. The specification says what must be true when done. The execution instructions say how the agent will make it true.

In construction, these are the construction documents: fully detailed instructions from which the project is built. In practice, they are never truly complete — which is why clarification (PROC-005) and discovered complexity (PROC-010) processes exist.

**Deliverables:**
- 01-4000 Quality Requirements (completed — testing standards, automated checks, coding standards)
- 01-5000 Work Restrictions (completed — component-level restrictions added)
- 01-6000 Materials and Methods (completed — development practices, file structure, configuration management)

---

## When This Process Applies

- A SPEC-XXX file is approved and baselined (PROC-003 complete)
- The component is complex enough that the agent's approach should be visible before execution begins
- The 01-3000 submittals schedule requires an implementation plan for this component

## When This Process Does Not Apply

- The component is simple enough that the agent can state its approach in a sentence and proceed (per GC-03 Section 3.4.4)
- The user has explicitly waived the implementation plan requirement for this category of work

---

## Prerequisites

From PROC-003:

1. Approved, baselined SPEC-XXX with acceptance criteria
2. Defined interfaces and dependencies
3. Known constraints and assumptions

---

## Phase 1: Plan the Implementation

**Actor: Agent**

Decompose the specification into implementation steps.

**Rules:**

1. Steps should be ordered by dependency, then risk. Prove the hardest part first
2. Each step should have a verifiable outcome — something the agent can check before proceeding to the next step
3. Identify which steps require tools, environments, access, or data that the agent doesn't yet have. These are blockers that must be resolved before execution, not during
4. Identify which steps touch existing systems, data, or code. These require the protections defined in GC-09 — backups, least privilege, user authorization for destructive operations. Add component-level restrictions to 01-5000
5. Identify which steps will produce intermediate outputs suitable for review (PROC-006). Place review gates at points where catching an error prevents cascading rework

**Failure mode:** Agent plans a linear sequence with no verification between steps. Errors propagate through the entire implementation before anyone notices.

---

## Phase 2: Define Quality Standards

**Actor: Agent**

Complete 01-4000 with the quality requirements for this project:

1. Testing requirements — what types of tests, what coverage targets, what tools
2. Automated evaluation — which checks must pass before every submittal (PROC-006)
3. Coding standards — style guide, naming conventions, documentation requirements
4. Review criteria — what the evaluator specifically looks for

These standards apply to all components and are used by PROC-007 (Quality Verification) as the evaluation baseline.

If 01-4000 was already completed for an earlier component, review and update as needed for the current component.

**Failure mode:** Agent begins building without defining how quality will be measured. Quality verification (PROC-007) has no standard to evaluate against.

---

## Phase 3: Complete Development Practices

**Actor: Agent**

Complete the development practices section of 01-6000:

1. Branching strategy
2. Commit practices
3. File structure
4. Configuration management
5. Naming conventions beyond coding standards

If 01-6000 development practices were already completed for an earlier component, review and update as needed.

---

## Phase 4: Identify Specification Gaps

**Actor: Agent**

The specification will have gaps. They always do. The agent identifies them now rather than during execution.

**Rules:**

1. Walk through the implementation steps mentally. At each step, ask: does the specification tell me enough to do this without guessing?
2. Where the answer is no, formulate a clarification request (PROC-005). Do this before execution begins, not after discovering the gap mid-build
3. Where the specification is silent on a decision, determine if it's a decision the agent can make (means and methods, per GC-03.1) or one the user must make (requirements). Agent decisions are documented in the execution plan. User decisions become clarification requests
4. Distinguish between gaps that block execution and gaps that can be resolved in parallel. Only blocking gaps must be resolved before starting

**Failure mode:** Agent begins execution with known specification gaps and makes assumptions that the user would not have agreed with.

---

## Phase 5: Present the Execution Plan

**Actor: Agent**

Per GC-03 Section 3.4, submit the execution plan for review.

**Required content:**

1. Implementation steps in sequence
2. Verification criteria for each step
3. Review gates — which steps require user/evaluator review before proceeding
4. Identified specification gaps and proposed clarification requests (PROC-005)
5. Tools, environments, and access required
6. Any deviations from the specification the agent is proposing (with rationale, per GC-03.8.5)

**Rules:**

1. The plan is a submittal per GC-02. It requires approval before detailed execution begins
2. The plan does not need to be exhaustive for simple components. GC-03.4.4 permits a brief statement of approach for simple tasks
3. The plan should not re-specify the component. It references the SPEC-XXX file; it doesn't replace it
4. If the agent identifies that the specification needs revision based on the implementation analysis, raise this now — it's cheaper to revise the spec than to build against a known-deficient spec

---

## Phase 6: User Review

**Actor: User**

The user reviews the execution plan and either:

1. **Approves** — the agent begins execution, following the plan and submitting for review at the defined gates (PROC-006)
2. **Modifies** — the user changes the approach, sequence, or review gates. The agent revises
3. **Redirects** — the implementation analysis reveals that the specification needs revision. The process loops back to PROC-003 for the affected requirements

**Rules:**

1. Approval of the execution plan authorizes the agent to begin building
2. The user is reviewing the approach, not the implementation details. GC-03.1: the user defines what, the agent determines how
3. Clarification requests (PROC-005) identified in Phase 4 can proceed in parallel with plan approval

---

## Transition to Execution

Upon approval, the agent executes the plan, submitting intermediate outputs for review per PROC-006 at the defined gates. During execution, the agent may invoke:

- **PROC-005** (Clarification Protocol) when ambiguity is encountered
- **PROC-006** (Intermediate Approval) at review gates
- **PROC-007** (Quality Verification) for self-evaluation before submitting
- **PROC-009** (Scope Management) when requirements change
- **PROC-010** (Discovered Complexity) when unexpected conditions arise
