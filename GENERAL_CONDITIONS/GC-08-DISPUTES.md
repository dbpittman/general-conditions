# GC-08 — Dispute Resolution

## 8.1 Specification as Authority

8.1.1 When there is a disagreement between User intent and Agent output, the Specification is the first authority.

8.1.2 If the output conforms to the Specification but not to User intent, the Specification is deficient, not the output. Resolution is a Change Order (GC-06 Section 6.2), not rework.

8.1.3 If the output does not conform to the Specification, it is defective work (GC-02 Section 2.4).

8.1.4 If the Specification is ambiguous and both interpretations are reasonable, neither party is at fault. Resolution is a Supplemental Instruction clarifying the intent, and the Agent adjusts the work accordingly.

## 8.2 Automated Evaluation

8.2.1 Where automated evaluation is available (test suites, linting, type checking, validation scripts), it shall be used as first-pass assessment before human review.

8.2.2 Automated evaluation results are advisory to the Evaluator, not dispositive, unless the Specification defines specific automated checks as acceptance criteria.

8.2.3 The Agent shall run applicable automated evaluations before submitting work for review.

## 8.3 Escalation Ladder

8.3.1 Disputes that cannot be resolved by reference to the Specification shall be resolved through progressive escalation:

1. **Agent Self-Correction** — Agent reviews its work against the Specification and corrects if deficient
2. **User Clarification** — User provides additional guidance on intent
3. **Re-specification** — The Specification is amended to remove ambiguity
4. **Alternative Approach** — A different method or agent is used for the disputed component
5. **Human Expert Review** — A human with domain expertise evaluates the dispute

8.3.2 Escalation should be proportional to the impact of the dispute. Minor issues should not require full escalation.

## 8.4 Preserved Options

8.4.1 Using one resolution path does not preclude others.

8.4.2 The User may accept partial output while disputing other components.

8.4.3 Resolution of one dispute does not establish precedent for other disputes unless the resolution is incorporated into the Specification or Supplementary Conditions.
