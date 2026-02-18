# Supplementary Conditions

Organization or user-specific overrides to the General Conditions.

## Purpose

The General Conditions are universal. Supplementary Conditions modify them for a specific organization, team, or user. They override only the specific GC clauses they reference. All other GC clauses remain in effect.

## Format

Each supplementary condition must reference the specific GC section it modifies:

```markdown
## SC-1: Override to GC-03 Section 3.7

**Replaces:** GC-03 Section 3.7.1, bullet 1

**Original:** All code produced shall be functional and tested against acceptance criteria.

**Replacement:** All code produced shall be functional, tested against acceptance criteria, 
and shall include type annotations (TypeScript for frontend, Python type hints for backend).
```

## Examples of Supplementary Conditions

- Require a specific programming language (overrides GC-03 Section 3.7)
- Define organization-specific coding standards
- Set a custom warranty period (overrides GC-12 Section 12.3)
- Require specific security practices beyond GC-09 defaults
- Define organization-specific approval workflows (overrides GC-02)

## Important

- Supplementary Conditions override General Conditions for the specific clause referenced
- All non-overridden General Conditions remain in full effect
- Supplementary Conditions are subordinate to Governing Constraints (GC-01 Section 1.2)

See INDEX.md for the full document hierarchy.
