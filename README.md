# Feature Lab Spec Sheets

This organization repository is the migration workspace for the Feature Lab Spec Sheets operating process. The intended workflow is transcript ingestion in Codex, direct review of the current `uSked/wde-service` default branch, and Google Drive as the home for Feature Lab working and final artifacts.

## Current authority

The [live Project Settings Google Doc](https://docs.google.com/document/d/1L3MC77mbsBH1X3goFo4AiAkn3TECJrO6djwLRT3L88g) and its linked instruction documents remain authoritative until the migration is reviewed and their authority is explicitly changed. Files in `migration/source-snapshots/` preserve the starting text; they are not active instructions.

The new [transcript ingestion skill](.agents/skills/feature-lab-ingestion/SKILL.md) uses the live Google instructions and adds a code review against the current `main` or `master` branch. See [MIGRATION.md](MIGRATION.md) for the cutover plan and [docs/code-review-standard.md](docs/code-review-standard.md) for the evidence standard.

## Sources and outputs

| Purpose | Location |
|---|---|
| Project-wide process, until cutover | [Project Settings](https://docs.google.com/document/d/1L3MC77mbsBH1X3goFo4AiAkn3TECJrO6djwLRT3L88g) |
| Pre-Spec and ingestion process, until cutover | [Feature Pre-Spec Instructions](https://docs.google.com/document/d/1AqbEu42Uoa8b5x6REb8uLynOxSxSH9RsrzgAkQ96VE4) |
| Spec Sheet process, until cutover | [Feature Spec Sheet Instructions](https://docs.google.com/document/d/1GfK0HnXye0cSW5VN8U7owAHx39muEQhYfMNre5ceHvE) |
| Current WDE/Usked implementation | [`uSked/wde-service`](https://github.com/uSked/wde-service), currently `master` |
| Transcripts and Feature Lab artifacts | Google Drive locations identified by live Project Settings and the relevant feature's source framing |

Do not commit transcripts, customer data, credentials, or feature-specific Google artifact copies to this repository. Link to those sources and record code commit IDs in reviews.
