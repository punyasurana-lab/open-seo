# Project management tool: design reference

`ai-intel-platform-standalone.html` is the design prototype for the AI Intel
Platform, the project and prospect management tool we are building around
OpenSEO. It is a design reference, not shipped code: nothing in `src/` imports
it, and it is not served by the app.

## How to view it

Open the file in a browser. It is a single self-contained "bundled page"
export (about 1 MB): the page template, fonts and assets are embedded, so it
works offline and needs no server.

```sh
open docs/maintainers/project-management-tool-reference/ai-intel-platform-standalone.html
```

## What it shows

Screens and flows visible in the prototype:

- **Project switcher** and a **New prospect audit** form: brand or
  organisation name, website URL, sitemap URL, city, sector, programmes /
  products / services, known competitors, deal size, win probability and pitch
  date.
- **Prospect pipeline**: status, package and outcome per prospect (in
  discussion, converted, lost), win rate and loss reasons, export, and a
  **View report** / **Preview draft report** action.
- **AI Visibility Snapshot**: engine-by-engine table (mentions, average
  position, owned citations, share of mentions), recommendation by engine,
  and a "The Gap" view of what AI says about the brand versus what the
  website says.
- **Citation share by source** and cited URLs, with a copy-URL action.
- **Prompt Scoreboard**: per prompt, its journey stage, tags, whether the
  brand is mentioned, position, whether an owned page is cited, facts missing,
  and the opportunity, with a **Create task** action.
- **Coverage by journey stage**, **How AI describes you**, and **Who writes
  your story**.

## How it maps to OpenSEO

The prototype's data comes from capabilities OpenSEO already has: AI
visibility prompt tracking (DataForSEO LLM responses), site audits, project
context, reports and competitor research. Treat the prototype as the target
UX; check the OpenSEO MCP tools and the `docs/maintainers/` specs for what the
backend provides today before assuming a screen is buildable as drawn.

## Keeping this folder useful

- Replace the HTML with the newer export when the design changes, and note
  what changed in the commit message.
- Put design decisions and open questions in this folder, not in chat or
  tickets, so the repo holds the full context for the tool.
