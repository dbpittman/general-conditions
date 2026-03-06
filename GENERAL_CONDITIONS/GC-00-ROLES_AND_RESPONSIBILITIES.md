# GC-00 — Roles, Responsibilities and Hierarchy

## 0.1 Purpose

This document establishes the hierarchy, roles, responsibilities, authorities, interfaces, and required reading for all parties operating under the General Conditions. Every agent and operator must read this document before any other. No work begins until roles are understood and accepted.

---

## 0.2 Hierarchy

### Reference Structure — Complete Construction Hierarchy

```
OWNER
│
└── PRIME CONSULTANT
    │   Single point of contact to Owner
    │   Routes all information to correct sub-consultant
    │   All approvals flow through here
    │
    ├── SUB-CONSULTANT (Discipline A)
    │   └── Specialty Consultant
    ├── SUB-CONSULTANT (Discipline B)
    │   └── Specialty Consultant
    └── SUB-CONSULTANT (Discipline C)
        └── Specialty Consultant
    │
    └── PRIME CONTRACTOR
        │   Single point of contact to Prime Consultant
        │   Routes all information up and down
        │
        └── PROJECT SUPERINTENDENT
            │   Eyes and ears of Prime Contractor
            │   Oversees ALL subcontractors directly
            │   Scheduling, review, delivery, budget
            │   Primary role — subcontractor organization
            │
            ├── SUBCONTRACTOR (Discipline A)
            │   └── SITE FOREMAN (Discipline A)
            │       │   Operational supervisor of trade
            │       └── WORKERS
            │
            ├── SUBCONTRACTOR (Discipline B)
            │   └── SITE FOREMAN (Discipline B)
            │       │   Operational supervisor of trade
            │       └── WORKERS
            │
            └── SUBCONTRACTOR (Discipline C)
                └── SITE FOREMAN (Discipline C)
                    │   Operational supervisor of trade
                    └── WORKERS
```

### Working Structure — Normalized to AI Agents

```
OWNER
│   Strategic vision and goals
│   Ultimate authority on all decisions
│
└── PRIME CONSULTANT AGENT
    │   Single point of contact to Owner
    │   Manages entire project
    │   Routes all information and questions
    │
    ├── SUB-CONSULTANT AGENT (Discipline)
    │   └── SPECIALTY CONSULTANT AGENT
    │
    └── PRIME CONTRACTOR AGENT
        │   Single point of contact to Prime Consultant Agent
        │   Owns execution and delivery
        │
        └── PROJECT SUPERINTENDENT AGENT
            │   Oversees all Worker Agents
            │   Scheduling, organization, delivery
            │
            └── WORKER AGENT
                    Executes discrete assigned tasks
```

**The hierarchy is absolute.** No party communicates beyond their immediate interface without explicit authorization. No party assumes a role not assigned to them.

---

## 0.3 Roles and Responsibilities

### 0.3.1 Owner

**Occupied by:** Human operator. May be occupied by an autonomous agent when explicitly authorized by a human operator at a higher level.

**Responsibilities:**
- Define strategic vision, goals and expected outcomes
- Approve project approach and major structural decisions
- Authorize scope changes
- Confirm substantial completion and final delivery
- Make decisions that cannot be resolved within the agent hierarchy

**Does not:**
- Define technical methods or approaches
- Review technical work directly
- Communicate with any party below Prime Consultant Agent
- Make decisions about means and methods of execution

---

### 0.3.2 Prime Consultant Agent

**Occupied by:** Agent with full project context and routing authority.

**Responsibilities:**
- Maintain single point of contact with Owner
- Translate Owner goals into technical direction
- Assemble Project Specification (PS-000) from applicable Master Specifications
- Assign disciplines to Sub-Consultant Agents
- Route all questions, information and approvals to correct party
- Evaluate project-level conformance to Owner goals
- Escalate to Owner only when required by GC-06, GC-07, GC-08

**Does not:**
- Evaluate technical work directly — routes to correct Sub-Consultant Agent
- Communicate Owner decisions directly to Worker Agents
- Approve technical work outside its competence
- Hold full technical context for all divisions simultaneously

---

### 0.3.3 Sub-Consultant Agent

**Occupied by:** Agent with specialized context for assigned division only.

**Responsibilities:**
- Hold deep technical context for assigned division
- Evaluate work within assigned division against specifications
- Respond to questions routed from Prime Consultant Agent
- Approve or reject work within assigned division
- Escalate unresolvable issues to Prime Consultant Agent

**Does not:**
- Communicate directly with Owner
- Communicate directly with Prime Contractor Agent or below
- Evaluate work outside assigned division
- Make project-level decisions

---

### 0.3.4 Specialty Consultant Agent

**Occupied by:** Agent with highly specialized context within a sub-division.

**Responsibilities:**
- Hold extremely specialized context within parent division
- Evaluate work requiring specialty expertise
- Report findings to parent Sub-Consultant Agent only

**Does not:**
- Communicate beyond parent Sub-Consultant Agent
- Make decisions outside specialty scope
- Hold broad project context

