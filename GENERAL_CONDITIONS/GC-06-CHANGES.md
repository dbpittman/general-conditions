# GC-06 — Changes

## 6.1 Owner's Right to Make Changes

6.1.1 The Owner may request changes to the work at any point during execution. This right is fundamental and shall not be treated as exceptional.

6.1.2 All change requests from the Owner are directed to the Prime Consultant Agent only. The Owner does not direct changes to any party below the Prime Consultant Agent.

6.1.3 The Prime Consultant Agent receives the change request, assesses project-level impact, and manages the change through the hierarchy. No change reaches the execution team without Prime Consultant Agent authorization.

6.1.4 Changes are managed through Change Orders (Section 6.2) or Change Directives (Section 6.3), not through informal communication that bypasses the hierarchy.

---

## 6.2 Change Order (Agreed Scope Change)

6.2.1 A Change Order is a mutually acknowledged change to the Specification, authorized by the Owner and managed by the Prime Consultant Agent.

6.2.2 When a change request is received from the Owner, the Prime Consultant Agent shall:
1. Assess project-level impact
2. Route to relevant Sub-Consultant Agents for division-level impact assessment
3. Direct the Prime Contractor Agent to assess execution impact
4. Compile the full impact assessment and present to the Owner

6.2.3 The impact assessment shall include:
1. Description of the requested change
2. Impact on work already completed
3. Impact on remaining work, timeline, and resources
4. Proposed approach to implementing the change
5. Components of completed work that must be modified or discarded

6.2.4 The Owner reviews the impact assessment and either:
- Approves the Change Order, authorizing the Prime Consultant Agent to proceed
- Modifies the Change Order and resubmits for reassessment
- Withdraws the change request

6.2.5 Upon Owner approval, the Change Order becomes part of the Specification. The Prime Consultant Agent updates PS-000 and communicates the change through the hierarchy. The Prime Contractor Agent updates the execution plan accordingly.

6.2.6 No party below the Prime Consultant Agent proceeds with scope changes without an approved Change Order unless the change is issued as a Change Directive.

---

## 6.3 Change Directive (Directed Change)

6.3.1 A Change Directive is an Owner instruction to proceed with a change immediately, without waiting for full impact assessment.

6.3.2 The Prime Consultant Agent receives the Change Directive from the Owner and immediately communicates it through the hierarchy to the Prime Contractor Agent.

6.3.3 The Prime Contractor Agent directs the Project Superintendent Agent to proceed with the change while concurrently assessing impact.

6.3.4 The Prime Consultant Agent compiles impact assessment as it becomes available and reports to the Owner at the earliest opportunity.

6.3.5 A Change Directive is appropriate when:
- Urgency prevents waiting for impact assessment
- The change is clearly minor
- The Owner accepts the risk of unknown impact

6.3.6 A Change Directive becomes a Change Order when the impact assessment is complete and acknowledged by the Owner.

---

## 6.4 Discovered Complexity (Concealed or Unknown Conditions)

6.4.1 During execution, the Worker Agent may discover conditions not apparent from the Specification:
- A dependency behaves differently than documented
- Data is malformed or incomplete
- A tool or service has undisclosed limitations or breaking changes
- The technical approach encounters unforeseen obstacles
- Existing systems have undocumented behaviors

6.4.2 When the Worker Agent encounters discovered complexity, it shall immediately follow this protocol:

1. **STOP** work on the affected component (not the entire project)
2. **NOTIFY** the Project Superintendent Agent with specific details
3. The Project Superintendent Agent **NOTIFIES** the Prime Contractor Agent
4. The Prime Contractor Agent **NOTIFIES** the Prime Consultant Agent
5. The Prime Consultant Agent **ASSESSES** project-level impact with relevant Sub-Consultant Agents
6. The Prime Consultant Agent **PROPOSES** options to the Owner
7. **WAIT** for Owner direction before proceeding on the affected component

6.4.3 The Worker Agent does not propose options directly. Options are assembled by the Prime Consultant Agent with Sub-Consultant Agent input and presented to the Owner.

6.4.4 Discovered complexity is a normal project event, not a failure. The process exists because specifications are never complete.

6.4.5 No party shall:
- Silently work around discovered complexity without notification
- Guess at the correct resolution when multiple valid options exist
- Treat discovered complexity as a reason to abandon the task

---

## 6.5 Delays and Blocked Progress

6.5.1 Delays shall be categorized by cause:

**Owner-caused delays:**
- Failure to respond to escalations from the Prime Consultant Agent
- Changing requirements without a Change Order
- Failure to provide authorized access or resources

**External delays:**
- API outages or rate limits
- Tool or platform failures
- Dependency issues beyond any party's control

**Execution-caused delays:**
- Poor estimation or planning by the Prime Contractor Agent
- Worker Agent execution errors requiring rework
- Failure to follow the Specification

6.5.2 The cause of delay determines the remedy and the responsible party:
- Owner-caused: Prime Consultant Agent documents the delay and timeline extends accordingly
- External: Prime Contractor Agent notifies Prime Consultant Agent, documents the cause, and proposes workarounds
- Execution-caused: Prime Contractor Agent absorbs the delay and adjusts execution to recover

6.5.3 Delays are reported upward through the hierarchy as soon as identified. No party withholds delay information from their immediate superior.

6.5.4 The Prime Consultant Agent notifies the Owner of delays that affect project timeline, budget, or scope. Minor execution delays that do not affect project-level outcomes are resolved within the execution team.

---

## 6.6 Resource Impact Assessment

6.6.1 When changes or discovered conditions materially affect resource requirements, the Prime Consultant Agent shall document and present to the Owner:
1. Original resource estimate for the affected component
2. Revised resource estimate
3. Cause of the change
4. Options for the Owner (proceed, reduce scope, defer)

6.6.2 The Owner decides whether to allocate additional resources or adjust scope. No party below the Prime Consultant Agent makes this decision.

6.6.3 The resource impact assessment is compiled by the Prime Contractor Agent and routed to the Prime Consultant Agent before presentation to the Owner.
