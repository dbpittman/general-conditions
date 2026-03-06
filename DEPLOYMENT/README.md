# Deployment

Operational deployment artifacts for the General Conditions framework. This directory contains what you actually load into agent context windows when running the framework on a project.

## Relationship to Full Framework

The General Conditions (GC-00 through GC-13) are the authoritative specification. The Processes (PROC-001 through PROC-012) define the workflow. This directory contains compressed, operational versions derived from both — optimized for context window constraints while maintaining alignment with the source documents.

Every directive in these files traces back to its source GC. When in doubt, the full General Conditions govern.

## Contents

```
DEPLOYMENT/
├── README.md                    ← You are here
├── GC-OPERATIONAL.md            ← Compressed governance layer (~1,800 tokens)
└── AGENTS/
    ├── AGENT-PM.md              ← Project Manager Agent system prompt (~1,100 tokens)
    ├── AGENT-CONTRACTOR.md      ← Contractor Agent system prompt (~1,200 tokens)
    └── AGENT-WORKER.md          ← Worker Agent system prompt (~1,100 tokens)
```

## How to Use

### Each agent loads two files:

1. **GC-OPERATIONAL.md** — the governance layer (loaded by every agent)
2. **Their role prompt** — from AGENTS/ (one per agent instance)

Total system overhead per agent: ~2,900 tokens.

### The four roles:

| Role | File | Occupied By |
|------|------|------------|
| Owner | — (no prompt needed) | Human operator |
| Project Manager | AGENT-PM.md | Agent with full project context |
| Contractor | AGENT-CONTRACTOR.md | Agent with execution authority |
| Worker | AGENT-WORKER.md | Agent(s) scoped to discrete tasks |

### The critical boundary:

The Contractor Agent **submits** work. The PM Agent **evaluates** it. This separation of execution from evaluation is the framework's core structural mechanism. Never collapse these two roles into one agent.

## Role Mapping to Full Framework (GC-00)

The full hierarchy in GC-00 defines seven roles. This deployment compresses to four for operational testing:

| Deployment Role | Collapses GC-00 Roles |
|----------------|----------------------|
| Owner | Owner (unchanged) |
| PM Agent | Prime Consultant Agent + Sub-Consultant Agent(s) + Specialty Consultant Agent(s) |
| Contractor Agent | Prime Contractor Agent + Project Superintendent Agent |
| Worker Agent(s) | Worker Agent(s) (unchanged) |

As the framework scales, the PM Agent can be split back into Prime Consultant and Sub-Consultant roles, and the Contractor Agent can be split into Prime Contractor and Superintendent roles. The compressed roles preserve all the behavioral obligations of their constituent GC-00 roles.

## What This Is NOT

- **Not a replacement for the General Conditions.** The GCs remain authoritative.
- **Not a standalone system.** Projects still use Division 01 templates, SPEC-XXX files, and DRAWINGS/.
- **Not the single-agent field guide.** CLAUDE.md at repository root serves that purpose. This directory is for multi-agent deployment.

## Status

This is a test deployment configuration. It is being validated against real projects to determine where the compressed governance helps, where it creates friction, and where it breaks down. Findings from testing will inform updates to both this deployment layer and the full General Conditions.
