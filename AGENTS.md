# Feature Lab workspace guidance

Read [Project Settings](docs/project-settings.md) and the relevant task guide. Their status is **Migration draft** until the cutover in [MIGRATION.md](MIGRATION.md) is complete; during that period, compare them with the corresponding live Google instruction docs and follow the live version if a material rule differs. After cutover, maintained Markdown governs the process. Never use `migration/source-snapshots/` as current instructions.

For a new meeting transcript, use [.agents/skills/feature-lab-ingestion/SKILL.md](.agents/skills/feature-lab-ingestion/SKILL.md). Google Drive is the home for transcripts, Pre-Specs, agendas that are saved, and spec sheets. Preserve the review gates for updates to the Pre-Spec, PMR, and product decisions.

For technical claims, inspect the latest `main` or `master` branch of `uSked/wde-service` and record the commit reviewed. Its root `AGENTS.md` currently redirects readers to `CLAUDE.md`; use that and focused `documents/` files to navigate, then verify behavior against code. Do not use a feature branch or an uncommitted checkout as the basis for a Feature Lab code review. Code informs feasibility and implementation questions; it does not override Feature Lab product decisions.
