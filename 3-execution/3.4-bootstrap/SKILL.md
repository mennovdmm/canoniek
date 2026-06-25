---
name: bootstrap
description: >
  Build a new user's first framework with them — interview, scan what they already have, and generate their
  first `core` from the templates. Use when someone has just cloned Canon and says "set me up", "get started",
  "bootstrap my framework", or opens the repo for the first time.
when_to_use: first-time setup of a new Canon instance; "set me up", "get started", "bootstrap"
---

# bootstrap — generate your first core

> **The entry point.** This is the "build your framework *with* you" experience. Run it in Claude Code after
> cloning the repo. It asks who you are, looks at what you already have, and writes your first `core` from the
> templates — then points you at the next steps. It asks questions; it never assumes a specific business.
>
> **Always read `rulebook.md` first.**

## Scope — what this IS and ISN'T
- **Is:** interviewing the user, generating their first instantiated `core`, and orienting them.
- **Isn't:** filling in their content for them (their data lives outside the repo) · making strategic
  decisions for them.

## What you read first
- [`1.1` the model](../../1-core/1.1-the-model.md) — so you can explain the structure as you build it.
- [`1.2` mindset](../../1-core/1.2-mindset.md) — the constitution template you'll instantiate.
- [`1.3` identity placeholders](../../1-core/1.3-identity-placeholders.md) — the slots + questions to ask.

## Steps
1. **Explain the shape** — briefly: three layers, the trinity, ship-the-schema (your content stays external).
   Set expectations: this is a project of days to weeks, fully self-serve.
2. **Scan first, ask second** — look at what the user already has (existing notes, folder structure, tools)
   so you don't ask what you can infer. Confirm inferences rather than asking blind.
3. **Interview** — walk the [identity slots](../../1-core/1.3-identity-placeholders.md) one at a time: who
   they are, tone, business + its customers, team, data homes, channels, tools. One question at a time;
   build on each answer.
4. **Generate the core** — write their first `core` by instantiating [`1.2`](../../1-core/1.2-mindset.md):
   keep the generic rules and way of working verbatim; replace every `<placeholder>` with their answers.
   Keep it lean — point to living sources, don't hardcode lists.
5. **Wire the externals** — confirm where their content/state/secrets live (outside this repo) and how work
   reaches them.
6. **Point to next steps** — build a first skill (from the [skill template](../3.3-templates/SKILL-TEMPLATE.md)),
   set up state (from the [state template](../3.3-templates/STATE-TEMPLATE.md)), start the learning loop.

## Definition of Done
- [ ] A filled-in `core` exists for the user (lean, no placeholders left, no secrets).
- [ ] Their externals (data/state/secrets) are confirmed to live outside the repo.
- [ ] The user knows the next three concrete steps.

## Anti-patterns
- Asking what you could have inferred from a quick scan.
- Inventing identity the user didn't give — leave a `<TODO>` and ask, never fabricate.
- Hardcoding lists (clients, tools) into the core — point to living sources.
- Writing any secret into the core or version control.

## Self-learning (required)
- Interview/generation lessons → `rulebook.md` here, as `- [YYYY-MM-DD] <rule> (re: <trigger>)`.
