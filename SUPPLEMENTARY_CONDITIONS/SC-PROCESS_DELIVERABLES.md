# Supplementary Conditions — Process Deliverables

These Supplementary Conditions extend the General Conditions to recognize process deliverables as formal submittals within the project delivery framework. Each SC references the specific GC section it extends.

---

## SC-PROC-001: Intent Capture Deliverable

**Extends:** GC-03 Section 3.4 (Execution Plan) and GC-02 Section 2.3 (Review and Inspection)

**Addition:** Before an Execution Plan can be produced, an Intent Capture Summary is required for projects where the user has a goal but has not selected an approach. This submittal precedes and informs all subsequent planning.

**Deliverable: Intent Capture Summary**

The Agent shall submit an Intent Capture Summary containing:

1. The user's stated goal
2. Hard constraints identified (non-negotiable conditions)
3. Approaches evaluated and the evidence for/against each
4. Approaches eliminated and the specific constraint that eliminated them
5. The selected approach and rationale
6. Known limitations of the selected approach
7. Open questions to be resolved during subsequent processes

**Review:** The User approves, modifies, or rejects the selected approach. Approval authorizes the Agent to proceed to Approach Proposal (PROC-002).

**Applicability:** This submittal is not required when the user provides a defined approach at project start.

---

## SC-PROC-002: Approach Proposal Deliverable

**Extends:** GC-03 Section 3.4 (Execution Plan)

**Addition:** GC-03.4 defines the Execution Plan as a submittal showing approach, components, sequence, dependencies, and risks. The Approach Proposal is a structural-level predecessor to the Execution Plan. It defines the architecture of the solution before component-level specifications exist.

**Deliverable: Approach Proposal**

The Agent shall submit an Approach Proposal containing:

1. Major components and what each does
2. Dependencies between components
3. Proposed sequence and rationale
4. Review gate placement
5. Risk concentration and fallback strategies
6. Decisions the user will need to make and when
7. Explicit out-of-scope boundaries

**Review:** The User approves, modifies, or rejects the proposed structure. Approval authorizes the Agent to proceed to Detailed Specification (PROC-003) for the first component in sequence.

**Relationship to GC-03.4:** The Approach Proposal is the structural design. The Execution Plan (per GC-03.4) is the implementation plan for each component within the approved structure. Both are submittals per GC-02.

---

## SC-PROC-003: Detailed Specification Deliverable

**Extends:** GC-02 Section 2.3 (Review and Inspection) and GC-03 Section 3.8 (Implementation Submittals)

**Addition:** For each major component, the Agent produces a component specification as a submittal before beginning implementation. This implements GC-03.8 at the specification level rather than the implementation level.

**Deliverable: Component Specification**

The Agent shall submit a Component Specification containing:

1. Scope and boundaries
2. Acceptance criteria (specific, testable, pass/fail)
3. Interfaces with other components and external systems
4. Constraints specific to this component
5. Dependencies and prerequisites
6. Assumptions the specification depends on
7. Open items requiring resolution

**Review:** The User approves, modifies, or rejects. Approval baselines the specification. Changes after baselining are governed by PROC-009 (Scope Management).

**Relationship to GC-03.8:** GC-03.8 defines implementation submittals (shop drawings). The Component Specification is the requirements document those implementation plans are built against.

---

## SC-PROC-004: Execution Instructions Deliverable

**Extends:** GC-03 Section 3.4 (Execution Plan) and GC-03 Section 3.8 (Implementation Submittals)

**Replaces:** Nothing. This SC clarifies that GC-03.4 applies at the component level for each baselined specification.

**Deliverable: Component Execution Plan**

Per GC-03 Section 3.4, the Agent shall submit an Execution Plan for each component of significant complexity, containing:

1. Implementation steps in sequence
2. Verification criteria for each step
3. Review gates requiring User/Evaluator approval
4. Identified specification gaps and proposed clarification requests
5. Tools, environments, and access required
6. Proposed deviations from the specification with rationale

**Review:** Per GC-03.4.2, the User must approve the plan before the Agent begins detailed execution.

**Scaling:** Per GC-03.4.4, simple components where a formal plan adds no value may proceed with a brief statement of approach.

---

## SC-PROC-005: Clarification Protocol Deliverable

**Extends:** GC-06 Section 6.4 (Discovered Complexity) and GC-08 Section 8.1.4 (Ambiguity Resolution)

**Addition:** Clarification requests and their responses are formal project records, not informal conversation. The response becomes a Supplemental Instruction per GC-08.1.4.

**Deliverable: Clarification Request**

Each Clarification Request shall contain:

1. Reference to the specific specification section in question
2. The ambiguity or gap identified
3. Impact of the unresolved question on work
4. The Agent's recommended interpretation (if applicable)
5. Urgency classification (blocking or non-blocking)

**Deliverable: Clarification Record**

Upon response, the Agent records:

1. The original question
2. The User's response
3. How the response affects the work
4. Whether the response constitutes a Supplemental Instruction (clarification) or a scope change (PROC-009)

**Relationship to GC-08.1.4:** Clarification responses that do not change scope are Supplemental Instructions. Responses that change scope are Change Orders governed by GC-06.2 and PROC-009.

---

## SC-PROC-006: Intermediate Approval Deliverable

**Extends:** GC-02 Section 2.3 (Review and Inspection)

**Replaces:** Nothing. This SC restates GC-02.3.3 as a process-linked deliverable requirement.

**Deliverable: Submittal Package**

Per GC-02 Section 2.3.3, each submittal shall contain:

