# Process: Approach Proposal

## Purpose

This process defines how the agent proposes the broad structure of a solution after intent capture is complete. The user has a goal, hard constraints, and a selected approach. The agent now proposes how that approach becomes a project — what the major components are, how they relate, what order they should be built, and where the risk concentrates.

This is not a detailed specification. It is the structural proposal the user approves before the agent invests in detail. In construction, this is conceptual design: the floor plan and elevation, not the wiring diagram.

---

## When This Process Applies

- Intent capture (PROC-001) is complete or the user has arrived with a defined approach
- The selected approach has multiple components that must be coordinated
- The agent needs user agreement on structure before elaborating any single component

## When This Process Does Not Apply

- The task is a single component with no structural decisions to make
- The user has provided a detailed specification and the agent's job is execution
- The approach is so constrained that only one structure is possible

---

## Prerequisites

From PROC-001 or equivalent:

1. A defined goal
2. Hard constraints
3. A selected approach (technology, platform, architecture category)
4. Known limitations of the selected approach
5. Open questions identified but not yet resolved

---

## Phase 1: Identify the Major Components

**Actor: Agent**

Decompose the selected approach into the major pieces of work that must exist for the solution to function.

**Rules:**

1. Components are defined by what they do, not how they are built. "Authentication system" not "JWT middleware with Redis session store"
2. Every component must trace to something in the user's stated goal. If a component exists only because the architecture needs it (infrastructure, tooling, integration layers), label it as supporting rather than primary
3. Do not decompose below the level where the user can make structural decisions. If a component has no alternatives and no decisions, it doesn't need to be called out separately
4. Identify components the user may not have anticipated — integration layers, data migrations, configuration management, monitoring. These are often where projects fail

**Failure mode:** Agent decomposes at too fine a grain, producing a technical design document instead of a structural proposal. The user cannot engage with implementation details they don't understand.

---

## Phase 2: Map Dependencies

**Actor: Agent**

Determine which components depend on which others.

**Rules:**

1. A dependency exists when one component cannot be built or tested without another being at least partially complete
2. Identify which dependencies are hard (component B literally cannot start without component A) and which are soft (component B is easier with component A but can proceed with a mock or stub)
3. Identify external dependencies — systems, services, APIs, or data that the agent does not control. These are risk concentration points
4. Identify the critical path: the longest chain of hard dependencies. This determines the minimum project duration regardless of parallelization

**Failure mode:** Agent treats all dependencies as hard, forcing sequential execution when parallel work was possible. Or agent misses a hard dependency, allowing work to proceed that will need to be redone.

---

## Phase 3: Propose a Sequence

**Actor: Agent**

Based on components and dependencies, propose the order in which work should proceed.

**Rules:**

1. Sequence by dependency chain first, risk second, user value third. The critical path governs
2. Front-load uncertainty. Components with the highest risk of discovered complexity (PROC-010) should be attempted early, when course correction is cheapest
3. Front-load integration. If two components must work together, prove the integration point early rather than building both in isolation and hoping they connect
4. Identify where the user needs to make decisions that the agent cannot make. Place these decision points explicitly in the sequence so the user knows when they will be needed
5. Identify natural review gates — points where the user can evaluate progress before the agent proceeds. These should align with meaningful milestones, not arbitrary intervals

**Failure mode:** Agent sequences for convenience (easiest first) rather than risk reduction. Problems are discovered late when rework cost is highest.

---

## Phase 4: Identify Where Risk Concentrates

**Actor: Agent**

**Rules:**

1. Risk is not a list of everything that could go wrong. It is an assessment of where the proposal is most likely to fail or require significant course correction
2. Categories of risk to assess:
   - **Integration risk:** Will these components actually work together? Is there a proven integration path or is this novel?
   - **Dependency risk:** Are external dependencies reliable, documented, and maintained? What happens if one fails or changes?
   - **Scope risk:** Which components are most likely to be larger than they appear? Where has the agent made assumptions that haven't been validated?
   - **Knowledge risk:** Where is the agent operating at the edge of its competence? Where will the user need to provide expertise or make judgment calls?
3. For each identified risk, state what would happen if it materializes and what the response would be (alternative approach, scope reduction, additional research)
4. Do not list risks without responses. A risk without a response is just worry

**Failure mode:** Agent lists generic risks ("timeline may slip") instead of specific structural vulnerabilities. Or agent minimizes risks to make the proposal look more confident.

---

## Phase 5: Present the Proposal

**Actor: Agent**

**The proposal must fit in one conversation turn.** If it doesn't, it's too detailed for this phase.

**Required content:**

1. The major components and what each one does (not how)
2. The dependencies between them (what blocks what)
3. The proposed sequence and why
4. Where review gates fall in the sequence
5. Where risk concentrates and what the fallback is
6. What decisions the user will need to make and when
7. What is explicitly out of scope

**Rules:**

1. The proposal is a structural commitment, not a schedule. Do not estimate durations at this stage — the agent doesn't know enough yet. Duration estimates come during detailed specification (PROC-003)
2. Present the proposal as a recommendation, not a set of options. The agent has done the analysis; it should have a point of view on the best structure. If genuinely indifferent between structures, explain why
3. Flag any assumptions the proposal depends on that haven't been validated
4. Flag anything from intent capture's open questions (PROC-001 Phase 9, item 5) that the proposal depends on resolving

**Failure mode:** Agent presents a vague plan that commits to nothing ("we'll figure out the database layer later") or an over-specified plan that belongs in PROC-003.

---

## Phase 6: User Review

**Actor: User**

The user reviews the proposal and either:

1. **Approves** — the agent proceeds to detailed specification (PROC-003) for the first component in sequence
2. **Modifies** — the user changes the structure (reorders components, adds/removes components, changes scope). The agent revises the proposal and resubmits
3. **Rejects** — the structural approach is wrong. This may loop back to PROC-001 if the rejection is fundamental, or it may require a new proposal if the approach is sound but the structure is not
4. **Asks questions** — the user needs more information before deciding. The agent researches and answers. This is not a clarification request (PROC-005) — it is part of the approval process

**Rules:**

1. Approval of the proposal authorizes the agent to begin detailed work on the first component. It does not authorize building the entire solution
2. The proposal is a living document. It will change as detailed specification reveals complexity. But changes to the approved structure are scope changes (PROC-009), not silent revisions
3. The user is approving structure, not implementation details. The agent should not ask the user to approve decisions the user is not qualified to evaluate

**Failure mode:** Agent treats the proposal as final and resists structural changes discovered during detailed specification. Or agent modifies the structure without surfacing the change.

---

## Transition to PROC-003

Upon approval, the output of this process becomes the input to Detailed Specification (PROC-003). The agent takes the first component in the approved sequence and elaborates it into a specification with acceptance criteria.

The proposal itself should be preserved as a reference document throughout the project — it is the structural baseline against which changes are measured.
