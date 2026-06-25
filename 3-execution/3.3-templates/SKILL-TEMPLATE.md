<!--
  SKILL-TEMPLATE.md — copy this to .claude/skills/<skill-name>/SKILL.md and fill it in.
  Skills MUST live under .claude/skills/<name>/ for Claude Code to auto-discover them; the numbered
  3-execution/ docs are the human reference, not the loaded location.
  Sister template: RULEBOOK-TEMPLATE.md (every skill also gets a rulebook.md, next to SKILL.md).
  Delete these comment blocks in your real skill; they're guidance only.

  HARD STANDARD:
  - ALWAYS YAML frontmatter.
  - `description` = what Claude auto-loads the skill on. Lead with the action + say WHEN.
    Put trigger words you'd actually say. description + when_to_use together < 1536 chars.
  - SKILL.md < 500 lines. Detail/examples/scripts → separate support files (progressive disclosure):
    they load only when opened, so they're cheap. Link to them with relative links.
  - State WHAT to do, not why/how at length. Every line stays in context = a recurring cost.
-->
---
name: <skill-name>            # = folder name, lowercase-with-hyphens
description: >
  <1 sentence: what the skill does> — Use when <concrete trigger: what the user says/asks,
  e.g. "make X", "recap [topic]", "handle this message">. <optional 1 sentence of scope>.
when_to_use: <short trigger summary in one sentence — separate from description, counts toward the 1536>
# Optional (only if relevant — otherwise omit):
# allowed-tools: Read, Bash(git status), ...     # pre-approved tools during the skill
# disable-model-invocation: true                  # for side effects: only you start it (deploy/send)
---

# <skill-name> — <goal in one line>

> **On-demand skill.** Trigger: <when someone invokes this>. Goal: <what you deliver>.
> **Always read `rulebook.md` first** — it holds the boundaries + accumulated learnings.

## Scope — what this IS and ISN'T
- **Is:** <the core of this skill>.
- **Isn't:** <what doesn't belong here> → use `.claude/skills/<other-skill>/` instead.
<!-- Skills bound each other explicitly (relative links) so no overlap/duplication arises. -->

## Tools
- <MCPs / CLIs / scripts this skill uses, briefly. Omit the trivial.>

## Steps
1. **<step>** — <what + with which tool>.
2. **<step>** — <…>.
3. **<step>** — <…>.
<!-- Numbered, concrete, executable. Run through to a reviewable deliverable; don't stop per step.
     Heavy detail/examples → a support file (progressive disclosure), not here. -->

## Definition of Done
- [ ] <objectively checkable result>.
- [ ] <e.g. draft prepared, never sent yourself>.
- [ ] Learnings logged (see below).

## Anti-patterns
- <typical mistake 1 — what you do NOT do>.
- <typical mistake 2>.

## Self-learning (required — nothing evaporates)
Capture every correction or lesson immediately; the chat is not memory, the rulebook is. Routing:
- **Style/tone** (messages) → your communication skill's rulebook.
- **Client-/context-specific** → that context's state/rulebook.
- **Process lesson about this skill** → `rulebook.md` next to this file, as a dated bullet
  `- [YYYY-MM-DD] <rule> (re: <trigger>)`.
