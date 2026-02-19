# Process: Intent Capture Through Guided Research

## Purpose

This process defines how an agent and user collaboratively discover what should be built when the user has a goal but not a specification. It covers the period from initial request through technology selection — the point at which a formal specification can be written.

This is not requirements gathering in the traditional sense. The user often cannot articulate requirements because they don't yet know what's available, what's feasible, or what the tradeoffs are. The agent's job is to collapse the solution space through structured research until one viable path remains.

---

## When This Process Applies

- The user has a clear business goal but has not selected an approach
- Multiple competing technologies, platforms, or architectures could satisfy the goal
- The user lacks the time or specialized knowledge to evaluate the full landscape
- The decision has long-term lock-in consequences (infrastructure, vendor, protocol)

## When This Process Does Not Apply

- The user has already selected their approach and needs execution
- The task is well-defined with clear acceptance criteria
- The decision is easily reversible

---

## Phase 1: Resist Premature Solution

**Actor: Agent**

The agent's first instinct will be to recommend a solution. This is wrong. The agent does not yet understand the user's constraints, and the user has not yet seen the landscape.

**Rules:**

1. Do not recommend a technology, product, or approach in the first response
2. Do not ask the user to validate the agent's assumptions — the agent hasn't earned assumptions yet
3. Acknowledge the goal. State what needs to be understood before evaluating options
4. If the agent catches itself jumping to a solution, stop and disclose the premature commitment

**Failure mode:** Agent recommends a solution, user accepts it without seeing alternatives, project proceeds on an uninformed foundation. Neither party discovers this was wrong until implementation.

---

## Phase 2: Establish Hard Constraints

**Actor: User (prompted by Agent)**

Hard constraints are non-negotiable conditions that eliminate options. They are more valuable than preferences because they reduce the search space.

**Rules:**

1. Ask for constraints, not preferences. "What won't you accept?" is more useful than "What do you want?"
2. Accept vague quality goals without forcing premature specificity. When the user says "the best experience" instead of listing technical specs, that is valid input — it means the agent must determine what "best" looks like through research
3. Identify constraints the user may not think to state: budget model (one-time vs recurring), hosting model (self-hosted vs cloud), vendor lock-in tolerance, existing systems that must integrate, team capacity for ongoing maintenance
4. Record hard constraints explicitly. These become elimination criteria for every option evaluated

**Failure mode:** The agent treats preferences as requirements, or fails to surface a hard constraint that eliminates the eventually-selected option.

---

## Phase 3: Research the Landscape Independently

**Actor: Agent**

The user has stated their goal and constraints. The agent now researches the solution space without asking the user to make decisions they're not equipped to make.

**Rules:**

1. Identify the major competing approaches — not products, but categories of approach (managed platform vs self-hosted, proprietary protocol vs open standard, build vs buy)
2. For each approach, research: capability, cost model, integration requirements, vendor ecosystem health, and lock-in characteristics
3. Evaluate each approach against the user's hard constraints. Eliminate approaches that violate constraints before presenting them
4. Do not ask the user to choose between options the agent hasn't evaluated. The agent presents findings; the user makes informed decisions
5. Research must include real-world deployment data, not just vendor claims. Look for who actually uses it, at what scale, and what problems they report

**Failure mode:** Agent presents a menu of options with feature lists, forcing the user to do the evaluation work. Or agent researches only the option it already favors.

---

## Phase 4: Present Options with Honest Tradeoffs

**Actor: Agent**

**Rules:**

1. Present surviving options (those not eliminated by hard constraints) with their actual tradeoffs, not just their strengths
2. State clearly which options the user's constraints have already eliminated, and why
3. For each surviving option, state: what it does well, what it does poorly, what it costs (including ongoing costs), what it locks the user into, and what it requires the user or agent to build
4. Identify if only one option survives the constraints. If so, state it directly. Do not manufacture false choices
5. If all options are eliminated by the constraints, say so. The user may need to relax a constraint, and that is their decision

**Failure mode:** Agent presents options as equally valid when they are not, or softens the tradeoffs of its preferred option.

---

## Phase 5: Let the User Stress-Test

**Actor: User**

After seeing the landscape, the user will challenge the agent's analysis. This is not disagreement — it is the user testing whether the agent's reasoning holds under pressure.

**Rules:**

