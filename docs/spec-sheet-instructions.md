# Feature Spec Sheet Instructions

Last Updated: 2026-09-24 (America/New_York)
Updated By: Codex, adapted from the [live Feature Spec Sheet Instructions Google Doc](https://docs.google.com/document/d/1GfK0HnXye0cSW5VN8U7owAHx39muEQhYfMNre5ceHvE)
Change Summary: Converted the detailed two-chapter spec rules to Markdown, preserving approval and artifact boundaries and replacing the Agents Docs technical reference with current code review.
Authority / Use: Spec Sheet Draft and Final Spec Sheet structure and definition of done after cutover.
Status: Migration draft; the live Google guide governs until cutover.

The [source snapshot](../migration/source-snapshots/spec-sheet-instructions.md) preserves the pre-migration wording. Project-wide rules are in [Project Settings](project-settings.md); Pre-Spec rules are in [Pre-Spec Instructions](pre-spec-instructions.md); code evidence rules are in the [code review standard](code-review-standard.md).

## 0. Freshness and Use Controls

Before drafting, check this file's status, project-settings.md, and the current feature Pre-Spec. During migration, compare material rules with the live Google guide; it governs until cutover. Use the current Google artifact versions for product sources and code-review-standard.md for technical evidence. Treat engineering feedback as process evidence only after Lyle approves it; full engineering conversations are not standing instructions unless promoted. Keep credentials and sensitive infrastructure details out of specs and user-facing summaries.

## 1. Purpose and Target Output Model

### 1.1 Purpose

Feature Spec Sheets are the final development-facing output of the Feature Lab Spec Sheets workflow.
A Feature Spec Sheet exists to translate confirmed product decisions into a clear, compact, implementable build target for Usked engineering and AI-assisted development.
The spec sheet should be optimized for AI-assisted implementation and engineering review. It should not be optimized as a long human product narrative.

### 1.2 Two-Chapter Spec Sheet Model

Feature Spec Sheets should use two main chapters:
Chapter 1: Dev Review Cover Sheet
The cover sheet is the human-facing review layer. It exists so a developer, Lyle, QA, or another reviewer can quickly check Codex's plan and output against the approved product intent, source basis, scope, and known blockers.
Chapter 2: Implementation Spec
The implementation spec is the core build artifact. It exists to give Codex, engineering, or another implementation agent only the information needed to produce an implementation plan, implement the feature, or review implementation readiness.
The implementation spec should be compact, precise, and written in WDE/Usked 2.0 terminology. Less is more. Do not add general product-description language when a specific WDE/2.0 implementation term or surface can be named.

### 1.3 Primary Design Principle

The Feature Spec Sheet should separate human review context from implementation instructions.
The human cover sheet may explain why the feature exists, what sources were used, what is approved, and what should be checked during review.
The implementation spec should give Codex exactly what it needs to do the work: build target, WDE/Usked 2.0 surfaces, behavior, configuration/data requirements, constraints, open confirmations, and acceptance/test requirements.

### 1.4 Relationship to Other Reference Documents

project-settings.md defines the project-wide lifecycle, source priority, configured reference locations, and artifact routing.
pre-spec-instructions.md defines how Feature Working Model / Pre-Spec artifacts are initialized, maintained, reconciled after transcript ingestion, used to identify and curate Implementation Concepts, used to draft concept-level implementation instructions, used to generate Lab Agendas and Pre Spec Implementation Questions, and promoted toward spec drafting.
Feature Spec Sheet Instructions define the target output that the Pre-Spec process is trying to produce.
PMR defines reusable Usked product/system conventions that should inform spec language without cluttering individual specs.
The latest `main` or `master` commit of `uSked/wde-service` is the implementation reference. Use its `CLAUDE.md` and relevant `documents/` files for navigation, then inspect code. Code does not determine product decisions or prove what is deployed.

### 1.5 What This Document Governs

This document governs:
1. the two-chapter Feature Spec Sheet model;
2. the difference between human review context and implementation-ready implementation instructions;
3. definition of implementable / implementation-ready;
4. WDE/2.0 terminology precision expectations;
5. required spec structure at the chapter level;
6. Pre-Spec readiness signals for promotion into Spec Sheet Draft;
7. final cleanup and definition of done.

### 1.6 What This Document Does Not Govern

This document does not replace:
1. project-settings.md for project-wide routing and source priority;
2. pre-spec-instructions.md for transcript ingestion, Pre-Spec maintenance, Implementation Concept definition and curation, draft implementation instruction rules, Lab Agenda generation, or Pre Spec Implementation Questions;
3. PMR for reusable product conventions;
4. current codebase for current WDE/Usked 2.0 technical architecture;
5. engineering-owned implementation planning, migration planning, or code-level execution workflows.

## 2. Definition of Implementable / Implementation-Ready

### 2.1 Implementable Spec Definition

A Feature Spec Sheet is implementable when the implementation spec is specific enough for Codex or engineering to derive a credible implementation plan without reconstructing product intent from transcripts or asking avoidable product questions.
An implementable spec should include:
1. clear build target and scope;
2. confirmed product decisions separated from open questions;
3. precise WDE/Usked 2.0 terminology;
4. user-facing and system behavior;
5. likely WDE/Usked 2.0 surfaces;
6. data, configuration, permission, and visibility requirements;
7. constraints and known non-goals;
8. setup, acceptance, and test requirements;
9. explicit unresolved product blockers or engineering confirmations.

### 2.2 What Engineering Should Be Able to Derive

The implementation spec should provide enough structure for engineering to derive a credible implementation plan without rediscovering product intent.
The implementation spec should make clear:
1. feature goal and user-facing behavior;
2. launch points and object context;
3. likely modules/tables, records, fields, relationships, contexts, context columns, views, actions, routes, scripts, or configuration surfaces;
4. permission and visibility expectations;
5. setup and testing expectations;
6. open implementation confirmations still needed.

### 2.3 What a Spec Should Not Over-Prescribe

A Feature Spec Sheet should not attempt to become the full engineering implementation plan.
Do not over-prescribe:
1. code-level architecture unless explicitly required;
2. exact implementation mechanics that engineering should choose;
3. sensitive infrastructure details;
4. engineering-owned handoff or session-continuity workflows;
5. general descriptive product language that makes Codex infer implementation from prose.

### 2.4 Open Questions / Blockers Standard

Open questions should be explicit. They should not be hidden inside requirements.
Product questions should identify the product decision needed.
Engineering questions should identify the implementation confirmation needed.
A spec can remain useful with explicit unresolved blockers, but it should not present unresolved blockers as final requirements.

## 3. Source Basis and Drafting Authority

### 3.1 Primary Drafting Source

Once a current Feature Working Model / Pre-Spec exists, use it as the primary source for drafting a Spec Sheet Draft.
Before drafting, verify that the Pre-Spec contains a current Implementation Concepts list and draft implementation instructions for confirmed concepts. pre-spec-instructions.md owns the definition, status model, curation process, and draft instruction rules for Implementation Concepts.
If the Pre-Spec does not contain a current Implementation Concepts list, or if the list appears stale, incomplete, or unresolved, flag the gap before drafting Chapter 2. Do not invent new Implementation Concepts during final spec drafting without surfacing the gap for Lyle review.

### 3.2 Supporting Sources

Use Feature Lab transcripts for validation, conflict resolution, reversals, and traceability, not as the primary drafting source when a current Pre-Spec exists.
Use the PMR for reusable product conventions, terminology, menu/action patterns, permissions, messaging distinctions, recipient-selection patterns, and object-context rules.
Use the current codebase for likely WDE/Usked 2.0 implementation surfaces, terminology, and implementation-vetting questions.
Use current feature mockups, UI briefs, QA/test planning docs, implementation review notes, and related cross-feature specs as supporting references according to the feature source map.

### 3.3 Code Review Freshness Rule

When code informs spec guidance, inspect the latest main or master branch of uSked/wde-service and record the branch and commit. Use CLAUDE.md and relevant documents/ files for navigation; verify implementation claims against code. Flag discrepancies and distinguish implemented code from site deployment or runtime configuration.

### 3.4 Engineering Feedback as Process Evidence

Engineering implementation feedback may be used to improve this instruction document only after Lyle approves the feedback as process evidence.
Use mapped feedback artifacts carefully:
1. Spec input given to an implementation agent may inform target spec-sheet shape.
2. Follow-up implementation questions may inform future Pre Spec Implementation Questions.
3. Generated implementation plans may inform the definition of implementation-ready.
4. Full engineering conversations are supporting evidence and traceability, not standing instruction sources unless Lyle explicitly promotes them.

### 3.5 Sensitive Implementation Detail Guardrail

Do not include credentials, passwords, SSH keys or paths, private server paths, developer-specific database names, connection strings, or other sensitive implementation details in spec sheets or user-facing summaries.

## 4. Required Feature Spec Sheet Structure

This section now defines the required chapter-level structure. The detailed contents of each chapter will be refined in later passes.

### 4.1 Chapter 1: Dev Review Cover Sheet

Purpose:
The Dev Review Cover Sheet is the human-facing review layer. It exists so a developer, Lyle, QA, or another reviewer can check Codex's plan and output against the approved product intent, source basis, scope, known blockers, and testing expectations.
Use the cover sheet to capture review context, not implementation instructions. Anything Codex needs in order to build should live in Chapter 2: Implementation Spec.
Required cover sheet sections:
1. Feature / Status Snapshot
2. Source Basis
3. Feature Summary
4. Scope / Non-Scope
5. Approved Product Decisions
6. Feature-Specific Review Risks / Watchouts
7. Known Blockers / Open Review Items
8. Links / Attachments
1. Feature / Status Snapshot
Purpose: Identify the spec and its current state.
Include:
- Feature name
- Spec status
- Last updated
- Updated by
- Monday item, if applicable
Do not include:
- Approval status
- Approval owner
- Related Pre-Spec
- Product area / licensee
2. Source Basis
Purpose: Show what sources the spec was built from so the developer can understand the review trail if needed.
Include:
- Current Feature Working Model / Pre-Spec
- Key Transcript Ingestion Reviews, if relevant
- Relevant final transcripts, if needed for traceability
- Mockup / UI references, if applicable
- PMR references, if directly implicated
- current codebase references, if used to shape WDE terminology or likely implementation surfaces
- Related specs or cross-feature references
Rule: Keep this as a source list, not a source summary. Do not restate the Pre-Spec.
3. Feature Summary
Purpose: Give the reviewer the human-readable product intent before they evaluate Codex's technical plan or output.
Include:
- what the feature does;
- where it fits in Usked / WDE / the relevant workflow;
- what user-facing problem or workflow gap it addresses;
- what outcome the user should experience.
Rule: Keep this short. Feature area, licensee/package context, or product context can appear here naturally if relevant.
4. Scope / Non-Scope
Purpose: Give the reviewer a fast boundary check so Codex's plan/output does not expand the feature.
Include:
- in scope;
- out of scope;
- phase boundaries, if applicable;
- explicit non-goals.
Rule: Focus on boundaries that matter for review.
5. Approved Product Decisions
Purpose: Let the reviewer quickly compare Codex's plan/output against decisions that are already settled.
Include only decisions that materially affect implementation or review, such as:
- product behavior decisions;
- UX decisions;
- permission / visibility decisions;
- scope decisions;
- data/model decisions that affect product behavior.
Do not include:
- raw meeting history;
- exploratory discussion;
- stale decisions;
- implementation details that belong only in Chapter 2.
6. Feature-Specific Review Risks / Watchouts
Purpose: Identify likely places where Codex, engineering, or a reviewer could misunderstand the feature, overbuild it, underbuild it, or implement the wrong WDE/Usked 2.0 pattern.
Include only when useful:
- likely pitfalls specific to this feature;
- edge cases that are easy to miss;
- product decisions Codex might accidentally reverse or generalize;
- WDE/Usked 2.0 surfaces that are especially important to preserve;
- places where similar WDE terminology could be confused;
- out-of-scope work Codex may be tempted to add;
- known implementation assumptions that should be checked against Chapter 2;
- feature-specific review questions for the developer.
Do not include:
- a generic Codex review checklist;
- internal dev workflow steps;
- broad "make sure it works" checks;
- generic code-quality checks;
- generic QA checklist items.
7. Known Blockers / Open Review Items
Purpose: Prevent the reviewer from assuming everything is resolved.
Include only active items:
- product blockers;
- design / mockup blockers;
- engineering confirmation blockers;
- QA / test setup blockers;
- approval or sequencing blockers, if relevant.
Rule: Resolved items should not remain here.
8. Links / Attachments
Purpose: Keep the cover sheet brief by pushing supporting material into links.
Include:
- Pre-Spec
- Mockups
- Monday item
- Transcript folder or specific transcripts
- Related specs
- Engineering feedback doc, only if relevant and approved as process evidence
Rule: Use links rather than duplicating source content.
Cover sheet writing rule:
Keep the cover sheet brief. It may be human-readable, but it should not become a second product spec or duplicate the implementation spec.

### 4.2 Chapter 2: Implementation Spec

Purpose:
The Implementation Spec is the core build artifact. It should be compact, precise, and specific enough for Codex to produce an implementation plan or implementation output without relying on broad product prose.
Chapter 2 should be drafted from the confirmed Implementation Concepts and draft implementation instructions already curated in the Pre-Spec. Carry forward the implementation intent, terminology, constraints, and open confirmations from the Pre-Spec, then finalize them into the required Feature Spec Sheet structure. Do not recreate the implementation model from scratch, and do not invent new Implementation Concepts during spec drafting without flagging the gap for Lyle review.
Use the implementation spec to provide implementation instructions, not meeting history or broad rationale.
Working content areas:
1. build target;
2. confirmed Implementation Concepts from the Pre-Spec;
3. in-scope and out-of-scope behavior;
4. WDE/Usked 2.0 surfaces;
5. behavior requirements;
6. configuration / data requirements;
7. permissions / visibility requirements;
8. implementation constraints / open confirmations;
9. acceptance / test requirements.
Implementation spec writing rule:
Use precise WDE/Usked 2.0 terminology from current codebase. Name likely surfaces directly when known. Avoid general language such as "add a page," "show a list," "create an action," or "store the data" when the correct WDE term is known, such as menu item, place, tab, context, context column, context action, row action, page/GAP action, module/table, record, field, Handlebars view, Lua script, TSA, backend route, or frontend JavaScript behavior.

### 4.3 Compactness Rule

The Implementation Spec should be as short as possible while still being implementation-ready.
Do not include:
1. raw meeting history;
2. long rationale;
3. repeated Pre-Spec discussion;
4. stale open questions;
5. implementation choices that engineering should make;
6. unsupported assumptions;
7. generic product description that forces Codex to infer WDE implementation details.

## 5. WDE / Usked 2.0 Terminology Precision

### 5.1 Principle

Use WDE/Usked 2.0 terminology carefully and specifically. The goal is to reduce the chance that Codex implements from generic product language rather than the intended WDE/2.0 pattern.

### 5.2 Preferred Terms

Prefer precise terms such as:
1. module / table when referring to a WDE data structure;
2. record when referring to one row/object instance;
3. field when referring to a stored column on a module;
4. context when referring to a configured data query/display source;
5. context column when referring to a displayed/queryable column in a context;
6. context view / detail view when referring to WDE view rendering tied to a context or object;
7. context action when referring to an action available from a context toolbar;
8. row action when referring to an action available on a row;
9. page action / GAP action when referring to object-level actions exposed through the page-action menu;
10. menu item / place / tab / subtab / fifth element when referring to navigation placement;
11. wizard when referring to a multi-step WDE workflow;
12. Lua script when referring to Lua-based implementation logic;
13. TSA / trigger / sequence / action when referring to event-driven automation;
14. Handlebars view when referring to server-rendered UI;
15. frontend JavaScript behavior when referring to browser-side dynamic behavior;
16. backend route when referring to route/controller behavior;
17. package / builder configuration when referring to configurable records rather than custom code.

### 5.3 Avoid Vague Terms

Avoid vague use of object, table, action, view, wizard, screen, page, workflow, database, or automation when a more precise WDE/Usked 2.0 term is known.
If the precise term is not known, capture that as a Pre Spec Implementation Question rather than guessing.

## 6. Chapter-Writing Standards

### 6.1 Chapter 1: Dev Review Cover Sheet Standards

The cover sheet may use human-readable language, but it should remain brief and review-focused.
It should help the developer check Codex's plan and output against approved scope, source basis, intended product behavior, known non-goals, active blockers, testing expectations, and feature-specific review risks.
The cover sheet should not contain a generic Codex review checklist. Include review guidance only when it is specific to the feature and helps prevent a likely misunderstanding, overbuild, underbuild, wrong WDE/Usked 2.0 pattern, missed edge case, or known implementation assumption.

### 6.2 Chapter 2: Implementation Spec Standards

The implementation spec should use short, direct statements.
Chapter 2 Feature Details should use the confirmed Implementation Concepts from the Pre-Spec as the organizing structure where applicable. Each concept section should carry forward the finalized implementation instructions needed to build that concept, using precise WDE/Usked 2.0 terminology and preserving explicit open confirmations.
Use structured lists, tables, and explicit labels where helpful.
Write for Codex and engineering, not for a broad business audience.
Each requirement should be traceable to a build behavior, WDE/Usked 2.0 surface, configuration requirement, permission requirement, or test requirement.
Avoid conversational or speculative phrasing.

### 6.3 Acceptance Criteria and Testing

Acceptance criteria should be written so a tester can determine pass/fail without reconstructing intent from the Pre-Spec or transcript.
Acceptance criteria should cover:
1. trigger or starting condition;
2. user or system action;
3. expected system behavior;
4. expected data/configuration result;
5. expected UI result, if applicable;
6. permission/visibility expectations;
7. relevant edge cases.

## 7. Pre-Spec Readiness and Question Generation

### 7.1 Pre-Spec Readiness Checklist

Before promoting a Feature Working Model / Pre-Spec into a Spec Sheet Draft, check whether the Pre-Spec has enough information to produce both chapters and whether the Implementation Concepts list is current enough to support Chapter 2.
The Pre-Spec is ready for spec drafting when:
1. source framing is current;
2. relevant transcripts have been ingested or explicitly marked as not required;
3. confirmed decisions are separated from likely decisions and open questions;
4. scope boundaries are stable enough for implementation drafting;
5. the product model is coherent;
6. user flows and launch contexts are sufficiently clear;
7. permissions and visibility are sufficiently clear;
8. data/backend/configuration implications are identified;
9. UI/mockup needs are resolved, not required, or explicitly open;
10. the running Implementation Concepts list is current;
11. candidate or newly proposed Implementation Concepts are confirmed, deferred, removed, or explicitly marked as blockers;
12. confirmed Implementation Concepts have draft implementation instructions sufficient to support Chapter 2;
13. code-informed implementation implications are reviewed, with freshness checked through the current main or master commit and relevant implementation files;
14. Pre Spec Implementation Questions have captured engineering-facing uncertainties;
15. remaining open questions are explicit and do not hide inside requirements;
16. Lyle has approved or requested movement into spec drafting.

### 7.2 Lab Agenda Product Question Rules

Lab Agenda questions should be generated by comparing the current Pre-Spec against what the two-chapter spec must eventually contain.
Add a question to the Lab Agenda when the missing information prevents the eventual spec from being implementable and requires product direction, workflow clarification, UX choice, policy decision, scope confirmation, or Feature Lab discussion.
Do not add engineering-facing implementation questions to the Lab Agenda unless answering them requires a product decision.

### 7.3 Pre Spec Implementation Question Rules

Pre Spec Implementation Questions should be generated from the current Pre-Spec's Implementation Concepts and draft implementation instructions, then checked against this document, the PMR, and current codebase.
Add a question to Pre Spec Implementation Questions when missing information prevents the implementation spec from being implementation-ready but can be answered by engineering outside Feature Lab.
Implementation questions should identify:
1. related Implementation Concept;
2. draft implementation instruction gap;
3. likely reference area;
4. possible WDE/Usked 2.0 implementation surface;
5. source trigger;
6. how the answer may affect the Pre-Spec or concept-level draft implementation instructions;
7. whether the answer may affect the eventual Implementation Spec.

### 7.4 When to Promote to Spec Sheet Draft

Promote to Spec Sheet Draft only when the Pre-Spec is stable enough to produce the Dev Review Cover Sheet and Implementation Spec.
If major product, permission, workflow, lifecycle, messaging, data, UX, or implementation-readiness gaps remain unresolved, either keep the feature in Pre-Spec or carry the gaps as explicit open blockers.

## 8. Final Spec Sheet Cleanup / Definition of Done

Before treating a Spec Sheet Draft as final or implementation-ready, perform a cleanup pass.
Confirm that:
1. both chapters are present when applicable;
2. the cover sheet is brief and review-focused;
3. the implementation spec is compact and implementation-ready;
4. Chapter 2 carries forward confirmed Implementation Concepts and finalized implementation instructions from the Pre-Spec;
5. no new Implementation Concepts were invented during spec drafting without being flagged for Lyle review;
6. exploratory meeting history has been removed;
7. source basis is current;
8. requirements are clear and testable;
9. decisions are not mixed with open questions;
10. all open questions are explicit;
11. terms match PMR and current codebase terminology where relevant;
12. WDE/Usked 2.0 surfaces are named precisely where known;
13. implementation notes clarify likely surfaces without exposing sensitive details;
14. edge cases and warnings are included where they affect build or testing;
15. testing instructions and pass/fail criteria are complete;
16. formatting, numbering, headings, and list structure are clean;
17. any remaining blockers are clearly identified for Lyle, engineering, QA, or design.

## 9. Feedback and Revision Handling

### 9.1 Purpose

This section prevents future feedback from bloating this document or being promoted into standing instruction too quickly.

### 9.2 Engineering Feedback Rule

Engineering implementation feedback can inform this document only after Lyle approves it as process evidence.
Do not automatically convert engineering-owned implementation notes, migration notes, handoff notes, or implementation conversation transcripts into Feature Spec Sheet Instructions.

### 9.3 Full Implementation Conversation Rule

Full engineering implementation conversations are supporting evidence only. Use them to understand why earlier feedback artifacts mattered, but do not treat them as standing instruction sources unless Lyle explicitly promotes them.

### 9.4 Codebase Update Boundary

Review implementation changes at the current `main` or `master` tip of `uSked/wde-service`. Do not copy engineering feedback into this instruction document unless it directly changes Spec Sheet drafting standards and Lyle approves the process change.

### 9.5 Current Active Process Sample

The History Tabs engineering implementation feedback is the current active process sample for refining this document.
Use it in later passes to define detailed contents for the Dev Review Cover Sheet, detailed contents for the Implementation Spec, implementation-ready expectations, WDE-heavy feature expectations, and the connection between spec structure and Pre Spec Implementation Questions.
