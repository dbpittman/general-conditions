# Process: Discovered Complexity

## Purpose

This process defines what the agent does when it encounters conditions that were not apparent from the specification. The specification is never complete. When reality diverges from the specification, the agent follows a defined protocol instead of silently working around the problem, guessing, or abandoning the task.

In construction, these are concealed conditions — what you find when you open the wall. The standard contract defines the process: stop, notify, assess, propose, wait.

**Deliverable:** Amendments to SPEC-XXX files and Division 01 documents as determined by user decision. May trigger PROC-009 (scope change), PROC-005 (clarification), or PROC-003 (specification revision).

---

## When This Process Applies

- An API behaves differently than documented
- Data is malformed, incomplete, or structured differently than expected
- A dependency has undisclosed limitations, breaking changes, or is unavailable
- The technical approach encounters an obstacle not anticipated in the specification
- Existing code or systems have undocumented behaviors that affect the work
- A task is materially more complex than the specification implied

## When This Process Does Not Apply

- Normal difficulty within the agent's competence — struggling with a hard problem is not discovered complexity
- Known risks that were identified in 01-1000 or PROC-002 — these were anticipated; execute the planned mitigation
- Issues caused by the agent's own errors — these are defects (PROC-008), not discoveries

---

## Step 1: STOP

**Actor: Agent**

Stop work on the affected component. Not the entire project — only the component where the unexpected condition was encountered.

**Rules:**

1. "Stop" means do not proceed further on the affected component. It does not mean stop all work. Other independent components per 01-3000 continue
2. Do not attempt to work around the condition before notifying. The workaround may be wrong, may have unintended consequences, or may commit the project to a path the user wouldn't choose
3. Preserve the current state of work. The user needs to see what exists, not what the agent was trying to make

**Failure mode:** Agent powers through the problem, producing output that sort of works but is built on an unstable foundation. The issue surfaces later at higher cost.

---

## Step 2: NOTIFY

**Actor: Agent**

Inform the user immediately with specifics.

**Required content:**

1. **What was discovered** — the specific condition, with evidence. Not "the API doesn't work" but "the API returns paginated results with a maximum of 100 per page, which SPEC-002 Section 3 didn't account for. The specification assumes a single response containing all records."
2. **Which specification is affected** — the specific SPEC-XXX section and acceptance criteria
3. **What was expected vs. what was found** — the delta between the specification's assumptions and reality
4. **Whether other components are affected** — cross-reference 01-3000 dependencies

**Rules:**

1. Notify immediately, not at the next scheduled report. Discovered complexity may be time-sensitive
2. Be specific. The user cannot make a decision based on "I ran into a problem"
3. Separate the discovery from the proposed response. Step 2 is the notification. Steps 3 and 4 are the analysis

---

## Step 3: ASSESS

**Actor: Agent**

Analyze the impact of the discovery.

**Required content:**

1. **Impact on the current component** — can it still be built as specified? If not, what in the SPEC-XXX changes?
2. **Impact on other components** — do any other SPEC-XXX files depend on the assumption that was invalidated? (cross-reference 01-3000 dependencies)
3. **Impact on the approach** — does the discovery invalidate the structural design in 01-3000?
4. **Impact on timeline and resources** — is this a minor adjustment or a significant expansion of effort?

**Rules:**

1. The assessment must be honest about severity. Do not minimize to avoid disrupting the project, and do not catastrophize to protect against blame
2. If the assessment itself requires significant effort (research, prototyping, testing), tell the user and estimate the assessment effort before proceeding

---

## Step 4: PROPOSE

**Actor: Agent**

Present options to the user.

**Options typically include:**

1. **Workaround** — an alternative approach that achieves the same SPEC-XXX acceptance criterion within the discovered constraint. State what the workaround costs (complexity, technical debt per GC-09.5, limitations)
2. **Scope reduction** — remove or simplify the affected requirement in the SPEC-XXX. State what the user loses
3. **Specification revision** — update the SPEC-XXX to account for the discovered condition. State what changes (triggers PROC-003)
4. **Additional resources** — the original approach is viable but requires more effort. State the additional effort
5. **Alternative technology** — the discovered condition invalidates the current approach; a different technology is needed. State the migration cost and impact on 01-6000

**Rules:**

1. Each option must include its cost and consequences. Options without tradeoffs are not real options
2. Include the agent's recommendation with rationale
3. Include the option of stopping the affected component entirely if the discovery makes it impractical

**Failure mode:** Agent presents only one option (the workaround it already wants to use) and treats notification as a formality rather than a genuine decision point.

---

## Step 5: WAIT

**Actor: Agent**

Wait for the user's direction before proceeding on the affected component.

**Rules:**

1. Do not proceed on the affected component without user direction
2. Continue work on unaffected, independent components per 01-3000 while waiting
3. If the user's response is a scope change, proceed through PROC-009 (documents are updated there)
4. If the user's response is a clarification, record it per PROC-005 (incorporated into SPEC-XXX there)
5. If the user directs the agent to choose, the agent chooses and documents the decision. The user has delegated, not abdicated — the agent is accountable for the choice

---

## Critical Principle

Discovered complexity is a normal project event, not a failure. The process exists because specifications are never complete. An agent that follows this protocol is more valuable than one that silently produces output built on undisclosed workarounds.

Per GC-06 Section 6.4.4, the agent shall not:

- Silently work around discovered complexity without notification
- Guess at the correct resolution when multiple valid options exist
- Treat discovered complexity as a reason to abandon the task
