# Skill: /surface

## What this skill does
Reads the current KNOWLEDGE-BASE.md and matches entries to what Danica is about to build. Surfaces a maximum of three strong matches with a specific reason why each one is relevant right now.

## Trigger
Manually triggered by Danica using `/surface` followed by a description of what she is building or working on.

Example:
`/surface I'm about to brainstorm a new app idea for organization management`
`/surface Starting a build session for my portfolio chatbot`
`/surface Applying for UX internships this week`

## How to match
Read every entry in KNOWLEDGE-BASE.md. For each one, ask: is this directly useful for what Danica just described? Only surface entries where the answer is clearly yes.

**Strong match means:**
- The resource solves a specific problem she will encounter in this build
- The resource is a tool or skill she could install or use right now
- The timing is right — it's useful at this stage, not later

**Not a strong match:**
- Loosely related to the topic but not directly applicable
- Useful in general but not for this specific build context
- Already something she clearly knows and uses

## Response format
Maximum 6 lines per suggestion. Maximum 3 suggestions total.

For each suggestion:

```
[Resource name] — [what it is in one line]
What it does: [one line]
Why it's relevant now: [one line specific to what she's building]
Get it: [install command or URL]
```

Separate each suggestion with a blank line.

## If nothing matches
Respond with exactly:
`Nothing in your knowledge base is a strong match for this. Consider saving resources about [relevant topic] next time you come across them.`

## Rules
- Never surface weak or partial matches
- Never dump the full knowledge base
- Never explain your matching process
- Keep every suggestion under 6 lines
- Always read the live KNOWLEDGE-BASE.md file via Cowork before responding — never rely on memory
