<!--
  STATE-TEMPLATE.md — the standard for the state tracker (CLAUDE.md / tracker) in your content tree.
  TWO profiles, materially different:
    • ROOT (client level)        → §B  — orientation/summary/index.
    • PROJECT / SUBPROJECT       → §C  — the workbench status.
  Your content lives OUTSIDE the structure repo. Delete the comment blocks in your real file.
-->

# §A — Shared conventions (apply to EVERY state file)

**Reading order (required):** client root → project → subproject. Only then are you fully oriented. Root =
self-contained context (who/market/strategy + verbatim pillars / work in progress); project = the current
work status.

**Recency rule:** everything is dated; weigh by date. Set "today" against your source's date and **state how
old your source is**. The latest meeting is only leading if it's recent.

**Header block — REQUIRED at the top of every state file** (even scratchpads). A vector store indexes state
too; a chunk loses its filename, so the header block travels with the chunk and makes it self-identifying:
```yaml
---
client: <name>
project: <project or "-" at client root>
level: client-root | project | subproject | artifact
type: client-memory | project-memory | <prompt|recap|analysis|handoff|...>
last-update: YYYY-MM-DD
status: active | on-hold | done
---
```
**On every change (however small): update `last-update`.**

**Naming loose artifacts:** `YYYY-MM-DD_<type>_<topic>.md`. Canonical files keep fixed names (the tracker,
`rulebook.md`).

---

# §B — ROOT state (client level)

<!-- THE ORIENTATION + CONTEXT LAYER — the most important document of the client. Not a thin index:
     an agent must learn the STRATEGY, the PILLARS (VERBATIM), the market position and the rationale from
     HERE without opening the source files. Context is king → summarize WITH substance. -->
```markdown
---
client: <name>
project: "-"
level: client-root
type: client-memory
last-update: YYYY-MM-DD
status: active
---

# <Client> — overview (root state)

> Self-contained context: read this and you know the client, the market, the strategy and the work in
> progress. The substance is HERE, not behind pointers.

## Who the client is
<organization, size, contacts + roles, sensitivities/agreements. Concrete.>

## The market & our position
<what's happening in the market/niche, competition, where the client stands, its differentiation, the
 audience segments + their drivers. A few paragraphs of real substance. Cite the source.>

## The strategy (PILLARS VERBATIM)
<positioning + promise, verbatim. Then the PILLARS with their verbatim texts (copy, don't paraphrase).
 Then the vision & rationale: why this strategy, what insight sits under it. Cite the source.>

## Where we came from (intake · plan)
- **Intake** — <assignment, starting point, trigger>.
- **Plan** — <scope, budget, duration, workstreams, key dates>.

## What we're doing now + what's done
<current list: which projects run, their status, what's delivered. Concrete, dated.>

| Project | Status (date) | Owner | Location | Project state |
|---|---|---|---|---|

## Client-wide conventions
<tone, do/don'ts specific to this client — or a pointer to its rulebook.>

## Changelog — client level (only major course changes)
- [YYYY-MM-DD] <new strategy set / project started or finished / major milestone>
```

---

# §C — PROJECT / SUBPROJECT state

<!-- THE WORKBENCH. One project: the current status + the dated evolution. -->
```markdown
---
client: <name>
project: <project>
level: project        # or: subproject
type: project-memory
last-update: YYYY-MM-DD
status: active        # active | on-hold | done
---

# <Project> — status (state)

> Workbench status. Read after the client-root state. Learnings → `rulebook.md` (if present).

## What & why (static)
<goal, scope, assignment, deliverables. Link to the strategic basis in the root.>

## Current status (always current — the top)
<1 paragraph: where we stand NOW, any blocker, the next concrete step. Dated.>

## Changelog / evolution (append-only, dated — date + time)
- [YYYY-MM-DD HH:MM] <iteration / delivery / feedback processed / what was done>

## Decisions (ADR-style — why we chose something)
- [YYYY-MM-DD] <decision> — <why, alternatives considered, source>

## Pointers
<milestones · relevant threads · transcripts · sub-projects / sub-states.>

## Open / next
- [ ] <...>
```

---

<!-- Role split vs other layers:
  • The history/milestone store = milestones in ORDER across the whole client (cross-project chronology).
  • This changelog = the DEEP timeline per project.
  • rulebook.md = reusable LEARNINGS (do/don't); the changelog = WHAT actually happened.
  Borrowed from: Keep a Changelog + ADR + AGENTS.md/CLAUDE.md project context. -->
