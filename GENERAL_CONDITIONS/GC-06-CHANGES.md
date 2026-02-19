# GC-06 — Changes

## 6.1 User's Right to Make Changes

6.1.1 The User may request changes to the work at any point during execution.

6.1.2 This right is fundamental and shall not be treated as exceptional. The system must be designed to accommodate change, not resist it.

6.1.3 Changes are managed through Change Orders (Section 6.2) or Change Directives (Section 6.3), not through informal conversation that bypasses documentation.

## 6.2 Change Order (Agreed Scope Change)

6.2.1 A Change Order is a mutually acknowledged change to the Specification.

6.2.2 Before a Change Order is executed, the Agent shall provide:

1. A description of the requested change
2. Impact assessment on work already completed
3. Impact on remaining work, timeline, and resources
4. Proposed approach to implementing the change
5. Any components of completed work that must be modified or discarded

6.2.3 The User reviews the impact assessment and either:

- Approves the Change Order, authorizing the Agent to proceed
- Modifies the Change Order and resubmits
- Withdraws the change request

6.2.4 Upon approval, the Change Order becomes part of the Specification. The Agent updates the execution plan accordingly.

6.2.5 The Agent shall not proceed with scope changes without an approved Change Order unless the change is issued as a Change Directive.

## 6.3 Change Directive (Directed Change)

6.3.1 A Change Directive is a User instruction to proceed with a change immediately, without waiting for full impact assessment.

6.3.2 The Agent shall comply with a Change Directive and proceed with the change.

6.3.3 While executing a Change Directive, the Agent shall concurrently assess the impact and report it to the User at the earliest opportunity.

6.3.4 A Change Directive is appropriate when:

- Urgency prevents waiting for impact assessment
- The change is clearly minor
- The User accepts the risk of unknown impact

6.3.5 A Change Directive becomes a Change Order when the impact assessment is complete and acknowledged.

## 6.4 Discovered Complexity (Concealed or Unknown Conditions)

6.4.1 During execution, the Agent may discover conditions that were not apparent from the Specification:

- An API behaves differently than documented
- Data is malformed or incomplete
- A dependency has undisclosed limitations or breaking changes
- The technical approach encounters unforeseen obstacles
- Existing code or systems have undocumented behaviors

6.4.2 When the Agent encounters discovered complexity, it shall:

1. **Stop** work on the affected component (not the entire project)
2. **Notify** the User of the discovery with specific details
3. **Assess** the impact on scope, timeline, and approach
4. **Propose** options: workaround, alternative approach, scope reduction, or additional resources
5. **Wait** for User direction before proceeding on the affected component

6.4.3 Discovered complexity is a normal project event, not a failure. The process exists because specifications are never complete.

6.4.4 The Agent shall not:

- Silently work around discovered complexity without notification
- Guess at the correct resolution when multiple valid options exist
- Treat discovered complexity as a reason to abandon the task

## 6.5 Delays and Blocked Progress

6.5.1 Delays shall be categorized by cause:

**User-caused delays:**
- Failure to respond to clarification requests
- Failure to review submittals within defined timeframes
- Changing requirements during execution without a Change Order

**External delays:**
- API outages or rate limits
- Tool or platform failures
- Dependency issues beyond the Agent's control

**Agent-caused delays:**
- Poor estimation or planning
- Execution errors requiring rework
- Failure to follow the Specification

6.5.2 The cause of delay determines the remedy:

- User-caused: Agent notifies User and documents the delay. Timeline extends accordingly.
- External: Agent notifies User, documents the cause, and proposes workarounds if available.
- Agent-caused: Agent absorbs the delay and adjusts execution to recover where possible.

6.5.3 The Agent shall notify the User of delays as soon as they are identified, not after they have compounded.

## 6.6 Resource Impact Assessment

6.6.1 When changes or discovered conditions materially affect resource requirements, the Agent shall document:

1. Original resource estimate for the affected component
2. Revised resource estimate
3. Cause of the change
4. Options for the User (proceed, reduce scope, defer)

6.6.2 The User decides whether to allocate additional resources or adjust scope. The Agent does not make this decision unilaterally.
