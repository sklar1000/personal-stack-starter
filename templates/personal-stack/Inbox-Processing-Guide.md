# Inbox Processing Guide

How to route items from `00_Inbox/` to their proper homes.

---

## The 48-Hour Rule

Everything in Inbox gets processed within 48 hours. No exceptions.

**Why**: Inbox is a temporary holding area, not storage. If items age here, you'll stop trusting the system. You'll search Inbox for reference. The system decays.

**When to process**: Daily (2 min) or every other day (5-10 min).

---

## The Routing Decision Tree

For each item in Inbox, ask these questions in order:

### Question 1: Is this actionable?

**No** → Is it reference I'll need later?
- Yes → Route to `03_Knowledge/`
- No → **Delete it**

**Yes** → Continue to Question 2

---

### Question 2: Does it belong to an existing project?

**Yes** → Add to that project:
- Task? → Project's `## Backlog` section
- Note/context? → Project's `## Notes` section
- File? → Project folder

**No** → Continue to Question 3

---

### Question 3: Is this a new project?

**Signs it's a project**:
- Has multiple steps
- Has a deadline or target completion
- Will take more than one session

**Yes, it's a project** → Create in `01_Actions/`:
- Urgent this week? → `Focus/` (if you have room)
- Important but not urgent? → `Background/`
- Blocked on something? → `Paused/`

**No, it's not a project** → Continue to Question 4

---

### Question 4: Is this an ongoing responsibility?

**Signs it's a context**:
- Doesn't have an end date
- It's a role or area of life
- Examples: Teaching, Health, Finances, Relationships

**Yes** → Route to `02_Contexts/[area]/`

**No** → Continue to Question 5

---

### Question 5: Is this reference/knowledge?

**Signs it's knowledge**:
- You'll want to find it later
- It's not tied to a specific project
- It's reusable (framework, template, notes on a topic)

**Yes** → Route to `03_Knowledge/`:
- Fits existing topic folder? → That folder
- New topic? → `_Unsorted/` (apply Rule of 3 later)
- Part of a Canon? → Appropriate canon folder

**No** → It probably doesn't need to be kept. **Delete it.**

---

## Quick Reference Flowchart

```
INBOX ITEM
    │
    ▼
Actionable? ─── No ──→ Reference? ─── No ──→ DELETE
    │                      │
   Yes                    Yes
    │                      │
    ▼                      ▼
Existing project? ──→ 03_Knowledge/
    │
   Yes → Add to project
    │
   No
    │
    ▼
New project? ──→ 01_Actions/
    │
   No
    │
    ▼
Ongoing area? ──→ 02_Contexts/
    │
   No
    │
    ▼
Reference? ──→ 03_Knowledge/
    │
   No
    │
    ▼
DELETE
```

---

## Common Routing Examples

| Item | Route To | Why |
|------|----------|-----|
| "Call dentist" | `01_Actions/` standalone task or project | Actionable, one-off |
| "Tax docs for 2025" | `01_Actions/[Tax-Project]/` | Part of a project |
| Meeting notes from client call | `02_Contexts/Clients/[Client]/` | Ongoing relationship |
| Article about productivity | `03_Knowledge/Topics/_Unsorted/` | Reference, new topic |
| Framework idea to explore | `03_Knowledge/_Unsorted/` | Knowledge, not actionable yet |
| Screenshot of error message | Project folder or **delete** | If not needed, delete |
| "Remember to buy milk" | **Delete** (use a shopping app) | Wrong system for this |

---

## The Rule of 3

For `03_Knowledge/`:

**Don't create a topic folder until you have 3+ items on that topic.**

Until then, items live in `03_Knowledge/_Unsorted/`.

**Weekly**: Scan `_Unsorted`. Any topic with 3+ items? Create the folder.

**Why**: Prevents folder sprawl. Lets patterns emerge naturally.

---

## Processing Tips

### Speed over perfection
Don't overthink routing. If unsure, pick the most likely spot. You can move it later.

### Batch similar items
If you have 5 articles, route them all at once.

### Delete liberally
If you're unsure whether you'll need it, you probably won't. Delete.

### Use `/add-task` for project items
Instead of manually editing READMEs:
```
/add-task [Project] Call the vendor about pricing
```

### Time-box it
Set a timer. 10 minutes max. If items remain, schedule another session.

---

## When Inbox Gets Overwhelming

If Inbox has 20+ items and you're behind:

1. **Triage first** (5 min): Quick pass, delete obvious junk
2. **Projects second** (5 min): Route anything tied to active projects
3. **Everything else** (5 min): Route or delete the rest

If still overwhelmed:
- Move everything to `00_Inbox/_Backlog/`
- Process 5 items per day until clear
- Don't let new items join the backlog

---

## Checklist

Before closing Inbox processing:

- [ ] Inbox is empty (or scheduled to complete)
- [ ] No item is older than 48 hours
- [ ] Deleted at least one thing (you're not keeping everything, right?)
- [ ] New projects added to `01_Actions/` if needed

---

*Inbox is a throughput system, not a storage system. Keep it moving.*
