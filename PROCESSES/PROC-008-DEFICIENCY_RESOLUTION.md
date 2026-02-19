# Process: Deficiency Resolution

## Purpose

This process defines how rejected or non-conforming work is diagnosed, corrected, and resubmitted. When quality verification (PROC-007) identifies defects, this process resolves them.

In construction, this is the deficiency list (punch list): a systematic inventory of items that do not meet specifications, tied to the original requirements, with specific remediation for each.

**Deliverable:** Corrected work resubmitted via PROC-006. Amendments to SPEC-XXX files if deficiency resolution reveals specification gaps.

---

## When This Process Applies

- A submittal (PROC-006) is returned with deficiencies identified
- Quality verification (PROC-007) identifies non-conformance
- A defect is discovered after acceptance (within the warranty period per GC-12.3)

## When This Process Does Not Apply

- The user wants something different from what the specification says — that is a change order (PROC-009), not a deficiency
- The specification was ambiguous and both interpretations are reasonable — that is a clarification (PROC-005), not a deficiency
- The user changed requirements after the work was approved — that is a change order (PROC-009)

---

## Phase 1: Classify the Finding

**Actor: Agent**

Before correcting, determine what the finding actually is. Per GC-02 Section 2.4 and GC-08 Section 8.1:

1. **Defect** — the output does not conform to the SPEC-XXX acceptance criteria. The agent's work is at fault. Correction is the agent's responsibility at no additional resource cost (GC-02.4.2)
2. **Specification gap** — the SPEC-XXX didn't address this requirement. The output conforms to what was specified but not to what the user intended. Resolution is a change order (PROC-009) or supplemental instruction (PROC-005)
3. **Ambiguity** — the specification can be reasonably interpreted multiple ways and the agent chose one. Neither party is at fault. Resolution is a clarification (PROC-005) with adjustment
4. **Changed requirement** — the user's expectation has shifted since the specification was baselined. Resolution is a change order (PROC-009)

**Rules:**

1. This classification matters because it determines responsibility. The agent corrects defects. The user authorizes scope changes. Neither party should absorb the other's cost
2. If the classification is disputed, the specification is the authority (GC-08.1.1). The output either conforms to the SPEC-XXX acceptance criteria or it doesn't
3. The agent should not accept defect classification when the specification supports its output, and should not dispute defect classification when the specification clearly requires something different from what was produced

**Failure mode:** Every rejection is treated as a defect, causing the agent to rework without questioning whether the specification supports the rejection. Or every rejection is disputed, delaying resolution.

---

## Phase 2: Diagnose the Defect

**Actor: Agent**

For confirmed defects:

**Rules:**

1. Identify the specific SPEC-XXX acceptance criterion that was not met
2. Determine why the defect occurred — was the specification misread, was the implementation incorrect, was a dependency at fault, or was this a class of error the agent tends to make?
3. Assess whether the same class of defect exists elsewhere in the work. A pattern defect is more serious than an isolated one
4. Determine the correction scope — what exactly needs to change, and what is the blast radius of the change

**Failure mode:** Agent patches the symptom without understanding the cause. The defect recurs in a different form.

---

## Phase 3: Propose Correction

**Actor: Agent**

Per GC-02 Section 2.4.4:

1. Identify the specific deficiency against the SPEC-XXX acceptance criterion
2. Propose a correction approach — what will change and why this correction will resolve the deficiency
3. Identify any impact on other completed work — does this correction require changes elsewhere?
4. If the correction is complex or risky, present it for user approval before executing. If straightforward, note the approach in the resubmission

**Rules:**

1. The correction must address the root cause, not just the symptom
2. The correction must not introduce new defects. If the change has a blast radius, verify the affected areas per PROC-007
3. If the defect reveals that the approach is fundamentally flawed (not just an implementation error), escalate — this may require revisiting PROC-004 (Execution Instructions) or PROC-003 (Detailed Specification)

---

## Phase 4: Execute Correction and Resubmit

**Actor: Agent**

1. Execute the correction
2. Verify the correction against the original SPEC-XXX acceptance criterion (PROC-007)
3. Verify that the correction hasn't introduced regressions
4. Resubmit per PROC-006, explicitly referencing the original deficiency and how it was resolved

**Rules:**

1. The resubmission must demonstrate that the specific deficiency has been resolved, not just that the work has been updated
2. If the original deficiency was part of a pattern, the resubmission should confirm that the pattern has been addressed throughout the work

---

## User Acceptance of Defective Work

Per GC-02 Section 2.4.5 and GC-05 Section 5.7:

The user may accept defective work without correction. This requires:

1. The deviation is explicitly documented
2. The impact of the deviation is understood
3. The acceptance is recorded as a SPEC-XXX amendment and noted in 01-7000 Closeout under accepted deviations

Accepted deviations are not defects for warranty purposes (GC-12.3).
