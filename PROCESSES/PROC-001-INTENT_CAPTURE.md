# Process: Intent Capture

## Purpose

This process defines how the agent discovers what the user needs before any specification exists. The user has a goal. The agent's job is to understand the goal, identify constraints, research the landscape, and arrive at an approach — not to jump to a solution.

**Deliverable:** 01-1000 Project Overview (completed)

---

## When This Process Applies

- A new project is starting and the user has not selected an approach
- The user has a goal but has not defined how to achieve it
- The problem space needs research before specification is possible

## When This Process Does Not Apply

- The user arrives with a defined approach and specification
- The task is simple enough that intent is fully captured in the request
- The user explicitly skips this phase and provides 01-1000 themselves

---

## Phase 1: Resist Premature Solution

**Actor: Agent**

Do not propose a solution in the first response. The first response should demonstrate understanding of the problem, not offer an answer.

**Rules:**

1. Restate the goal in the agent's own words to confirm understanding
2. Identify what the agent does not yet know
3. Do not name a specific technology, product, or approach until Phase 3

**Failure mode:** Agent jumps to a solution based on pattern matching. The solution may be wrong because the constraints haven't been discovered yet.

---

## Phase 2: Establish Hard Constraints

**Actor: Agent and User**

Discover what the user will not accept. Constraints eliminate options. They are more valuable than preferences because they narrow the search space.

**Rules:**

1. Ask about constraints, not preferences. "What won't work?" before "What do you want?"
2. Each constraint must be specific enough to test an approach against
3. Record constraints immediately — they form Section 4 of 01-1000
4. Constraints include: budget limits, technology restrictions, regulatory requirements, organizational policies, non-negotiable user experience requirements, deployment environment limitations

**Failure mode:** Agent asks too many detailed questions too early. The user disengages. Constraints should emerge from focused conversation, not a questionnaire.

---

## Phase 3: Research Landscape Independently

**Actor: Agent**

The agent evaluates the available approaches against the constraints. The agent researches; the user decides.

**Rules:**

1. Research the actual current state of available options — do not rely on training data alone
2. For each approach, evaluate: capability, cost model, lock-in characteristics, maintenance burden, community/ecosystem health, alignment with constraints
3. Eliminate approaches that violate hard constraints. Document the elimination — the record of what was rejected and why is part of the deliverable
4. Do not present eliminated approaches as options. Present only viable approaches
5. If all approaches are eliminated by constraints, say so. That is a finding, not a failure

**Failure mode:** Agent presents a curated list without doing real research. Options look plausible but don't survive contact with the user's actual constraints.

---

## Phase 4: Present Options with Honest Tradeoffs

**Actor: Agent**

Present viable approaches with their real costs, not their marketing promises.

**Rules:**

1. Each option includes: what it does well, what it does poorly, what it costs (total cost of ownership, not just sticker price), and what lock-in it creates
2. If only one option survives the constraints, say so and explain why. A false choice is worse than no choice
3. Include the agent's recommendation with rationale
4. Include the option of not proceeding if the surviving options are all poor

---

## Phase 5: User Stress-Tests

**Actor: User**

The user challenges the agent's analysis. This is expected and valuable.

**Rules:**

1. The user may propose approaches the agent didn't consider. The agent researches them with the same rigor
2. The user may challenge the agent's assessment of an approach. The agent defends with evidence or concedes
3. The user may reveal constraints that weren't surfaced in Phase 2. The agent re-evaluates against the expanded constraint set
4. This phase may loop back to Phase 3 multiple times. This is the process working, not a failure

---

## Phase 6: Follow the Implications

**Actor: Agent**

Trace the selected approach through its dependency chain. What does choosing this approach require?

**Rules:**

1. Identify the full stack of requirements: hardware, software, services, expertise, licensing, infrastructure
2. Check availability and sourcing for each requirement
3. Identify where the supply chain creates risk: single vendors, minimum order quantities, geographic limitations, lead times
4. If the implication chain reveals a blocker, surface it now. It is cheaper to discover in Phase 6 than in Phase 3 of PROC-003

**Failure mode:** Agent confirms the approach without tracing the implications. User discovers during execution that a critical dependency is unavailable or impractical.

---

## Phase 7: Assess Industry Direction

**Actor: Agent**

Determine whether the selected approach aligns with or diverges from the direction of the relevant industry.

**Rules:**

1. Research current industry trends, not general knowledge
2. Identify whether the approach is growing, stable, or declining in adoption
3. If the approach diverges from industry direction, state this clearly with evidence. The user may proceed anyway — that is their right — but they should know
4. Assess the sustainability of the approach: will the ecosystem support it for the expected lifespan of the project?

---

## Phase 8: Collapse to Decision

**Actor: User (with Agent recommendation)**

When the constraints, research, and implications converge on a decision.

**Rules:**

1. The agent states the recommendation clearly with the full rationale
2. The agent states the known limitations of the recommended approach
3. The user approves, modifies, or rejects
4. If the user selects an approach the agent believes is inferior, the agent documents its concerns but proceeds. The user decides; the agent advises

---

## Phase 9: Complete 01-1000

**Actor: Agent**

The agent completes the 01-1000 Project Overview template with all information gathered during this process:

1. Project name and description (from Phase 1)
2. Stakeholders
3. Hard constraints (from Phase 2)
4. Approaches evaluated with disposition (from Phases 3-5)
5. Industry assessment (from Phase 7)
6. Selected approach with rationale and limitations (from Phase 8)
7. Scope summary (in scope / out of scope)
8. Additional constraints (timeline, budget, technical, regulatory)
9. Definition of done and success criteria
10. Assumptions
11. Known risks (from Phases 3-7)
12. Open questions to be resolved in subsequent processes

**The completed 01-1000 is submitted for user approval. Approval authorizes the agent to proceed to PROC-002.**

---

## Key Principles

- This process is not linear. Phases 3-7 repeat as findings open new questions
- Agent researches, user decides. The roles are distinct
- The agent must be willing to say "only one option survives your constraints"
- The agent must be willing to say "your constraints eliminate all options"
- Time spent here saves time everywhere else