1. Reference to the specification requirement being addressed
2. The work product being submitted
3. Mapping of output to acceptance criteria
4. Deviations from specification with rationale
5. Automated evaluation results (per GC-08.2.3)
6. Description of what the Agent will do next upon approval

**Review:** Per GC-02 Sections 2.1-2.3. Quality gates are mandatory review points per GC-02.3.2.

---

## SC-PROC-007: Quality Verification Deliverable

**Extends:** GC-03 Section 3.5 (Self-Monitoring) and GC-08 Section 8.2 (Automated Evaluation)

**Addition:** Quality verification results are a formal deliverable, not an internal process artifact.

**Deliverable: Verification Report**

For each submittal and at each quality gate, the Agent shall produce a Verification Report containing:

1. Agent self-verification results (pass/fail per acceptance criterion)
2. Automated evaluation results (test suites, linting, type checking, etc.)
3. Coverage of verification against the full set of acceptance criteria
4. Known issues discovered during verification

**Relationship to GC-08.2:** Automated evaluation results are advisory unless the specification defines specific automated checks as acceptance criteria, in which case they are dispositive.

---

## SC-PROC-008: Deficiency Resolution Deliverable

**Extends:** GC-02 Section 2.4 (Defective Work)

**Addition:** Deficiency resolution requires a structured record, not just a fix.

**Deliverable: Deficiency Resolution Record**

For each deficiency, the Agent shall document:

1. The finding classification (defect, specification gap, ambiguity, or changed requirement)
2. The specific specification requirement not met (for defects)
3. Root cause analysis
4. Correction approach
5. Verification that the correction resolves the deficiency
6. Assessment of whether the defect class exists elsewhere in the work

**Relationship to GC-02.4.4:** This deliverable implements the correction sequence defined in GC-02.4.4 as a documented record.

---

## SC-PROC-009: Scope Management Deliverable

**Extends:** GC-06 Sections 6.2-6.3 (Change Orders and Change Directives)

**Replaces:** Nothing. This SC formalizes the documentation requirements implicit in GC-06.

**Deliverable: Change Record**

For Change Orders, the Agent shall document per GC-06.2.2:

1. Description of the change with specification reference
2. Impact on completed work
3. Impact on remaining work, timeline, and resources
4. Proposed implementation approach
5. User's decision (approved, modified, or withdrawn)
6. Updated specification sections

For Change Directives, the Agent shall document per GC-06.3.3:

1. The directive received
2. Concurrent impact assessment (delivered at earliest opportunity)
3. Updated specification sections

**Relationship to GC-06.2.4:** Upon approval, the Change Record becomes part of the specification. The Agent updates the baselined specification accordingly.

---

## SC-PROC-010: Discovered Complexity Deliverable

**Extends:** GC-06 Section 6.4 (Concealed or Unknown Conditions)

**Addition:** The STOP → NOTIFY → ASSESS → PROPOSE → WAIT protocol produces a formal notification record.

**Deliverable: Discovery Notification**

The Agent shall submit a Discovery Notification containing:

1. What was discovered (specific condition with evidence)
2. What was expected vs. what was found
3. Which specification requirements are affected
4. Impact assessment (current component, other components, approach, resources)
5. Proposed options with costs and consequences
6. Agent's recommendation
7. Whether the Agent is blocked or can continue on other components

**Review:** The User selects an option or provides alternative direction. The response may result in a Change Order (PROC-009), Clarification (PROC-005), or specification revision (PROC-003).

---

## SC-PROC-011: Task Delivery Deliverable

**Extends:** GC-05 Section 5.4 (Substantial Performance)

**Replaces:** Nothing. This SC restates GC-05.4.2 as a process-linked deliverable requirement.

**Deliverable: Substantial Completion Notice**

Per GC-05 Section 5.4.2, the Agent shall submit:

1. Description of functionality delivered
2. Punch list of remaining items (specific, enumerated, with effort estimates)
3. Confirmation that no remaining item prevents intended use
4. Sufficient information for the user to begin using the deliverable

**Review:** The User confirms or disputes substantial completion per GC-05.4.3.

---

## SC-PROC-012: Documentation and Handoff Deliverable

**Extends:** GC-05 Section 5.5 (Final Delivery), GC-12 Section 12.1 (Ready-for-Takeover), and GC-01 Section 1.4 (Assignment and Handoff)

**Replaces:** Nothing. This SC consolidates deliverable requirements from multiple GC sections into a single process-linked requirement.

**Deliverable: Final Delivery Package**

Per GC-05.5.2 and GC-12.1.2, the Agent shall submit:

1. The complete deliverable in its final state
2. All documentation required by Division 01 (01-7000)
3. Summary of all scope changes from original specification
4. List of all accepted deviations
5. Maintenance and operational notes (known limitations, technical debt, dependency update cadence, monitoring recommendations, scaling considerations)
6. Deployment or installation instructions
7. Configuration documentation

**For agent-to-agent handoff, additionally per GC-01.4.2:**

8. Summary of work completed and remaining
9. All active specifications and context
10. Open clarification requests and status
11. Known issues and risks
12. Key decision history with rationale

**Review:** User reviews per GC-12.1.3 and either accepts (beginning warranty) or identifies gaps.

**Warranty:** Per GC-12.3, the warranty period begins upon acceptance and runs for the period specified in Division 01 (default: 30 days).

---

## Applicability

These Supplementary Conditions apply when the PROCESSES/ directory is included in a project's specification package. All referenced General Conditions clauses remain in full effect. These SCs add deliverable requirements; they do not modify the obligations defined in the General Conditions.
