# Feature Lab workspace guidance

This repository is migrating the Feature Lab Spec Sheets process to Codex. Until the cutover described in `MIGRATION.md` is complete, open the live Project Settings Google Doc and the task-specific linked instruction doc before Feature Lab work. Do not use `migration/source-snapshots/` as current instructions.

For a new meeting transcript, use `.agents/skills/feature-lab-ingestion/SKILL.md`. Google Drive is the home for transcripts, Pre-Specs, agendas that are saved, and spec sheets. Preserve the current review gates for updates to the Pre-Spec, PMR, and product decisions.

For technical claims, inspect the latest `main` or `master` branch of `uSked/wde-service` and record the commit reviewed. Its root `AGENTS.md` currently redirects readers to `CLAUDE.md`; use that and focused `documents/` files to navigate, then verify behavior against code. Do not use a feature branch or an uncommitted checkout as the basis for a Feature Lab code review. Code informs feasibility and implementation questions; it does not override Feature Lab product decisions.
