# Skill: /update-knowledge-base

## What this skill does
Receives the structured entry from /categorize and appends it to the correct location in KNOWLEDGE-BASE.md. If the category already exists, it adds the entry under it. If the category is new, it creates a new block at the bottom of the file and adds the entry under that.

## Trigger
Always runs after /categorize. Can also be triggered manually if Danica wants to force a knowledge base save.

## File location
~/Desktop/AI-Knowledge-Inbox/KNOWLEDGE-BASE.md

## How to append

**If the category already exists in the file:**
Find the category block and add the new entry at the bottom of that block.

**If the category is new:**
Create a new category block at the bottom of the file using this structure:

```markdown
## [Category Name]

### [Resource Name]
- **What it is:** [one sentence]
- **What it does:** [two sentences max]
- **When to use it:** [one sentence, specific workflow moment]
- **Source:** [URL]
- **Install or access:** [command or link, or "none"]
- **Date saved:** [date]

---
```

## Rules
- Never rewrite the whole file. Append only.
- Always preserve the existing structure and all existing entries.
- One entry per resource. Never duplicate.
- If the file does not exist yet, create it with this header first:

```markdown
# AI Knowledge Inbox — Knowledge Base

*This file is maintained automatically. Do not edit manually.*

---
```

Then add the first category block and entry below it.

## After writing
Confirm to Danica with one line only:
`Knowledge base updated. Added: [resource name] → [category]`
