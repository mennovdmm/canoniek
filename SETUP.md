# Setup — getting started

Canon is a methodology handbook you read in order and instantiate, *and* a working Claude Code project that
runs. This page gets you from a fresh clone to a loaded, personal framework.

## The one hard rule
**Your data lives outside this repo.** This repo is *structure + logic* (versioned, shareable). Your actual
content — your business knowledge, files, project state, secrets — lives **externally** (your own storage,
databases, drive) and is wired in per user. That separation is what makes an instance disposable and
rebuildable, and it's what keeps anything private out of a public repo. See
[1.1 §8 ship-the-schema](1-core/1.1-the-model.md).

## Prerequisites — what you actually need to start
Canon runs entirely on **your own accounts** — no vendor lock-in, no hidden costs, nothing hosted by anyone
else. Be honest with yourself about these three: without them, you won't get off the ground.

1. **Claude Code on a capable plan.** Canon is built for [Claude Code](https://claude.com/claude-code) (it
   auto-loads the root `CLAUDE.md` and discovers skills under `.claude/skills/`). Real agentic work — standing
   agents, research, drafting — uses a lot of capacity, so a **substantial subscription is strongly
   recommended** (e.g. Claude Max); a minimal plan stalls quickly. It runs on your subscription — **no
   expensive API billing needed.**
2. **A workspace where your work lives.** The place your knowledge, files and mail already live —
   **Google Workspace, Microsoft 365, or similar.** Canon manages *your* content there; it stays yours and
   external to this repo.
3. **Git and a host (e.g. GitHub).** You clone Canon and version *your* instance. The structure is versioned;
   your data stays external (see the one hard rule below).

**Grows with you (not a barrier to starting):**
- **Tool connections (MCPs)** to your stack (drive, mail, calendar, CRM…). You do **not** wire these all up
  front — the bootstrap and the "there must be an MCP for this" reflex add them as real needs appear.
- **An always-on machine** if you want standing agents running around the clock. You can start on your laptop.

**Always:** **no secrets in version control** — credentials live in your environment, never in the repo.

## Run the bootstrap
1. Clone the repo and open the folder in Claude Code.
2. Opening it auto-loads [`CLAUDE.md`](CLAUDE.md) (the Canon orientation).
3. Say **"set me up"** / **"get started"**, or invoke the **`bootstrap`** skill
   ([`.claude/skills/bootstrap/`](.claude/skills/bootstrap/SKILL.md)).
4. It explains the shape, scans what you already have, interviews you through the
   [identity slots](1-core/1.3-identity-placeholders.md), and **writes your core into the root `CLAUDE.md`**
   (backing up the Canon orientation to `CLAUDE.md.bak`).
5. Re-open the project: Claude Code now auto-loads *your* core every session.

## How your instance hangs on the structure
- **Your core** = the root **`CLAUDE.md`** — your instantiated [`1.2` mindset](1-core/1.2-mindset.md)
  (auto-loaded, lean, points to living sources).
- **Your skills** = folders under **`.claude/skills/<name>/`** (`SKILL.md` + `rulebook.md`), built from the
  [skill template](3-execution/3.3-templates/SKILL-TEMPLATE.md). Claude Code auto-discovers them.
- **Your state** = files in your **external** store, in the
  [state format](3-execution/3.3-templates/STATE-TEMPLATE.md) (client root → project → subproject).
- **Your registry** = your one index of what you've built, in the
  [registry format](3-execution/3.3-templates/REGISTRY-TEMPLATE.md).
- **The numbered handbook** (`1-core/` … `3-execution/`) stays as your lazy-loaded reference — you read and
  check it; `.claude/` is the loaded layer. That split *is* the model.

## The non-negotiables
- **No secrets in version control** — environment only.
- **Everything reproducible from the schema** — content lives externally; an instance is disposable.
- **Non-destructive** — archive, don't delete; back up before overwrite (the bootstrap does this for your
  `CLAUDE.md`).
- **Nothing evaporates** — corrections become dated rulebook lines (the learning loop).
