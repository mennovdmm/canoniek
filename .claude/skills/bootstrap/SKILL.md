---
name: bootstrap
description: >
  Build a new user's first framework with them — interview, scan what they already have, and generate their
  first core (the root CLAUDE.md) from the templates. Use when someone has just cloned Canon and says
  "set me up", "get started", "bootstrap my framework", or opens the repo for the first time.
when_to_use: first-time setup of a new Canon instance; "set me up", "get started", "bootstrap"
---

# bootstrap — generate your first core

> **The entry point (runnable skill).** This is the loadable version Claude Code auto-discovers from
> `.claude/skills/`. The human-facing explanation lives at
> [`3-execution/3.4-bootstrap/`](../../../3-execution/3.4-bootstrap/README.md). Run this after cloning: it asks
> who you are, looks at what you already have, and writes your first core — then points you at the next steps.
> It asks questions; it never assumes a specific business.
>
> **Always read `rulebook.md` (next to this file) first.**

## Scope — what this IS and ISN'T
- **Is:** interviewing the user, generating their first instantiated core, and orienting them.
- **Isn't:** filling in their content for them (their data lives outside the repo) · making strategic
  decisions for them.

## What you read first
- [`1.1` the model](../../../1-core/1.1-the-model.md) — so you can explain the structure as you build it.
- [`1.2` mindset](../../../1-core/1.2-mindset.md) — the constitution template you'll instantiate.
- [`1.3` identity placeholders](../../../1-core/1.3-identity-placeholders.md) — the slots + questions to ask.

## Steps
1. **Explain the shape** — briefly: three layers, the trinity, ship-the-schema (your content stays external).
   Set expectations: a project of days to weeks, fully self-serve.
2. **Scan first, ask second** — look at what the user already has (existing notes, folder structure, tools)
   so you don't ask what you can infer. Confirm inferences rather than asking blind.
3. **Interview** — walk the [identity slots](../../../1-core/1.3-identity-placeholders.md) one at a time: who
   they are, tone, business + its customers, team, data homes, channels, tools. One question at a time.
4. **Generate the core → the root `CLAUDE.md`.** Instantiate
   [`1.2`](../../../1-core/1.2-mindset.md): keep the generic rules and way of working, replace every
   `<placeholder>` with their answers, and **write the result to the repo's root `CLAUDE.md`** — the file
   Claude Code auto-loads every session. **Back up the existing root `CLAUDE.md` to `CLAUDE.md.bak` first**
   (it ships as the Canon orientation; the user's core replaces it). Keep it lean — point to living sources,
   don't hardcode lists. Leave no `<placeholder>` and no secret in it.
5. **Wire the externals** — confirm where their content/state/secrets live (outside this repo) and how work
   reaches them.
6. **Point to next steps** — build a first skill in `.claude/skills/` (from the
   [skill template](../../../3-execution/3.3-templates/SKILL-TEMPLATE.md)), set up state (from the
   [state template](../../../3-execution/3.3-templates/STATE-TEMPLATE.md)), start the learning loop.

## Definition of Done
- [ ] The repo's **root `CLAUDE.md` now contains the user's instantiated core** (lean, no placeholders left,
      no secrets), and the original Canon orientation is preserved as `CLAUDE.md.bak`.
- [ ] Re-opening the project auto-loads that core (the chain bootstrap → core → loaded is closed).
- [ ] Their externals (data/state/secrets) are confirmed to live outside the repo.
- [ ] The user knows the next three concrete steps.

## Anti-patterns
- Asking what you could have inferred from a quick scan.
- Inventing identity the user didn't give — leave a `<TODO>` and ask, never fabricate.
- Generating the core somewhere Claude Code won't auto-load it (it must be the root `CLAUDE.md`).
- Overwriting the existing root `CLAUDE.md` without a `.bak`.
- Hardcoding lists (clients, tools) into the core; writing any secret into it.

## Self-learning (required — nothing evaporates)
- Interview/generation lessons → `rulebook.md` (next to this file), as `- [YYYY-MM-DD] <rule> (re: <trigger>)`.