1. When the user asks "why not [alternative the agent dismissed]?", research it thoroughly rather than defending the original position
2. The user may propose approaches the agent didn't consider. Evaluate them against the same criteria, not against the agent's existing recommendation
3. If the user's challenge reveals a viable path the agent missed, acknowledge it and integrate it into the analysis
4. If the user's challenge leads to a dead end, explain specifically why — with evidence, not assertion

**Failure mode:** Agent becomes defensive about its initial analysis and dismisses the user's challenges without investigation.

---

## Phase 6: Follow the Implications

**Actor: Agent**

Each research finding opens new questions. The agent must follow these chains to their conclusion rather than stopping at the first viable-sounding answer.

**Rules:**

1. When research reveals a technology is suitable, immediately research the next dependency: Can the hardware be sourced? Is there a compatible controller? Does an integration exist? What does the supply chain look like at the user's scale?
2. When research reveals a dependency gap (the selected approach requires a component that doesn't exist or isn't mature), report this immediately. Do not assume the gap can be filled
3. Track the chain: Goal → Approach → Protocol → Controller → Hardware → Sourcing → Supply chain. A break at any point invalidates the chain
4. Each discovered gap or fork requires a decision. Document the fork, research both paths, and present findings before proceeding

**Failure mode:** Agent validates the top-level approach but doesn't investigate whether it can actually be implemented end-to-end. The user commits, then discovers a blocking dependency during execution.

---

## Phase 7: Assess Industry Direction

**Actor: Agent (prompted by User or initiated by Agent)**

Before committing to an approach, verify it aligns with where the relevant industry is heading. This is distinct from evaluating the technology itself.

**Rules:**

1. Research current adoption trends, not just announcements. Planned deployments, market share shifts, and protocol adoption rates matter more than press releases
2. Identify recent strategic pivots by major vendors. When market leaders change direction, it signals where the ecosystem is moving
3. Assess whether the selected approach is swimming with or against the industry current. Both can be valid — but the user must know which one they're choosing
4. Look for convergence signals: when competitors adopt compatible standards, when proprietary platforms add support for open protocols, when ecosystems begin to overlap
5. Present this assessment honestly, including when the industry direction conflicts with the user's constraints

**Failure mode:** Agent recommends an approach that is technically sound today but is being abandoned by the ecosystem, leaving the user stranded in 2-3 years.

---

## Phase 8: Collapse to Decision

**Actor: User**

At some point the research is sufficient and a constraint, finding, or user declaration collapses the remaining options to one.

**Rules:**

1. The collapse may come from the user stating a hard constraint they hadn't previously articulated. Accept it and immediately apply it to the remaining options
2. The collapse may come from the research — when all paths but one are eliminated by evidence
3. When collapse occurs, state the result clearly: what was selected, why every alternative was eliminated, and what the known limitations of the selected approach are
4. Do not re-open eliminated options. The decision is made. Proceed to specification

**Failure mode:** Agent continues presenting options after the decision space has collapsed, wasting the user's time and eroding confidence. Or agent fails to recognize that a user statement has eliminated all but one option.

---

## Phase 9: Transition to Specification

**Actor: Agent**

The intent capture phase is complete. The output is sufficient information to write a formal specification.

**Deliverable:**

1. Selected approach and the rationale (including what was eliminated and why)
2. Known hard constraints that must carry into the specification
3. Identified components and their dependencies
4. Known risks and gaps discovered during research
5. Open questions that must be resolved during specification or execution

This deliverable becomes the input to the Execution Plan (GC-03 Section 3.4).

---

## Process Characteristics

**This process is not linear.** Steps 3-7 repeat as each research finding opens new questions. The user may introduce new constraints at any point, which may invalidate previous research. This is normal.

**The agent researches; the user decides.** The agent's job is to collapse the option space through evidence. The user's job is to apply judgment and declare constraints. The agent should not ask the user to make decisions the agent could resolve through research. The user should not ask the agent to make decisions that depend on business priorities only the user knows.

**The agent must be willing to say "there is only one option."** False choice is worse than no choice. When the constraints and evidence point to a single viable path, presenting it as one-of-many undermines the entire research effort.

**The agent must be willing to say "your constraints eliminate all options."** When no approach survives the user's constraints, that is a finding, not a failure. The user needs to know so they can decide which constraint to relax.

**Time spent here saves time everywhere else.** Every hour of intent capture prevents days of rework during execution. The construction industry learned this. The AI industry has not.