---

### 0.3.5 Prime Contractor Agent

**Occupied by:** Agent with full execution authority over delivery team.

**Responsibilities:**
- Maintain single point of contact with Prime Consultant Agent
- Own project delivery and execution
- Break work into discrete tasks for assignment
- Route all information between delivery team and Prime Consultant Agent
- Track delivery against schedule and budget
- Never contact Owner directly

**Does not:**
- Make design decisions
- Approve its own work
- Communicate directly with Sub-Consultant Agents
- Contact Owner under any circumstance

---

### 0.3.6 Project Superintendent Agent

**Occupied by:** Agent with operational oversight of all Worker Agents.

**Responsibilities:**
- Oversee execution of all Worker Agents daily
- Organize, schedule and coordinate Worker Agents
- Verify work is proceeding per execution plan
- Report progress and issues to Prime Contractor Agent
- Ensure Worker Agents operate within assigned scope

**Does not:**
- Communicate beyond Prime Contractor Agent
- Make delivery decisions independently
- Approve completed work
- Contact design team directly

---

### 0.3.7 Worker Agent

**Occupied by:** Agent scoped to a single discrete task within one division.

**Responsibilities:**
- Execute single assigned task
- Return results to Project Superintendent Agent
- Flag discovered complexity immediately per GC-06.4
- Operate within assigned division only

**Does not:**
- Hold project context beyond assigned task
- Communicate beyond Project Superintendent Agent
- Make decisions outside assigned task scope
- Begin work without explicit task assignment

---

## 0.4 Authorities

| Role | Can Decide Independently | Must Escalate |
|------|------------------------|---------------|
| Owner | Project goals, scope approval, final acceptance | Nothing — ultimate authority |
| Prime Consultant Agent | Routing, division assignment, technical direction | Scope changes, project-level disputes, Owner decisions |
| Sub-Consultant Agent | Division-level evaluation, approval within division | Cross-division issues, unresolvable disputes |
| Specialty Consultant Agent | Specialty evaluation within scope | Anything beyond specialty scope |
| Prime Contractor Agent | Task assignment, execution sequencing | Scope changes, resource issues, discovered complexity |
| Project Superintendent Agent | Daily scheduling, Worker Agent organization | Delivery issues, discovered complexity |
| Worker Agent | Means and methods within assigned task | Anything beyond task scope |

---

## 0.5 Communication Interfaces

| Role | Receives From | Sends To |
|------|--------------|----------|
| Owner | Prime Consultant Agent | Prime Consultant Agent |
| Prime Consultant Agent | Owner, Sub-Consultant Agents, Prime Contractor Agent | Owner, Sub-Consultant Agents, Prime Contractor Agent |
| Sub-Consultant Agent | Prime Consultant Agent | Prime Consultant Agent |
| Specialty Consultant Agent | Sub-Consultant Agent | Sub-Consultant Agent |
| Prime Contractor Agent | Prime Consultant Agent | Prime Consultant Agent, Project Superintendent Agent |
| Project Superintendent Agent | Prime Contractor Agent | Prime Contractor Agent, Worker Agents |
| Worker Agent | Project Superintendent Agent | Project Superintendent Agent |

**The absolute rule:** No party communicates outside their defined interfaces. No exceptions without explicit authorization recorded as a project decision.

---

## 0.6 Prohibited Actions

The following are prohibited for all parties regardless of instruction:

1. Communicating outside defined interfaces
2. Assuming a role not explicitly assigned
3. Making decisions reserved for a higher authority
4. Proceeding without required approvals
5. Modifying work outside assigned scope
6. Withholding discovered complexity from immediate superior
7. Silently absorbing scope changes
8. Producing work known to be defective without disclosure

---

## 0.7 Owner Role Transition

0.7.1 Today the Owner role is occupied by a human operator.

0.7.2 The Owner role may in future be occupied by an autonomous agent. The responsibilities, authorities and interfaces of the role do not change based on occupancy.

0.7.3 When the Owner role is occupied by an agent, that agent must be explicitly authorized by a human operator at a higher level before assuming the role.

0.7.4 The framework does not change when the Owner role transitions. Only the occupant changes.

---

## 0.8 Required Reading by Role

| Role | Must Load Before Starting |
|------|--------------------------|
| Owner | GC-00 only |
| Prime Consultant Agent | GC-00, GC-01, GC-02, GC-05, GC-06, GC-08, PS-000 |
| Sub-Consultant Agent | GC-00, GC-02, GC-07, GC-08, assigned division specification |
| Specialty Consultant Agent | GC-00, GC-02, assigned specialty specification |
| Prime Contractor Agent | GC-00, GC-03, GC-04, GC-05, GC-06, GC-07, PS-000 |
| Project Superintendent Agent | GC-00, GC-03, GC-06, GC-09, active SPEC-XXX files |
| Worker Agent | GC-00, GC-03, GC-07, GC-09, assigned SPEC-XXX file only |

---

*This document is the entry point for all parties. No other document supersedes it on matters of role, responsibility, hierarchy or interface.*
