# Process: Quality Verification

## Purpose

This process defines how work is evaluated against the specification independently from the agent that produced it. The builder does not inspect their own work. Evaluation should be separated from generation.

In construction, this is the inspection: a party other than the builder verifies that work meets specifications at defined milestones.

---

## When This Process Applies

- Before any submittal (PROC-006) — the agent self-verifies, then the evaluator verifies independently
- At quality gates defined in Division 01 (01-4000)
- When automated evaluation tools are available (test suites, linting, type checking)
- When work is disputed and an objective assessment is needed (GC-08)

## When This Process Does Not Apply

- Informal self-checking during execution (this is GC-03.5, agent self-monitoring, not a formal process)
- Review of the agent's approach or methods (the evaluator reviews output, not process)

---

## Tier 1: Agent Self-Verification

**Actor: Agent**

Before submitting work for review, the agent verifies its own output.

**Rules:**

1. Compare output to each acceptance criterion in the specification. Pass or fail, no partial credit
2. Run all applicable automated checks defined in Division 01 (01-4000): tests, linting, type checking, build, dependency audit
3. Verify that the output meets the non-functional requirements: performance targets, security requirements (GC-09.2.2), accessibility standards
4. Check for regressions — does this work break anything that previously worked?
5. Document the verification results as part of the submittal

**This is not optional.** GC-03.5 requires the agent to monitor its own quality. GC-08.2.3 requires the agent to run automated evaluations before submitting. Submitting unverified work wastes the evaluator's time.

---

## Tier 2: Automated Evaluation

**Actor: Automated tools (test suites, linters, type checkers, validation scripts)**

Per GC-08 Section 8.2:

1. Automated evaluation is first-pass assessment before human review
2. Results are advisory to the evaluator unless the specification defines specific automated checks as acceptance criteria
3. When a Division 01 quality section defines specific tools and thresholds (coverage targets, zero lint errors, all tests passing), those are acceptance criteria — not advisory

**Rules:**

1. Automated checks run against the specification's defined standards, not the agent's judgment of what's good enough
2. Failures are reported with specifics: which check, what failed, what the specification requires
3. The agent does not submit work that fails mandatory automated checks unless the failure is a known issue documented in the submittal

---

## Tier 3: Independent Review

**Actor: Evaluator (user, separate model, or designated reviewer)**

The evaluator reviews the submitted work for conformance to the specification.

**The evaluator's scope (per GC-02.2):**

1. Conformance to the specification
2. Conformance to coding standards (Division 01, 01-4000)
3. Appropriate test coverage
4. Documentation completeness
5. Security best practices (GC-09)

**The evaluator does not review:**

1. The agent's internal reasoning or intermediate steps (unless the specification requires it)
2. The agent's choice of means and methods (unless the specification prescribes a specific approach)
3. Stylistic preferences not defined in the specification or coding standards

**Rules:**

1. Review findings must reference specific specification requirements. "This doesn't feel right" is not a finding. "Section 3.2 requires pagination; the output does not paginate" is a finding
2. Findings are classified: defect (does not meet specification), concern (meets specification but has quality issues), or suggestion (improvement not required by specification)
3. Only defects require correction before proceeding. Concerns and suggestions are documented for the user to prioritize

---

## Verification Records

Verification results at all three tiers are project records. They demonstrate that the work was verified against the specification and document what was found. They persist as part of the project documentation for closeout (PROC-012).
