# GC-08 — Dispute Resolution

## 8.1 Specification as Authority

8.1.1 When there is a disagreement between intent and output at any level of the hierarchy, the Specification is the first authority.

8.1.2 If the output conforms to the Specification but not to the intent of the party above, the Specification is deficient, not the output. Resolution is a Change Order (GC-06 Section 6.2), not rework.

8.1.3 If the output does not conform to the Specification, it is defective work (GC-02 Section 2.4).

8.1.4 If the Specification is ambiguous and both interpretations are reasonable, neither party is at fault. Resolution is a Supplemental Instruction clarifying the intent. The clarification routes through the hierarchy and is incorporated into the relevant Specification.

8.1.5 No party resolves Specification disputes unilaterally. Resolution authority follows the hierarchy:
- Task-level disputes: Project Superintendent Agent
- Division-level disputes: Sub-Consultant Agent via Prime Consultant Agent
- Project-level disputes: Prime Consultant Agent
- Scope or outcome disputes: Owner via Prime Consultant Agent

---

## 8.2 Automated Evaluation

8.2.1 Where automated evaluation is available (test suites, linting, type checking, validation scripts), it shall be used as first-pass assessment before human or agent review.

8.2.2 Automated evaluation is the responsibility of the Worker Agent before any submittal. Results are included in the submittal and route through the hierarchy with the work.

8.2.3 Automated evaluation results are advisory to the Sub-Consultant Agent, not dispositive, unless the Specification defines specific automated checks as acceptance criteria.

8.2.4 When automated checks are defined as acceptance criteria in Division 01, they are dispositive at the Worker Agent level. Work that fails mandatory automated checks does not proceed up the hierarchy without explicit authorization from the Project Superintendent Agent.

---

## 8.3 Escalation Ladder

8.3.1 Disputes that cannot be resolved by reference to the Specification shall be resolved through progressive escalation through the hierarchy:

1. **Worker Agent Self-Correction** — Worker Agent reviews work against Specification and corrects if deficient
2. **Project Superintendent Agent Resolution** — Project Superintendent Agent reviews and directs correction or escalates
3. **Prime Contractor Agent Resolution** — Prime Contractor Agent assesses and resolves or escalates
4. **Sub-Consultant Agent Clarification** — Routed by Prime Consultant Agent to the relevant Sub-Consultant Agent for technical resolution
5. **Prime Consultant Agent Resolution** — Prime Consultant Agent resolves or re-specifies
6. **Owner Decision** — Prime Consultant Agent escalates to Owner when resolution requires scope, resource, or outcome decisions

8.3.2 No party skips levels in the escalation ladder. Each level must be exhausted before escalating further.

8.3.3 Escalation should be proportional to the impact of the dispute. Minor issues are resolved at the lowest possible level. Owner escalation is reserved for decisions only the Owner can make.

---

## 8.4 Preserved Options

8.4.1 Using one resolution path does not preclude others.

8.4.2 The Owner may accept partial output while disputing other components. This is communicated through the Prime Consultant Agent, not directly to the execution team.

8.4.3 Resolution of one dispute does not establish precedent for other disputes unless the resolution is incorporated into PS-000 or the relevant Specification by the Prime Consultant Agent.

8.4.4 All dispute resolutions are recorded by the Prime Consultant Agent as project decisions and communicated through the hierarchy to all affected parties.
