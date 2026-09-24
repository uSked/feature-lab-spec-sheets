# Instruction migration plan

## Boundary

Move the **operating instructions** to this repository. Keep Feature Lab transcripts, PMR, feature Pre-Specs, agendas when saved, Spec Sheet Drafts, and Final Spec Sheets in Google Drive. The snapshots in `migration/source-snapshots/` record the pre-migration instructions captured on 2026-09-24 and make rule-by-rule reconciliation possible.

## Migration sequence

1. Inventory the live Project Settings, Feature Pre-Spec Instructions, and Feature Spec Sheet Instructions. Map every operating rule, trigger, source priority, artifact boundary, freshness rule, and review gate to a maintained Markdown destination. Keep the Google links as provenance during the conversion.
2. Convert the project-wide source hierarchy and task router into a concise `docs/project-settings.md`. Convert detailed Pre-Spec and Spec Sheet rules into focused reference files. Put only always-applicable routing in `AGENTS.md` and task mechanics in Codex skills. Do not copy every source document into the agent's startup context.
3. Replace the old Agents Docs technical-source rule with `docs/code-review-standard.md`. The current target is the latest `main` or `master` branch of `uSked/wde-service` (currently `master`). Use repo documentation for navigation and the code for claims about implementation. Record branch, commit, file/function evidence, and uncertainty on every code-informed review.
4. Pilot one new transcript ingestion. Compare the resulting Transcript Ingestion Review, Implementation Concept questions, and proposed agenda with the existing Feature Lab rules. Check that engineering questions stay out of the meeting agenda unless a product decision is needed, and that the Pre-Spec is not updated before its review gate.
5. Review the converted rules against the source snapshots and resolve omissions or conflicts. Once Lyle accepts the cutover, update the live Google instruction docs to point to this repo as the process authority and label their old instruction text archival. Do this as one coordinated cutover so two active instruction sources do not compete.
6. After cutover, remove the migration-only routing from `AGENTS.md`, make the maintained Markdown files authoritative, and retain the Google source links and the git history for traceability. Keep Google artifact links in the project settings source map.

## Current status

The three Google instruction documents have been captured and converted to maintained Markdown drafts. Their artifact boundaries, decision statuses, approval gates, and detailed Pre-Spec and Spec Sheet procedures are retained. The old Agents Docs technical reference has been rewritten as current `uSked/wde-service` code review. One source conflict was reconciled in the drafts: the older Project Settings guide prescribed meeting-by-meeting retrospective ingestion, while the newer Pre-Spec guide makes consolidated review the default for a bounded pre-historic series. The remaining steps are a final rule audit, a pilot ingestion, and the coordinated authority cutover. The live Google instruction documents remain authoritative until that cutover. No Google artifact or PMR has been changed by this stage.
