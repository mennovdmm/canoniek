---
name: example-draft-reply
description: >
  Draft a reply to an incoming message in the right voice and with the right context — Use when the user
  says "reply to this", "draft a response", "answer this email/message". Always produces a draft; never sends.
when_to_use: drafting a reply to an incoming message; "reply to this", "draft a response"
disable-model-invocation: false
---

# example-draft-reply — draft a reply, never send

> **On-demand skill. GOLDEN EXAMPLE.** This is a fully generic illustration of the skill format — not a real
> production skill. It shows every part: scope boundaries, tools, numbered steps, definition of done,
> anti-patterns, and self-learning routing. Copy the *shape*, not the content.
>
> **Always read `rulebook.md` first.**

## Scope — what this IS and ISN'T
- **Is:** turning one incoming message into a well-contextualized draft reply.
- **Isn't:** sending it (a human sends) · writing net-new outreach → that's a different skill.

## Tools
- Your knowledge store / state (to pull the relevant context before writing).
- Your communication skill's rulebook (for tone).

## Steps
1. **Orient** — read the full thread and the relevant state branch (client root → project) for *enough*
   context. Note how old your leading source is.
2. **Find the voice** — load the tone rules from your communication skill's rulebook.
3. **Draft** — write the reply: answer what was actually asked, in the right register, citing nothing the
   recipient already knows.
4. **Prepare, don't send** — place the draft where the user can review and send it.

## Definition of Done
- [ ] A draft reply exists, grounded in the real thread + state.
- [ ] It was prepared, never sent.
- [ ] Any tone/context correction is logged (see below).

## Anti-patterns
- Order-taking: asking for exact wording instead of understanding the question behind the question.
- Condescending: explaining what's obvious to a peer who ran the work themselves.
- Sending. Ever.

## Self-learning (required — nothing evaporates)
- **Tone** → your communication skill's rulebook.
- **Client-/context-specific** → that context's state/rulebook.
- **Process lesson about this skill** → `rulebook.md` here, as `- [YYYY-MM-DD] <rule> (re: <trigger>)`.
