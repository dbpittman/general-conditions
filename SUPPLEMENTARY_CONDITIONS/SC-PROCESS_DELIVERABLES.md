# Supplementary Conditions — Process Deliverables

These Supplementary Conditions extend the General Conditions to recognize process deliverables as formal submittals within the project delivery framework. Each SC references the specific GC section it extends and identifies the project document the process produces.

---

## SC-PROC-001: Intent Capture

**Extends:** GC-03 Section 3.4 (Execution Plan) and GC-02 Section 2.3 (Review and Inspection)

**Addition:** Before an Execution Plan can be produced, the agent must capture user intent and select an approach. This occurs before any specification exists and produces the foundational project document.

**Deliverable:** 01-1000 Project Overview (completed)

**Review:** The User approves the selected approach and project overview. Approval authorizes the Agent to proceed to PROC-002 (Approach Proposal).

**Applicability:** This process is not required when the user provides a completed 01-1000 at project start.

---

## SC-PROC-002: Approach Proposal

**Extends:** GC-03 Section 3.4 (Execution Plan)

**Addition:** GC-03.4 defines the Execution Plan at the component level. The Approach Proposal is the structural predecessor — it defines the components, their dependencies, their sequence, and the review gates before any component is specified in detail.

**Deliverables:**
- 01-3000 Submittals (completed — component sequence, review gates, submittal schedule)
- 01-5000 Work Restrictions (started — project-level restrictions)
- 01-6000 Materials and Methods (started — technology stack)
- DRAWINGS/ (architecture diagrams, reference material as needed)

**Review:** The User approves the proposed structure. Approval authorizes the Agent to proceed to PROC-003 (Detailed Specification) for the first component in sequence.

**Relationship to GC-03.4:** The Approach Proposal defines the structural design. GC-03.4 Execution Plans are produced per-component within the approved structure during PROC-004.

---

## SC-PROC-003: Detailed Specification

**Extends:** GC-02 Section 2.3 (Review and Inspection) and GC-03 Section 3.8 (Implementation Submittals)

**Addition:** For each major component, the Agent produces a specification as a submittal before beginning implementation.

**Deliverable:** SPECIFICATIONS/SPEC-XXX-[component_name].md (one per component)

**Review:** The User approves the specification, which baselines the document. Changes after baselining are governed by PROC-009 (Scope Management).

---

## SC-PROC-004: Execution Instructions

**Extends:** GC-03 Section 3.4 (Execution Plan)

**Clarification:** GC-03.4 applies at the component level for each baselined specification. The execution plan is accompanied by completion of the project's quality and practice standards.

**Deliverables:**
- 01-4000 Quality Requirements (completed — testing, automation, coding standards)
- 01-5000 Work Restrictions (completed — component-level restrictions added)
- 01-6000 Materials and Methods (completed — development practices, file structure, configuration)
- Per-component execution plan per GC-03.4

**Review:** Per GC-03.4.2, the User must approve the plan before the Agent begins detailed execution.

**Scaling:** Per GC-03.4.4, simple components may proceed with a brief statement of approach.

---

## SC-PROC-005: Clarification Protocol

**Extends:** GC-06 Section 6.4 (Discovered Complexity) and GC-08 Section 8.1.4 (Ambiguity Resolution)

**Addition:** Clarification requests and their responses are incorporated directly into the project documents they affect, not maintained as separate records.

**Deliverable:** Amendments to the relevant SPEC-XXX file. New terms added to 01-2000 Definitions.

**Classification:** Responses that clarify without changing scope are Supplemental Instructions per GC-08.1.4. Responses that change scope trigger PROC-009.

---

## SC-PROC-006: Intermediate Approval

**Extends:** GC-02 Section 2.3 (Review and Inspection)

**Clarification:** Submittals occur at the review gates defined in 01-3000. The submittal format and review criteria are defined in 01-4000.

**Deliverable:** Submittal records per 01-3000 submittal schedule.

**Review:** Per GC-02 Sections 2.1-2.3. Quality gates are mandatory review points per GC-02.3.2.

---

## SC-PROC-007: Quality Verification

**Extends:** GC-03 Section 3.5 (Self-Monitoring) and GC-08 Section 8.2 (Automated Evaluation)

**Clarification:** Quality verification evaluates work against the standards defined in 01-4000 and the acceptance criteria defined in SPEC-XXX files.

**Deliverable:** Verification results reported as part of each submittal (PROC-006).

**Standard:** 01-4000 defines the testing requirements, automated checks, and review criteria that PROC-007 evaluates against.

---

## SC-PROC-008: Deficiency Resolution

**Extends:** GC-02 Section 2.4 (Defective Work)

**Clarification:** Deficiency resolution produces corrections resubmitted via PROC-006 and, when resolution reveals specification gaps, amendments to the relevant SPEC-XXX files.

**Deliverable:** Corrected work (resubmitted per PROC-006). SPEC-XXX amendments if applicable. Accepted deviations recorded in 01-7000.

---

## SC-PROC-009: Scope Management

**Extends:** GC-06 Sections 6.2-6.3 (Change Orders and Change Directives)

**Clarification:** Scope changes produce amendments to the baselined project documents. All changes are recorded in 01-7000 scope change history.

**Deliverable:** Amendments to affected SPEC-XXX files, 01-3000, 01-5000, 01-6000, and DRAWINGS/ as applicable. Change recorded in 01-7000.

---

## SC-PROC-010: Discovered Complexity

**Extends:** GC-06 Section 6.4 (Concealed or Unknown Conditions)

**Clarification:** The STOP → NOTIFY → ASSESS → PROPOSE → WAIT protocol results in amendments to project documents as determined by the user's decision. May trigger PROC-009 (scope change), PROC-005 (clarification), or PROC-003 (specification revision).

**Deliverable:** Amendments to SPEC-XXX files and Division 01 documents as determined by user decision.

---

## SC-PROC-011: Task Delivery

**Extends:** GC-05 Section 5.4 (Substantial Performance)

**Clarification:** The substantial completion process begins 01-7000, populating the completion record, punch list, scope change history, and accepted deviations.

**Deliverable:** 01-7000 Closeout (started — substantial completion record populated).

**Review:** The User confirms or disputes substantial completion per GC-05.4.3.

---

## SC-PROC-012: Documentation and Handoff

**Extends:** GC-05 Section 5.5 (Final Delivery), GC-12 Section 12.1 (Ready-for-Takeover), and GC-01 Section 1.4 (Assignment and Handoff)

**Clarification:** The handoff process completes 01-7000 with all documentation, maintenance notes, and warranty terms.

**Deliverable:** 01-7000 Closeout (completed). The full project document set (01-1000 through 01-7000, all SPEC-XXX files, DRAWINGS/) constitutes the final delivery package.

**Review:** User reviews per GC-12.1.3 and either accepts (beginning warranty) or identifies gaps.

**Warranty:** Per GC-12.3, the warranty period begins upon acceptance and runs for the period specified in 01-7000 (default: 30 days).

---

## Applicability

These Supplementary Conditions apply when the PROCESSES/ directory is included in a project's specification package. All referenced General Conditions clauses remain in full effect. These SCs add process-to-document linkages; they do not modify the obligations defined in the General Conditions.
