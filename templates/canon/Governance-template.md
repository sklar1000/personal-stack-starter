---
id: [domain]-canon-governance
title: "[Domain] Canon Governance"
status: draft
version: 0.1.0
type: governance
updated: [DATE]
---

# [Domain] Canon Governance

Rules for maintaining this canon as a trusted source of truth.

---

## Ownership

**Owner**: [Name]
**Role**: [What the owner is responsible for]
**Reviewers**: [Names of people who can review changes, if any]

**Contact**: [How to reach owner with questions or proposals]

---

## Purpose of This Canon

**What it codifies**: [The domain knowledge this canon contains]
**Who relies on it**: [Students, clients, team, software]
**Why governance matters**: [What happens if it drifts or becomes unreliable]

---

## Status Definitions

### Draft
- Experimental, actively changing
- Not ready for others to rely on
- Use internally only
- May be significantly revised or removed

### Candidate
- Tested in at least one real context
- Mostly stable, minor refinements expected
- Safe for limited external use
- Gathering feedback before promotion

### Stable
- Proven across multiple contexts
- Complete documentation
- Safe for external sharing and reliance
- Changes require formal review

---

## Promotion Rules

### Draft → Candidate

Requirements:
- [ ] Used in at least 1 real context (not just theory)
- [ ] Core documentation complete
- [ ] No known major issues or contradictions
- [ ] Owner approves promotion

### Candidate → Stable

Requirements:
- [ ] Used in 3+ different contexts
- [ ] Positive feedback documented
- [ ] Edge cases and limitations documented
- [ ] Examples and anti-patterns included
- [ ] Owner approves promotion

---

## Change Policies

### Minor Changes (Patch: 0.1.0 → 0.1.1)
- Typos, clarifications, formatting
- No meaning change
- Can be made directly by owner
- No notification required

### Significant Changes (Minor: 0.1.0 → 0.2.0)
- New sections, expanded content
- Restructuring that doesn't change meaning
- Requires brief changelog entry
- Notify regular users if relevant

### Breaking Changes (Major: 0.1.0 → 1.0.0)
- Renaming core concepts
- Removing or significantly changing frameworks
- Contradicting previous stable content
- **Requires**: Decision memo documenting why
- **Requires**: Owner approval
- **Requires**: Notification to all relying users/systems

---

## Decision Memo Format

For breaking changes, create a decision memo:

```markdown
# Decision: [What's changing]

**Date**: [Date]
**Author**: [Name]
**Status**: Proposed | Approved | Rejected

## Context
[Why is this change being considered?]

## Decision
[What specifically is changing?]

## Consequences
[What breaks? What improves? Who needs to update?]

## Alternatives Considered
[What other options were evaluated?]
```

---

## Quality Standards

All canon artifacts should have:

**Required**:
- [ ] Frontmatter with id, status, version
- [ ] Clear one-line summary
- [ ] Updated date

**Recommended** (for candidate+):
- [ ] When to use / when not to use
- [ ] At least one worked example
- [ ] Common mistakes section
- [ ] Related links

**Required for Stable**:
- [ ] All of the above
- [ ] Anti-confusions documented
- [ ] Tested in 3+ contexts

---

## Review Schedule

**Weekly**: Owner scans for drift or outdated content
**Monthly**: Review status of all draft artifacts - promote or remove?
**Quarterly**: Full canon review - is structure still serving users?

---

## Archiving Policy

**When to archive**:
- Framework superseded by better approach
- Concept no longer relevant to domain
- Content hasn't been used in 6+ months

**How to archive**:
1. Move to `_archive/` subfolder
2. Add frontmatter: `status: archived`, `archived_date: [DATE]`
3. Note reason for archiving
4. Don't delete - future reference may be valuable

---

## Who Can Change What

| Role | Can Change | Requires Approval |
|------|------------|-------------------|
| Owner | Anything | No (but document major changes) |
| Reviewer | Draft artifacts | Owner approval for candidate+ |
| User | Nothing directly | Submit proposal to owner |

---

## Versioning

This canon uses semantic versioning:

- **MAJOR** (1.0.0): Breaking changes to core concepts
- **MINOR** (0.1.0): New content, non-breaking changes
- **PATCH** (0.1.1): Fixes, clarifications, typos

Current version: **0.1.0**

---

## Related

- [[../README|Canon README]] - What this canon contains
- [[../01-ontology/[domain]-ontology|Ontology]] - Core concepts
- Decision memos stored in this folder

---

*Governance is what separates a canon from a pile of notes. Maintain it.*
