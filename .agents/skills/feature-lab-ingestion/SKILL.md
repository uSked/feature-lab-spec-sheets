---
name: feature-lab-ingestion
description: Ingest a new Feature Lab meeting transcript, review changed Implementation Concepts against the current wde-service code, and prepare a Transcript Ingestion Review with next-lab recommendations.
---

# Ingest a Feature Lab transcript

Read the maintained [Project Settings](../../../docs/project-settings.md) and [Feature Pre-Spec Instructions](../../../docs/pre-spec-instructions.md). If either is marked Migration draft, also open its live Google source linked in the file; the live source governs material conflicts until the coordinated cutover. After cutover, use the maintained Markdown as the process authority. Check the governing source's title, metadata, status, hierarchy, and ingestion rules. `migration/source-snapshots/` are historical references only.

Identify the feature chat or series, new transcript, current Pre-Spec/Feature Working Model, latest Transcript Ingestion Review, and any referenced feature specs. Follow their source framing and the governing Project Settings. Treat new lab decisions as Working Decisions unless the governing instructions establish that they were confirmed.

Produce a Transcript Ingestion Review under the governing Pre-Spec Instructions before reconciling the Pre-Spec, unless Lyle explicitly directs a different route. Include candidate or changed Implementation Concepts, PMR candidates, implementation implications, and product-facing questions. Preserve the review and approval gates.

For each concept with material technical implications, use [the code review standard](../../../docs/code-review-standard.md). Inspect the latest `main` or `master` tip of `uSked/wde-service` (currently `master`) and record its commit. Search the relevant implementation, then separate demonstrated behavior from inference and gaps. Do not treat source code as product approval or deployed behavior.

Draft Pre Spec Implementation Questions from the concept-level implementation instructions using the format required by the governing Pre-Spec Instructions. Use code evidence to rank likely answers. Put a question on the Lab Agenda only when it needs product direction; keep engineering facts to confirm in Pre Spec Implementation Questions. Recommend a concise meeting agenda from the current Pre-Spec and review, without turning the agenda into a technical report.

Store an artifact in Google Drive when the governing instructions or Lyle's request call for a durable artifact. Confirm the Transcript Ingestion Review before updating the Pre-Spec. Do not update the PMR without Lyle's approval.
