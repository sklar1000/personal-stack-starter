---
id: canon-builders-guide
type: guide
status: draft
created: 2026-01-06
updated: 2026-01-06
objective: pc-business
related:
  - "[[Personal-Stack-Builders-Guide]]"
  - "[[Personal-Stack-Essay]]"
tags: [#writing, #personal-stack, #canon, #guide]
---

# Building Canons: Knowledge Systems That Compound

How to build structured knowledge bases that become sources of truth for your work.

---

## What Is a Canon?

A canon is not just a folder of notes. It's a **governed knowledge system** with:

- **Clear ownership** - Someone is responsible for what's true
- **Defined concepts** - An ontology of what terms mean
- **Status gates** - Draft → Candidate → Stable progression
- **Versioning** - Changes are tracked and intentional
- **Navigation** - Multiple entry points for different users
- **Integration** - Structured for both humans and AI/software

Think of it like this:

| Regular Folder | Canon |
|----------------|-------|
| "My notes on X" | "The authoritative reference for X" |
| Grows randomly | Grows intentionally |
| Anyone can edit | Changes are governed |
| Find stuff by searching | Navigate by role or task |
| Works for you | Works for you AND others |

**Canons compound.** Regular folders decay.

---

## When Do You Need a Canon?

You don't start with canons. You graduate to them.

**Signs you need a canon:**

- You keep explaining the same concepts to different people
- You have a methodology that others want to learn
- You're building something that needs a "single source of truth"
- Multiple people need to work from the same definitions
- You want AI/software to understand your frameworks
- You're teaching or coaching a discipline

**Don't create a canon for:**

- Personal notes you're still figuring out
- One-off projects
- Topics you're learning (not teaching)
- Anything that changes faster than you can govern it

**Rule of thumb**: If you've been working in a domain for 2+ years and have tested frameworks, you might be ready for a canon.

---

## The Canon Structure

A full canon has layers that progress from **foundations** to **applications** to **validation**:

```
[Domain]-Canon/
├── 00-overview/          What is this canon? Navigation.
├── 01-ontology/          Core concepts and definitions
├── 02-taxonomy/          Glossary, term relationships
├── 03-frameworks/        Mental models, design patterns
├── 04-processes/         Workflows, step-by-step methods
├── 05-templates/         Blank forms, organized by audience
├── 06-examples/          Worked examples, case studies
├── 07-governance/        Rules, change policies, decision memos
└── README.md             Entry point
```

**You don't need all folders on day one.** Start with what you have, add layers as patterns emerge.

---

## The Three Essential Layers

If you're starting a canon, focus on these three first:

### 1. Ontology (What things mean)

This is the foundation. Before frameworks, before templates, define your core concepts.

**Create `01-ontology/[domain]-ontology.md`:**

```markdown
# [Domain] Ontology

Core concepts and their definitions.

---

## Primitive Concepts

These are the atoms everything else builds from:

### [Concept 1]
**Definition**: [Clear, one-sentence definition]
**Not to be confused with**: [Common misunderstanding]
**Examples**: [2-3 concrete examples]

### [Concept 2]
**Definition**: ...
...

---

## Concept Relationships

How concepts connect:

- [Concept A] produces → [Concept B]
- [Concept C] requires → [Concept D]
- [Concept E] is a type of → [Concept F]

---

## The Transformation Ladder

How raw inputs become outputs in this domain:

```
[Raw Evidence]
    ↓ extraction
[Primitives/Claims]
    ↓ structuring
[Organized Records]
    ↓ synthesis
[Maps/Models]
    ↓ application
[Actions/Artifacts]
```
```

**Why this matters**: Without ontology, you'll use the same word to mean different things. Your frameworks will be inconsistent. Others won't be able to learn your system because terms are fuzzy.

### 2. Frameworks (How things work)

Once concepts are defined, document how they combine into mental models and processes.

**Create `03-frameworks/[framework-name].md`:**

```markdown
---
id: [domain]-[framework-slug]
status: draft | candidate | stable
version: 0.1.0
---

# [Framework Name]

**One-line**: [What this framework does in one sentence]

---

## When to Use

- [Situation 1]
- [Situation 2]

## When NOT to Use

- [Anti-pattern 1]
- [Anti-pattern 2]

---

## The Framework

[Visual or step-by-step explanation]

### Step 1: [Name]
[What to do]

### Step 2: [Name]
[What to do]

...

---

## Examples

### Example 1: [Title]
[Worked example showing framework in action]

---

## Common Mistakes

1. [Mistake] — [Why it happens] — [How to avoid]
2. ...

---

## Related

- [[other-framework]] - [How they connect]
- [[concept-from-ontology]] - [Foundation this builds on]
```

### 3. Governance (How things change)

This is what separates a canon from a pile of notes. Someone owns it. Changes are intentional.

**Create `07-governance/canon-rules.md`:**

```markdown
# [Domain] Canon Governance

Rules for maintaining this canon.

---

## Ownership

**Owner**: [Name]
**Reviewers**: [Names, if applicable]
**Update frequency**: [Weekly/Monthly/As needed]

---

## Status Definitions

### Draft
- Experimental, may change significantly
- Not ready for others to rely on
- Okay to use internally, not externally

### Candidate
- Tested but still refining
- Safe for limited use (one project, one cohort)
- Gathering feedback before stabilizing

### Stable
- Proven across multiple uses
- Safe for external sharing
- Changes require review

---

## Promotion Rules

**Draft → Candidate**:
- [ ] Used in at least one real context
- [ ] Documentation complete
- [ ] No known major issues

**Candidate → Stable**:
- [ ] Used in 3+ contexts
- [ ] Positive feedback documented
- [ ] Owner approves promotion

---

## Change Policy

**Minor changes** (typos, clarifications):
- Make directly, update version patch (0.1.0 → 0.1.1)

**Significant changes** (new sections, restructuring):
- Document in changelog
- Update minor version (0.1.0 → 0.2.0)

**Breaking changes** (renaming concepts, removing frameworks):
- Write decision memo explaining why
- Update major version (0.1.0 → 1.0.0)
- Notify anyone relying on the canon
```

---

## Building Your First Canon

### Phase 1: Audit What You Have

Before creating structure, inventory your existing knowledge:

1. **List your frameworks** - What mental models do you use repeatedly?
2. **List your templates** - What blank forms do you share with others?
3. **List your definitions** - What terms do you keep explaining?
4. **List your examples** - What case studies demonstrate your approach?

Don't create anything yet. Just list.

### Phase 2: Define the Ontology

Take your definitions and formalize them:

1. Create `01-ontology/[domain]-ontology.md`
2. Write a one-sentence definition for each core concept
3. Note what each concept is NOT (anti-confusions)
4. Map how concepts relate to each other

**Test**: Can you explain your domain using only these terms? If you need undefined words, add them.

### Phase 3: Document 2-3 Core Frameworks

Pick your most-used frameworks and document them:

1. Create `03-frameworks/` folder
2. Write up each framework with: when to use, steps, examples, common mistakes
3. Set status to "candidate" (you've tested these, but not formally governed)

**Test**: Could someone else use these frameworks without you explaining them?

### Phase 4: Create Templates for Others

If you have blank forms or worksheets:

1. Create `05-templates/` folder
2. Organize by who uses them (students, clients, team)
3. Add brief instructions to each template

### Phase 5: Add Governance

Now that you have content, add rules:

1. Create `07-governance/canon-rules.md`
2. Define owner, status levels, change policy
3. Review each artifact and set its status

### Phase 6: Create Navigation

Make it findable:

1. Write `README.md` at the canon root
2. Explain: What is this? Who is it for? How to navigate?
3. Link to the 5-7 most important artifacts

---

## The Status Gate System

This is what makes a canon trustworthy. Content earns its way to stable.

```
┌─────────────┐
│   Draft     │  "I'm figuring this out"
├─────────────┤
│   Used 1x   │  ← Test in real context
├─────────────┤
│ Candidate   │  "This works, still refining"
├─────────────┤
│   Used 3x+  │  ← Broader testing, evidence
├─────────────┤
│   Stable    │  "This is proven, rely on it"
└─────────────┘
```

**You can't skip levels.** Everything starts as draft.

**Stable means something.** Don't call things stable just because you like them. Stable means tested, documented, and you're committed to maintaining it.

---

## Connecting Canons

If you have multiple domains, they can connect:

**Philosophy flows down**:
```
[Your Core Beliefs Canon]
         ↓
   ┌─────┴─────┐
   ↓           ↓
[Domain A]  [Domain B]
```

Your core beliefs inform all domains. Domain canons implement those beliefs in specific contexts.

**Cross-domain patterns**:
- Teaching patterns might apply across domains
- Frameworks from one domain might inspire another
- But don't force connections—keep domains independent

**Rule**: Domain canons shouldn't import each other's content. They can reference, but each should stand alone.

---

## AI/Software Integration

If you want AI or software to use your canon:

### Frontmatter Metadata

Every artifact should have structured metadata:

```yaml
---
id: unique-slug
title: Human-Readable Title
status: draft | candidate | stable
version: 0.1.0
type: framework | process | template | concept
tags: [#domain/category]
---
```

### Export to JSON (Optional)

For software access, export to JSONL:

```json
{"id": "hammer-framework", "title": "HAMMER Loop", "status": "stable", "path": "03-frameworks/hammer.md"}
{"id": "3c-model", "title": "3C Model", "status": "stable", "path": "03-frameworks/3c-model.md"}
```

AI agents can read this index and navigate your canon.

### CLAUDE.md Reference

In your vault's CLAUDE.md, reference your canons:

```markdown
## Canons

- **[Domain]-Canon**: `03_Knowledge/[Domain]-Canon/`
  - Ontology: `01-ontology/[domain]-ontology.md`
  - Key frameworks: [list]
  - Status: [how mature]
```

Now AI knows where to find authoritative definitions.

---

## Common Mistakes

### 1. Building structure before content
Don't create 14 empty folders. Start with what you have. Add structure as content accumulates.

### 2. Calling everything stable
If everything is stable, nothing is. Be honest about what's tested vs. aspirational.

### 3. No governance
Without an owner and change rules, canons drift. Someone has to maintain truth.

### 4. Too many concepts in ontology
Start with 5-10 core concepts. You can always add more. Bloated ontology is unusable.

### 5. Forgetting who it's for
A canon for yourself looks different than one for students or clients. Know your audience.

### 6. Skipping examples
Frameworks without examples are theory. Add real, worked examples that show the framework in action.

---

## Canon vs. Personal Stack Relationship

Your Personal Stack is the operating system. Canons are applications that run on it.

```
Personal Stack (Operating System)
├── Actions, Contexts, Knowledge...
└── 03_Knowledge/
    ├── [Domain-A]-Canon/    ← Application
    ├── [Domain-B]-Canon/    ← Application
    └── Topics/              ← Loose reference (not canons)
```

**Not everything needs to be a canon.** Most of your Knowledge folder will be regular notes. Canons are for domains where you need:
- Governed truth
- Teachable frameworks
- Stable definitions others can rely on

---

## Quick Start Checklist

**Week 1-2: Foundation**
- [ ] Inventory existing frameworks, templates, definitions
- [ ] Create canon folder: `03_Knowledge/[Domain]-Canon/`
- [ ] Write `01-ontology/[domain]-ontology.md` with 5-10 core concepts
- [ ] Write `README.md` explaining what this canon is

**Week 3-4: Core Content**
- [ ] Document 2-3 core frameworks in `03-frameworks/`
- [ ] Move existing templates to `05-templates/`
- [ ] Add worked examples to `06-examples/`

**Week 5-6: Governance**
- [ ] Write `07-governance/canon-rules.md`
- [ ] Set status (draft/candidate/stable) for each artifact
- [ ] Add frontmatter metadata to all files

**Ongoing**:
- [ ] Test frameworks in real contexts
- [ ] Promote artifacts as evidence accumulates
- [ ] Update ontology when new concepts emerge
- [ ] Review quarterly: what's stable? what's drifted?

---

## Resources

- **Personal Stack Builders Guide**: How to build the operating system canons run on
- **Personal Stack Starter Kit**: Templates for basic structure
- **PC-Canon**: Example of a mature methodology canon

---

*Canons are how you package expertise. Build them when you're ready to be the authority on something.*
