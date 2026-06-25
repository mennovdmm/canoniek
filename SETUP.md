# Setup — getting started

> **Stub — to be built (Tier 1).** Source: derived from the model's core principle *"ship the schema, not
> the data"* (MODEL §8) + the way-of-working in `1.2-mindset.md`. Build per the extraction rules.

## The one hard rule
**Your data lives outside this repo.** This repo is *structure + logic* (versioned, shareable). Your actual
content — your business knowledge, client files, project state, secrets — lives **externally** (your own
storage, databases, drive) and is wired in per user. That separation is what makes an instance disposable
and rebuildable, and it's what keeps anything private out of a public repo.

## What goes here (later)
- Prerequisites (Claude Code, a place for your external data).
- How to run the bootstrap interview.
- How your filled-in `core`, skills and state connect to this structure.
- The non-negotiables: no secrets in version control; everything reproducible from the schema.
