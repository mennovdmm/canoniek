# Contributing to Canon

Canon is an open framework — a methodology you read in order and instantiate. Contributions are welcome, with
one guiding principle that shapes everything else.

## Ship the schema, not the data
This repo holds **structure, principles, and templates** — never anyone's filled-in content. So:
- Contribute to the **generic** layer: the model, the way of working, the formats, the templates, or a single
  anonymized golden example.
- **Never** contribute business-specific content, client data, names, internal URLs/IPs, or secrets. If a
  change only makes sense for your own setup, it belongs in *your* instance, not here.

## Ground it in real practice
Canon is extracted from a system that actually runs, not from aspiration. A contribution should reflect a
**real, working** pattern — something you have actually done — not a nice-sounding idea. If you can't point to
it working, it isn't ready.

## Keep it in shape
- English; keep the numbered structure (`1-core/` · `2-system/` · `3-execution/`).
- One thing per file; small, focused commits with clear messages.
- A doc that references another doc or template → make sure the target exists (no dead links).
- Keep each doc lean — detail goes in a linked support file, not inline.

## How to propose a change
1. Open an issue describing the pattern and why it's generic (it works beyond one business).
2. For a change, open a pull request — small and self-contained.
3. Expect review on two axes: is it **generic** (no specifics), and is it **grounded** (it really works)?

## What does not belong here
- Filled-in cores, real skills/processes/rulebooks, memories, or registries with real content.
- Secrets, credentials, names, internal hostnames/IPs.
- Aspirational features no one has actually run.

Keep the schema clean and real, and Canon stays useful for everyone.

This project follows its [Code of Conduct](CODE_OF_CONDUCT.md).
