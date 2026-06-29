---
name: example-inbox-router
description: >
  Read incoming messages, decide which client/topic each belongs to, and drop it into the right agent's
  inbox — draft-first, never sending. Runs automatically on a schedule/event (no human trigger) → a PROCESS.
when_to_use: automatic — a runner starts this; it is not called by a human
disable-model-invocation: true
---

# example-inbox-router — route incoming work to the right agent

> **Process. GOLDEN EXAMPLE.** A fully generic illustration of the *process* format — not a real production
> process. It shows the one thing that makes a process a process (a runner, no human) plus the Definition of
> Done extras a process needs: a health-check and a ping-on-failure.
>
> **Always read `rulebook.md` first.**

## Skill or process? (the deciding test)
A runner/schedule/event starts this **without a human** → it's a **process**. (If a human had to call it, it
would be a skill.) No runner = no process.

## Scope — what this IS and ISN'T
- **Is:** classifying each incoming item by client/topic and delivering it to the right agent's inbox.
- **Isn't:** answering the message (that's the receiving agent's job, via a draft) · sending anything.

## How it runs
- **Runner:** a schedule or an event (a new message arrives) triggers it — no human.
- **Action:** for each new item → determine client/topic → append it to that agent's inbox → nudge the agent.
- **Draft-first:** it never replies or sends; it only *delivers* work.

## Routing discipline (two rules that prevent cross-contamination)
- **Route only to registered, canonical agents — never to ad-hoc/scratch sessions.** A distributor that can
  deliver to a throwaway session will eventually deliver a client's work into the wrong, unmanaged place.
  Resolve the target against the agent registry; if there's no registered home, hold it, don't improvise.
- **Watch for case-insensitive filename collisions** in per-session state/inbox files. On a case-insensitive
  filesystem, two sessions whose names differ only in case share the *same* file → one agent's inbox bleeds
  into another's. Normalize names; treat a case-only difference as the same target, not two.

## Definition of Done (process extras)
- [ ] Runner/schedule configured.
- [ ] **Health-check** — a check that confirms the runner ran and processed items (a stale runner = a flag).
- [ ] **Ping-on-failure** — on error it routes to a maintainer/queue that can act (never only to the user).
- [ ] Registry entry + a last-run log.

## Anti-patterns
- Letting it answer or send (it routes; it doesn't reply).
- No health-check → silent failure, the worst kind.

## Self-learning (required)
- Routing/classification mistakes → `rulebook.md` here, as `- [YYYY-MM-DD] <rule> (re: <trigger>)`.
