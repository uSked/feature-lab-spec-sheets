# Feature Lab Spec Sheets — Project Settings

Last Updated: 2026-09-24 (America/New_York)
Updated By: Codex, adapted from the [live Project Settings Google Doc](https://docs.google.com/document/d/1L3MC77mbsBH1X3goFo4AiAkn3TECJrO6djwLRT3L88g)
Change Summary: Converted to Markdown and introduced current-code review in place of the Drive Agents Docs technical reference.
Authority / Use: Project-wide process and source registry after the coordinated cutover.
Status: Migration draft; the live Google instruction docs govern until cutover.

The [source snapshot](../migration/source-snapshots/project-settings.md) preserves the pre-migration wording. The [migration plan](../MIGRATION.md) tracks the authority change.

## 0. Runtime Operating Dashboard

Purpose of this dashboard:
Use this section first. It tells Codex what to check before acting, which linked instruction doc governs the task, and which guardrails must not be violated.

### 0.1 Startup Checklist

Before Feature Lab work, check this file's status and the [migration plan](../MIGRATION.md), identify the artifact type, and open the task-specific Markdown guide. During migration, compare with the corresponding live Google instruction doc and follow it if a material rule differs. For Google artifacts, open the live version and check its title, metadata, status, and content. Stop and tell Lyle if a required governing source or artifact is unavailable, incomplete, or internally contradictory.

### 0.2 Task Router

Transcript ingestion / Transcript Ingestion Review:
- Use Section 6 of this doc and Feature Pre-Spec Instructions. Transcript Ingestion Review identifies decisions, gaps, and candidate or changed Implementation Concepts.

Feature Working Model / Pre-Spec work:
- Use Feature Pre-Spec Instructions. The Pre-Spec owns the Implementation Concept definition, running concept list, statuses, and concept-level draft implementation instructions.

Lab Kickoff Agenda:
- Use Feature Pre-Spec Instructions, Lab Kickoff Agenda rules.

Lab Agenda / between-meeting agenda:
- Use Feature Pre-Spec Instructions, Lab Agenda rules. Lab Agendas may include Implementation Concept Review when the concept model is new, changed, uncertain, or blocking spec readiness.
- Keep agendas meeting-facing, concise, and free of ingestion-review, PMR, or process commentary.

Spec Sheet Draft / Final Spec Sheet:
- Use Feature Spec Sheet Instructions. Spec Sheet Drafts carry forward confirmed Implementation Concepts and finalized implementation instructions from the Pre-Spec rather than redefining the concept model.

PMR review / PMR update proposal:
- Use Section 7 of this doc and the PMR.
- Do not update the PMR without Lyle approval.

Codebase / implementation-vetting work:
- Use Sections 12, 13, and 15 plus code-review-standard.md.
- Codebase review is read-only for Feature Lab work.

Source hierarchy / methodology / artifact-process questions:
- Use this Project Settings doc first, then the relevant linked instruction doc.

### 0.3 Hard Guardrails

- Do not write to the application codebase during Feature Lab review.
- Do not update the PMR without Lyle approval.
- Do not update a Feature Working Model / Pre-Spec directly from a transcript unless Lyle explicitly asks for a direct update.
- Do not treat Lab Agendas as Transcript Ingestion Reviews, pre-spec briefs, PMR notes, or process explanations.
- Do not duplicate project-wide source registries inside feature-specific pre-specs unless a source is directly implicated by that feature.
- Do not rely on stale synced/uploaded sources when the live Google Doc or Drive source is available.

## 1. Purpose

This project converts Feature Lab discussions into clear, complete, dev-ready spec sheets for Usked engineering and AI-assisted development. Feature Spec Sheet Instructions define the target output and definition of done for those implementable spec sheets.
It also supports ongoing Feature Lab continuity by turning meeting transcripts into decisions, gaps, Implementation Concepts, PMR candidates, implementation implications, Pre Spec Implementation Questions, and next-meeting questions while the feature discussion is still active.

## 2. Operating Principles

Feature Labs, led by Lyle and Marvin, define product concepts, constraints, and decisions.
Gemini notes/transcripts capture raw discussion.
Codex is used to:
* synthesize Feature Lab discussions
* distinguish confirmed decisions from exploratory discussion
* identify gaps, conflicts, reversals, Implementation Concepts, and open questions
* identify reusable product conventions that may belong in the PMR
* vet decisions and Implementation Concepts against PMR and codebase implementation patterns
* update feature-specific working artifacts after review
* translate stable decisions into structured, precise spec language
Spec Sheets are the final output for development. Working artifacts exist to make the final spec cleaner, more accurate, and more implementable under Feature Spec Sheet Instructions.

## 3. Chat Organization / Feature Workspaces

Use a separate chat for each major feature topic.
Each feature chat is the continuity thread for that feature’s transcripts, source review, Transcript Ingestion Reviews, Feature Working Model / Pre-Spec, Implementation Concepts, question sets, spec drafts, and final spec handoff.
Methodology or project-settings chats may be used to refine project instructions, shared reference documents, source hierarchy, and spec-writing process. Do not treat a methodology/project-settings chat as the active feature workspace unless the user explicitly says so.
Recommended chat naming convention:
* Feature Lab – [Feature Name]
* Spec Sheet – [Feature Name]
* Feature Prep – [Feature Name]
When starting a new feature chat, first identify:
* feature name
* relevant Feature Lab transcripts
* existing prep/core-model/pre-spec/spec documents
* known source-of-truth documents
* current goal: meeting synthesis, transcript ingestion, question generation, pre-spec update, spec drafting, or final review

## 4. Feature Artifact Lifecycle

For each major feature, use this progressive lifecycle:
1. Transcript / Notes
Raw meeting source. Used as product-intent input, not as cleaned requirements.
2. Transcript Ingestion Review
Lightweight first-pass output created after each new Feature Lab transcript. It identifies key markers from the meeting before updating larger working artifacts.
3. Feature Working Model / Pre-Spec
Living synthesis document for the feature while Feature Lab is still active. It accumulates confirmed decisions, working definitions, scope boundaries, product model, architecture assumptions, unresolved questions, PMR candidates, Implementation Concepts, concept-level draft implementation instructions, implementation implications, and Pre Spec Implementation Questions across meetings. It is updated after the Transcript Ingestion Review has been reviewed or confirmed, unless Lyle explicitly asks to update it directly. Its source-framing section should reference the project-wide source hierarchy rather than duplicate the full list of project-wide reference documents. Its purpose is to progressively gather and organize the information needed to produce an implementable Feature Spec Sheet.
4. Spec Sheet Draft
Dev-facing implementation draft generated from the Feature Working Model / Pre-Spec once the feature direction is stable enough and evaluated against Feature Spec Sheet Instructions. Chapter 2 should carry forward confirmed Implementation Concepts and finalized implementation instructions from the Pre-Spec.
5. Final Spec Sheet
Approved implementation-ready Google Doc. It should satisfy Feature Spec Sheet Instructions and contain final requirements and any remaining explicit open questions, not exploratory meeting history.
The Feature Working Model / Pre-Spec is the bridge between raw transcripts and the final spec sheet. It is expected to change after each meeting in a multi-meeting feature series and should be shaped by the information needed to satisfy Feature Spec Sheet Instructions. The working flow is: Transcript -> decisions / gaps / Implementation Concepts -> Pre-Spec -> Lab Agenda / implementation questions -> Spec Sheet.
Derivative Artifact Source Rule
Once a Feature Working Model / Pre-Spec exists, derivative artifacts should use the Pre-Spec as the primary working source and canonical product model. This includes UI Mockup Request / Design Briefs, mockup coverage docs, QA/test planning docs, design review notes, implementation review notes, handoff summaries, and other support artifacts.

Feature Lab transcripts/notes remain the product-intent authority for validation, conflict resolution, reversals, and decision traceability, but derivative artifacts should generally be generated from the Pre-Spec rather than directly from raw transcripts. Current Spec Sheet Drafts, existing mockups, prior coverage/review artifacts, and relevant cross-feature references should be used as supporting inputs according to the feature’s Source Framing / Reference Tree.
Feature Pre-Spec Source Framing Rule

Do not list every project-wide reference document inside each Feature Working Model / Pre-Spec. Project-wide source hierarchy lives in this Project Settings guide and should be referenced, not duplicated.

Each Feature Working Model / Pre-Spec should list only feature-specific sources, such as relevant Feature Lab transcripts, Transcript Ingestion Reviews, existing feature working-model / pre-spec / core-model docs, current feature spec drafts or final specs, directly related cross-feature specs/pre-specs, and feature-specific supporting artifacts.

Project-wide reference documents should be named in a feature Pre-Spec only when directly implicated by a feature-specific interpretation, conflict, proposed update, implementation implication, design implication, mockup requirement, or source-priority exception.

Detailed pre-spec source-framing procedure lives in Feature Pre-Spec Instructions:
pre-spec-instructions.md

Feature Spec Sheet Instructions define the final target output and spec-sheet definition of done:
spec-sheet-instructions.md

UI Deliverables / Mockup Requirements
During Transcript Ingestion Reviews, Feature Working Model / Pre-Spec updates, and final spec review, identify whether UI mockups are required for the feature.

Mockups are not required for every feature. Recommend mockups when the feature introduces or materially changes a screen, page, navigation pattern, context/table/card/detail view, wizard flow, modal, fifth-element detail surface, badge/count behavior, recipient-selection pattern, permission-dependent visibility, or interaction state that cannot be clearly specified in text alone.

The Feature Working Model / Pre-Spec is the canonical internal place to track UI Deliverables / Mockup Requirements while the feature is being shaped. Separate UI Mockup Request / Design Brief documents should be created only when mockups need to be assigned, reviewed externally, or shared outside the feature-planning chat.

Detailed pre-spec UI/mockup tracking procedures live in Feature Pre-Spec Instructions:
pre-spec-instructions.md

Reusable UI decisions should be proposed as Design Guide updates for Lyle review. Do not update the Design Guide automatically.

## 5. Feature Lab Feedback Loop

After each Feature Lab meeting:

- Add or identify the specific transcript/notes source.
- Continue in the relevant feature chat.
- Produce a Transcript Ingestion Review before updating the Feature Working Model / Pre-Spec, unless Lyle explicitly requests a direct update.
- After Lyle reviews or confirms the Transcript Ingestion Review, update the Feature Working Model / Pre-Spec, its source framing, its running Implementation Concepts list, and affected draft implementation instructions as needed.
- Generate or update Lab Agenda / between-meeting prep when useful, using Feature Pre-Spec Instructions and Feature Spec Sheet Instructions to identify product-facing gaps or Implementation Concept review items that block an implementable spec.
- Repeat until the lab series is complete and the feature is ready for a Spec Sheet Draft.

Detailed pre-spec maintenance, source-scope check, and between-meeting prep procedures live in Feature Pre-Spec Instructions:
pre-spec-instructions.md

The goal is to surface gaps while the Feature Lab discussion is still active so product-facing questions and Implementation Concept review items can be answered directly or brought to the next meeting, and engineering-facing questions can be captured separately as Pre Spec Implementation Questions rather than reconstructed later.

## 6. Transcript Ingestion Review

Retrospective Feature Lab Reconstruction

Use Retrospective Feature Lab Reconstruction for older Feature Lab series that predate the structured Lab Agenda / Pre-Spec feedback loop. The goal is to preserve the current process shape while adding a confidence/reconstruction layer for source material that was not originally guided by Lab Agendas or ongoing Pre-Spec review.

For retrospective lab series:
- Create or identify a feature-specific Feature Working Model / Pre-Spec first.
- When Lyle identifies a bounded historical corpus as a pre-historic series, use the consolidated reconstruction route in the Feature Pre-Spec Instructions by default. Use meeting-by-meeting ingestion when Lyle requests individual approvals, sources arrive incrementally, or the source scope is ambiguous.
- Treat reconstruction as distinct from normal forward-process ingestion. Preserve meeting-level attribution even when the review is consolidated.
- Explicitly track confirmed decisions, strong product direction, assumptions, conflicts, reversals, missing feedback-loop questions, and confidence level.
- Use the reconstructed Pre-Spec to decide whether a clarification meeting is needed before spec drafting.

A clarification meeting should be recommended when unresolved questions materially affect the system model, permissions, object relationships, data model, core UX flow, or developer implementation decisions. A clarification meeting is usually not required for wording-level questions, edge-case-only questions, or items that can be safely deferred to design, QA, engineering implementation review, or final spec review.

Detailed retrospective reconstruction procedure lives in Feature Pre-Spec Instructions:
pre-spec-instructions.md

A Transcript Ingestion Review is the standard first-pass output after a new Feature Lab transcript is added. It should be shorter and easier to review than the Feature Working Model / Pre-Spec.

The review should identify meeting metadata, confirmed decisions, likely decisions needing confirmation, open questions, conflicts/reversals/pre-spec impacts, source-framing impacts, UI/mockup needs, terminology/product-model markers, candidate or changed Implementation Concepts, PMR candidates, codebase implementation implications, Pre Spec Implementation Questions, recommended Feature Working Model / Pre-Spec updates, and Lab Agenda / between-meeting prep needs.

Detailed Transcript Ingestion Review and transcript-to-pre-spec reconciliation procedures live in Feature Pre-Spec Instructions:
pre-spec-instructions.md

Do not update the Feature Working Model / Pre-Spec directly from a transcript unless Lyle explicitly asks for that. First produce the Transcript Ingestion Review, let Lyle confirm/correct it, then update the working Pre-Spec.

## 7. PMR Review Process

PMR review happens inside the Transcript Ingestion Review after every new Feature Lab transcript is added.
Review the transcript not only for feature-specific decisions, but also for reusable Usked product conventions that may belong in the Usked Product Model Reference.
Use this rule of thumb:
   * Feature-specific decision → Feature Working Model / Pre-Spec or Spec Sheet
   * Reusable Usked product convention → PMR
   * Technical implementation pattern → code-informed notes or Pre Spec Implementation Questions
   * Raw discussion detail → transcript synthesis / meeting notes
For each recommended PMR update, state:
   * proposed PMR language
   * why it belongs in the PMR instead of only in the feature spec
   * which transcript or decision supports it
   * whether it conflicts with or refines existing PMR language
Do not update the PMR automatically. Always present proposed PMR changes first and wait for approval.

## 8. How to Interpret Feature Lab Notes

Treat Feature Lab transcripts as source-of-truth inputs for product intent, but not final decisions unless clearly stated.
Separate:
   * confirmed decisions
   * likely decisions needing confirmation
   * open questions
   * exploratory discussion
   * conflicts or reversals
Prioritize repeated ideas across meetings and explicit Lyle/Marvin agreement. Call out ambiguity instead of guessing.

## 9. Source Priority

Use sources in this order unless Lyle gives a different instruction:

1. Feature Lab notes/transcripts for product intent, decisions, and discussion history.
2. Current Core Model / Pre-Spec / Feature Working Model for vetted feature-specific decisions and architecture direction.
3. [Feature Spec Sheet Instructions](spec-sheet-instructions.md) for the output structure and definition of done.
4. Usked Product Model Reference (PMR) for reusable product and system conventions.
5. The current `main` or `master` branch of `uSked/wde-service` for implemented WDE/Usked 2.0 behavior and implementation vetting; see the [code review standard](code-review-standard.md).
6. Older documentation folders, SOPs, and historical system docs as supporting references, validated before becoming requirements.

Code evidence does not promote a product proposal to a decision and does not establish what is deployed on a particular site. Flag stale or conflicting sources.
Cross-Feature Spec Reference Rule
When a feature spec references another feature, workflow, module, or product area, first search for an existing spec sheet, pre-spec, core model, or working model for that referenced feature. Use the most current existing spec/pre-spec as the primary cross-feature reference before relying only on transcripts.

Use Feature Lab transcripts to validate, fill gaps, or resolve conflicts, but do not treat transcripts as the only source when an implementation spec already exists for the related feature.

When updating a spec that depends on another feature, define only the current spec’s feature-specific launch context, defaults, scope boundaries, or integration requirements. Do not re-spec the other feature’s full behavior unless the user explicitly asks to merge or revise that related spec.

If no related spec/pre-spec exists, state that no current cross-feature spec was found and fall back to transcripts, PMR, current codebase, and supporting docs using the normal source priority rules.
Resource Document Final-Pass Rule
When a work product is considered done and one or more shared resource documents were edited as part of that work, recommend a final pass on each edited resource document before closing the loop.

The final pass should check readability, formatting consistency, heading/list structure, stale or duplicate language, cross-reference clarity, and any substantive consistency issues that would make the resource document less useful for future work.

This applies to resource documents such as the PMR, code-informed reference notes, Project Settings, reusable working-model templates, source-priority docs, or any other shared reference used across future Feature Lab/spec-sheet work.

The final pass should not introduce new product decisions. It should tighten the document for future reuse and flag any substantive uncertainty for Lyle review instead of silently resolving it.

### Project Reference Freshness Registry

After cutover, this Git repository is the instruction registry. During migration, the linked live Google instruction docs remain authoritative. Use Git history and the current main commit for instruction versions; use each live Google artifact's title, header metadata, status, and content for artifact freshness. A newer artifact date than an instruction file is normal. Warn Lyle when a required source is unavailable, non-current, incomplete, internally contradictory, or substantively conflicting.

| Reference | Authority and use | Location |
|---|---|---|
| Project Settings | Project-wide process and source map | project-settings.md |
| Feature Pre-Spec Instructions | Ingestion, Pre-Spec, Implementation Concepts, agendas, implementation questions | pre-spec-instructions.md |
| Feature Spec Sheet Instructions | Spec Sheet Draft and Final Spec Sheet standards | spec-sheet-instructions.md |
| Code Review Standard | Current implementation evidence, code citations, uncertainty | code-review-standard.md |
| PMR | Reusable product conventions; updates require Lyle approval | Live Google Drive document, located through project-wide references |
| Design Guide / Mockup Instructions | Reusable design guidance when applicable | Live Google Drive document once linked; edit at Lyle's direction |

Project-wide reference documents and folders still live in the Project-Wide Reference Docs folder:
https://drive.google.com/drive/folders/1B6JDLXH3qSVaTnT1rGjxZBTNwtj3ZQ8U

Add a new reusable reference to this source map only after Lyle approves its authority and usage rule. Feature Pre-Specs list feature-specific sources; they do not copy the entire project-wide registry. When editing an instruction file, update its header metadata and Git history. Do not mirror dates across other instruction files merely because one changes.

## 10. Configured Project Sources

Configured project source locations include:
Project-Wide Reference Docs folder:
https://drive.google.com/drive/folders/1B6JDLXH3qSVaTnT1rGjxZBTNwtj3ZQ8U
Used for shared reference documents across Feature Lab Spec Sheets, including Project Settings, PMR, Design Guide, mockup/design process docs, QA/testing references, source-priority guides, Feature Pre-Spec Instructions, Feature Spec Sheet Instructions, and reusable templates. Do not rely on this folder as a project Source. Use this folder link/name when searching Google Drive for current project-wide reference documents.
Feature Lab Transcriptions folder:
https://drive.google.com/drive/folders/1nfFN3i6F4zJzLj0R5Sp56PcfSt7xfrzV
Used for all Feature Lab transcripts for this project. Do not rely on this folder as a project Source. Use this folder link/name when searching Google Drive for transcripts during transcript ingestion or feature source-scope review.
Current codebase:
uSked/wde-service, latest main or master branch (currently master). Use code-review-standard.md for implementation vetting. The older Agents Docs Drive folder is historical support only; use it to investigate discrepancies, not as proof of current implementation.

Other configured/supporting source groups may include:
- Documentation - WDE
- Documentation - Usked 2.0
- Solutions Spec Sheets
- Usked Product Model Reference
The configured list is a hint, not a restriction. Follow explicit user instructions.
The detailed file/folder inventory may live in project connector scope, Drive source configuration, or the linked project-wide folders above and does not need to be repeated in full here.
Documentation folders may include useful terminology, existing system concepts, WDE mechanics, Handlebars, workflows, permissions, and historical implementation patterns. Treat them as supporting reference material, not final authority, because they may not be fully current.
When using older/supporting docs, phrase conclusions carefully:
“This supports the terminology…”
“This appears to describe the existing WDE pattern…”
“This should be confirmed if it becomes a requirement…”
Do not treat supporting docs as proving current behavior unless confirmed by current Feature Lab decisions, the PMR, current codebase, or explicit user confirmation.

## 11. Usked Product Model Reference (PMR)

The PMR is a durable reference for reusable Usked product/system knowledge that should not clutter individual spec sheets.
Use it for:
   * menu hierarchy
   * Row / Bulk / Page Actions
   * permission model conventions
   * dynamic menu and badge behavior
   * inbox / thread / message distinctions
   * team / role / mailbox distinctions
   * recipient-selection UX patterns
   * object context and object-specific actions
   * permission references in specs
   * reusable terminology, UX patterns, permission assumptions, or object-model distinctions
Update the PMR when Feature Lab decisions establish reusable Usked product conventions that should apply across future specs.
Do not use the PMR for feature-specific scope, phase decisions, one-off requirements, or implementation details that belong in code-informed notes or the feature spec.

## 12. Current Codebase Technical Reference

Use the latest main or master branch of uSked/wde-service as the implementation reference. The repository root AGENTS.md points to CLAUDE.md; use those and relevant documents/ files for navigation, then inspect code for claims about implemented behavior. Record repository, branch, commit, and file/function evidence. Do not use a feature branch or uncommitted working tree as the basis for an ingestion review. Code informs feasibility; it does not override Feature Lab decisions or prove site-specific deployment. Treat documents/plans/ as proposals.

## 13. Code-Informed Implementation Vetting

During transcript ingestion and before finalizing a complex spec, review changed Implementation Concepts against relevant modules/tables, fields, contexts and context columns, views, actions, filter groups, wizards, Lua scripts, TSAs, Handlebars, frontend JavaScript, backend routes, notifications, packages, jobs, and configuration. Identify product-correct but technically vague requirements, likely existing patterns, dependencies, and risks. Separate confirmed code evidence from inference and deployment-dependent behavior. Turn unresolved implementation facts into Pre Spec Implementation Questions; keep product decisions for Lyle and the lab. Follow code-review-standard.md.

## 14. WDE Terminology Precision

Use Module/table for a WDE data structure; record for one row or instance; field for a stored column; context for a configured query/display source; context column for a displayed or queryable column; context action, row action, and page/GAP action for their respective action surfaces; wizard for a step-based workflow; Handlebars view for server-rendered UI; and TSA for event-driven Trigger-Sequence-Action automation. Avoid vague terms when the precise WDE term is known.

## 15. Technical Guardrails

The repository currently uses a modular PHP backend, browser frontend, LuaSandbox-based Lua 5.1, Handlebars-style server-rendered views, WDE/Lua wizards, contexts for query/display, and TSAs for data-change automation. Verify any implementation-specific implication against the current commit. Dynamic UI may involve frontend JavaScript, backend routes, views, or a combination. Do not include credentials, private paths, connection strings, developer-specific databases, or sensitive infrastructure details in Feature Lab artifacts.

## 16. Spec Writing Standards

Write specs for developers building the feature.
All spec outputs should:
   * be clear, structured, and unambiguous
   * avoid conversational or speculative language
   * separate requirements, logic, UX behavior, backend/data structures, inputs, outputs, constraints, edge cases, and open questions
   * avoid over-engineering or adding features not discussed
   * improve clarity without changing intent
   * identify missing logic or gaps
   * push back when something is unclear or inconsistent
Formatting-sensitive drafting rule: Draft and edit with cleanup in mind. Maintain clean numbering, heading hierarchy, spacing, list structure, punctuation consistency, and section boundaries as part of the edit rather than as a separate cleanup step. When removing or moving items, renumber affected lists immediately and preserve consistent Markdown/Google Docs structure.

Default structure when applicable is now governed by Feature Spec Sheet Instructions. Use the abbreviated structure below only as a lightweight fallback:
   1. Purpose
   2. Definitions / Concepts
   3. User Flow / Steps
   4. Functional Requirements
   5. Logic / Rules
   6. Data / Backend Requirements
   7. UX Considerations
   8. Edge Cases / Warnings
   9. Open Questions
For complex topics, use a working canvas/prep doc first, then move final approved language into the Google Doc spec sheet. Keep exploratory language out of final specs.

## 17. Messaging-Specific Principles

Messaging must respect object context and permissions.
Recipient selection must be controlled and filtered, not open-ended.
Support both:
   * individual recipients / people
   * team / role-based recipients
Avoid “network tab dumping.” All recipient options must be intentional and preferably driven by backend mapping tables such as role/object mapping.

## 18. Collaboration Style

Be concise and direct.
Do not assume decisions that were not made.
When helpful, propose:
   * cleaner models
   * clearer abstractions
   * better naming
The goal is to produce spec sheets that require minimal back-and-forth with engineering, can be implemented quickly, and are compatible with AI-assisted development workflows.
