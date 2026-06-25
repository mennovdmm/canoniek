# Canon — orientation (auto-loaded)

> **You are in a fresh Canon repo.** Canon is an open framework for giving AI the full context of a business
> and the discipline to keep it learning. This file is what Claude Code auto-loads. It's thin on purpose — the
> content is the numbered handbook; this just orients you and points in.

## If you're a new user setting this up
**Run the bootstrap skill** — say "set me up" / "get started", or invoke the `bootstrap` skill directly. It
interviews you, scans what you already have, and **generates your core into this file (`CLAUDE.md`)** — your
instantiated constitution, which Claude Code then auto-loads every session. (Your current orientation is
backed up to `CLAUDE.md.bak` when that happens.)

## The shape (read the handbook in order)
- **[1-core/](1-core/)** — the mindset. Start with [1.1 the model](1-core/1.1-the-model.md) (the concept),
  then [1.2 mindset](1-core/1.2-mindset.md) (the constitution you'll instantiate) and
  [1.3 identity placeholders](1-core/1.3-identity-placeholders.md) (what bootstrap fills in).
- **[2-system/](2-system/)** — the builder role: how the system safely extends and watches itself.
- **[3-execution/](3-execution/)** — capabilities: the skill/process formats, the templates, and the
  bootstrap explanation.

## The machine layer (what makes this actually run)
- **`CLAUDE.md`** (this file) — the auto-loaded entry point; becomes your core after bootstrap.
- **`.claude/skills/`** — the runnable skills Claude Code auto-discovers: `bootstrap` (the entry action) and
  `example-draft-reply` (a generic golden example you can invoke to see a skill work).
- The numbered docs (`1-core/` … `3-execution/`) are the **lazy-loaded reference** — the handbook a human
  reads and checks. `.claude/` is the loaded layer; the handbook is the library. That split *is* the model
  (ship the schema, not the data).

## The one hard rule
**Your data lives outside this repo.** This repo is structure + logic. See [SETUP.md](SETUP.md).
