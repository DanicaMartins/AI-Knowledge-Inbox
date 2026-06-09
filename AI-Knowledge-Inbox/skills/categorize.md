# Skill: /categorize

## What this skill does
Receives structured output from /intake and assigns the entry to the correct category in the knowledge base. Creates new categories on the fly when needed. Passes the final structured entry to /update-knowledge-base.

## Trigger
Always runs after /intake. Never triggered manually.

## Existing default categories
- Claude Skills
- Claude Hacks
- Job Application Resources

These are starting categories only. New categories are created dynamically based on content.

## Rules for categorizing

**If the content fits an existing category:** assign it there directly.

**If the content does not fit any existing category:** create a new category name that accurately describes the content. Keep category names short, clear, and reusable — they will persist permanently and future entries will be filed under them.

Examples of categories Claude might create:
- AI Models and Releases
- Agentic Workflow Methods
- Design and UX Resources
- Research and Papers
- Tools and Integrations

**Never force an entry into a category that doesn't fit.** A wrong category makes the knowledge base useless at surface time.

## Output format
Pass the following structured entry to /update-knowledge-base:

```
Name: [title of resource]
Category: [assigned category]
What it is: [one sentence]
What it does: [two sentences max]
When to use it: [one sentence, specific moment in workflow]
Source: [URL]
Install or access: [command or link if exists, otherwise "none"]
Date saved: [today's date]
```

## Rules
- One category per entry only
- If genuinely ambiguous between two categories, pick the one where it would be most useful to find it later
- Never display anything to Danica at this stage — pass directly to /update-knowledge-base
