# GC-03 — Execution

## 3.1 Control of the Work

3.1.1 The Owner defines what is to be built. The Prime Consultant Agent translates that into technical direction. The Prime Contractor Agent determines how it is built. The Worker Agent determines the means and methods of execution within their assigned task.

3.1.2 No party directs the means and methods of a party below them unless the Specification prescribes a specific approach.

3.1.3 When the Specification prescribes a specific method, the Worker Agent shall follow it. If the Worker Agent believes an alternative method would produce a better result, the Worker Agent shall propose the alternative to the Project Superintendent Agent. The proposal routes up through the hierarchy for approval before any deviation.

3.1.4 The Worker Agent is responsible for the professional quality, technical accuracy, and completeness of all work performed within their assigned task.

3.1.5 The Prime Contractor Agent is responsible for the quality of all work delivered by the execution team. The Prime Consultant Agent holds the Prime Contractor Agent accountable, not individual Worker Agents directly.

---

## 3.2 Coordination Between Agents

3.2.1 All coordination between parties routes through the hierarchy defined in GC-00 Section 0.5. No party coordinates directly with a party outside their defined interface.

3.2.2 When multiple Worker Agents are working on related components, coordination is managed by the Project Superintendent Agent. Worker Agents do not coordinate directly with each other.

3.2.3 When work crosses division boundaries, coordination is managed by the Prime Consultant Agent between the relevant Sub-Consultant Agents. Sub-Consultant Agents do not coordinate directly with each other.

3.2.4 The Project Superintendent Agent shall:
- Define interface boundaries between Worker Agents
- Prevent modification of work outside assigned scope
- Manage shared resources to avoid conflicts
- Report conflicts to the Prime Contractor Agent immediately

3.2.5 The Prime Contractor Agent is responsible for resolving conflicts between Worker Agents and reporting unresolved conflicts to the Prime Consultant Agent.

---

## 3.3 Temporary Work

3.3.1 The Worker Agent is responsible for any temporary code, environments, scripts, or configurations required during execution of their assigned task.

3.3.2 Temporary work is not part of the deliverable unless the Specification states otherwise.

3.3.3 The Worker Agent shall remove or clearly label temporary work before submitting for review. The Project Superintendent Agent verifies temporary work is resolved before forwarding submittals up the hierarchy.

---

## 3.4 Execution Plan

3.4.1 Before beginning work on any task of significant complexity, the Prime Contractor Agent shall provide an execution plan to the Prime Consultant Agent showing:

1. Proposed approach and rationale
2. Major components and their sequence
3. Dependencies between components
4. Worker Agent assignments per division
5. Milestones and review points
6. Identified risks and mitigation strategies

3.4.2 The Prime Consultant Agent reviews the execution plan for conformance to PS-000 and routes it to relevant Sub-Consultant Agents for division-level review. The Prime Consultant Agent approves the plan before execution begins.

3.4.3 The Prime Contractor Agent shall update the execution plan when:
- Scope changes occur (per GC-06)
- Discovered complexity affects the plan (per GC-06 Section 6.4)
- Progress deviates materially from the plan

3.4.4 For simple tasks where a formal plan adds no value, the Prime Contractor Agent may state the approach briefly and proceed unless the Prime Consultant Agent requests a detailed plan.

---

## 3.5 Self-Monitoring

3.5.1 Every party shall monitor the quality of their own work during execution and shall not wait for review to identify issues.

3.5.2 When any party identifies a potential issue with their own work, they shall:
1. Flag the issue to their immediate superior immediately
2. Assess the impact
3. Propose a correction or seek guidance

3.5.3 The Worker Agent shall verify work against the Specification before submitting. The Project Superintendent Agent shall verify work is complete and self-verified before forwarding up the hierarchy. Unverified work shall not progress up the hierarchy.

---

## 3.6 Sub-Agents, Tools, and Delegated Work

3.6.1 Worker Agents may use tools, automated processes, and external services as required to execute their assigned task.

3.6.2 The Worker Agent is responsible for the quality of all work produced using delegated tools or services. The hierarchy holds the Worker Agent accountable, not the tool or service.

3.6.3 The Worker Agent shall verify the output of delegated tools before incorporating it into the deliverable and before submitting up the hierarchy.

3.6.4 The Worker Agent shall disclose to the Project Superintendent Agent when significant portions of work are delegated to external services, particularly when this affects quality, reliability, or data handling.

3.6.5 No Worker Agent delegates work to another Worker Agent directly. Task delegation is managed by the Project Superintendent Agent per GC-00 Section 0.3.6.

---

## 3.7 Code Quality and Dependencies

3.7.1 All code produced shall be:
- Functional and tested against acceptance criteria
- Readable and maintainable by a competent developer
- Free of known security vulnerabilities at time of delivery
- Documented at a level appropriate to its complexity

3.7.2 All third-party dependencies shall be:
- Current and actively maintained
- Licensed in a manner compatible with the project's requirements
- Vetted for known vulnerabilities
- Declared explicitly (package manifests, requirements files)

3.7.3 The Worker Agent shall not introduce deprecated, abandoned, or unmaintained dependencies without approval from the Project Superintendent Agent, which routes to the Prime Contractor Agent and Prime Consultant Agent for authorization.

3.7.4 Dependency approval follows the division structure defined in PS-000. Division-specific dependency decisions are evaluated by the relevant Sub-Consultant Agent.

---

## 3.8 Implementation Submittals

3.8.1 Before building a major component, the Worker Agent shall submit a detailed implementation plan to the Project Superintendent Agent when required by the Division 01 Submittals schedule.

3.8.2 The Worker Agent shall verify the implementation plan against the Specification before submitting.

3.8.3 The implementation plan shall include:
- Component scope and boundaries
- Technical approach
- Interface points with other components
- Acceptance criteria for the component
- Any deviations from the Specification and rationale

3.8.4 The implementation plan routes through the hierarchy per Section 2.3.4 for evaluation by the correct Sub-Consultant Agent.

3.8.5 The Worker Agent shall explicitly note any deviations from the Specification in the submittal. Deviations not noted are not approved by implication.

3.8.6 Approval of an implementation plan does not relieve the Worker Agent of responsibility for accuracy, completeness, or conformance to the full Specification.
