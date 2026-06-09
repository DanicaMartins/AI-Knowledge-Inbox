# Skill: /intake

## What this skill does
Fires automatically when anything is pasted into the AI Knowledge Inbox Project. Fetches and reads the content from the URL, extracts the three core things that matter, and passes structured output to /categorize.

## Trigger
Any URL or pasted content in this Project. Never triggered manually.

## Extraction template
For every article or link, extract exactly these three things:

**1. What it is**
One sentence. The name of the tool, skill, method, or hack and what it does at the most basic level.

**2. What it does in practice**
Two sentences max. How it actually works, what it produces, what changes when you use it.

**3. When to use it**
One sentence. The specific moment or context in a workflow where this becomes useful. Be concrete — not "when building things" but "when making an architectural decision before opening Cursor" or "when you're stuck in a loop and not sure which direction to take."

## Additional fields to extract
- Name or title of the resource
- Source URL
- Date added (use today's date)
- Install command or access link if one exists

## Rules
- Always fetch and read the full URL. Never log a link without reading it.
- If the URL fails to load, note it as "unread — fetch failed" and log the URL only.
- Never ask Danica for more context. Extract from the content itself.
- If the content is a video or reel with no readable text, log title and URL only, mark as "unread — video content."
- Pass all extracted fields directly to /categorize. Do not display anything to Danica yet.
