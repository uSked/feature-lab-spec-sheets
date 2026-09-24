# Feature Pre-Spec Instructions

Last Updated: 2026-09-24 (America/New_York)
Updated By: Codex, adapted from the [live Feature Pre-Spec Instructions Google Doc](https://docs.google.com/document/d/1AqbEu42Uoa8b5x6REb8uLynOxSxSH9RsrzgAkQ96VE4)
Change Summary: Converted the detailed procedure to Markdown, preserving artifact and decision gates and replacing the Agents Docs technical reference with current code review.
Authority / Use: Ingestion, Pre-Spec, Implementation Concepts, agendas, and Pre Spec Implementation Questions after cutover.
Status: Migration draft; the live Google guide governs until cutover.

The [source snapshot](../migration/source-snapshots/pre-spec-instructions.md) preserves the pre-migration wording. Project-wide rules are in [Project Settings](project-settings.md); code evidence rules are in the [code review standard](code-review-standard.md).

## 1. Purpose

This document defines the reusable process for creating and maintaining Feature Working Model / Pre-Spec artifacts in the Feature Lab Spec Sheets project. The purpose of the Pre-Spec process is to progressively gather, test, organize, and reconcile the information needed to produce an implementable Feature Spec Sheet.

A Feature Working Model / Pre-Spec is a living synthesis document used while a Feature Lab series is active. It is not a final implementation spec. It exists to preserve feature-specific source framing, confirmed decisions, working definitions, scope boundaries, product model, unresolved questions, PMR candidates, Implementation Concepts, draft implementation instructions, Pre Spec Implementation Questions, and meeting prep while the feature is still being shaped.

Feature Spec Sheet Instructions define the target output and definition of done for implementable Feature Spec Sheets. Pre-Specs, Lab Agendas, Implementation Concepts, draft implementation instructions, and Pre Spec Implementation Questions should be shaped by what the eventual spec sheet must contain.

## 2. Command: Start New Feature Lab Pre-Spec

Operational trigger phrase:
"Start new feature lab pre spec"

Use this command when Lyle wants to initialize a new Feature Working Model / Pre-Spec for a new feature series before the feature has a stable working model. If Lyle describes the series as “pre-historic” or asks to reconstruct a bounded historical transcript series as a whole, route immediately to Section 4.6.1, Consolidated Pre-Historic Reconstruction. Do not default that request to individual transcript approvals.

Command purpose:
Create a clean source-framed Feature Working Model / Pre-Spec shell and establish the correct artifact lifecycle before detailed product synthesis begins.

This command should not produce a full product model unless one of the following is true:
1. A Transcript Ingestion Review has already been completed and confirmed.
2. Lyle explicitly asks for direct working-model content to be added before formal transcript ingestion.
3. The user provides enough confirmed source material and explicitly asks for a more developed initial pre-spec.

## 3. Required Inputs

Before creating or updating a pre-spec, collect or infer:
1. Feature name.
2. Current goal.
3. Whether this starts a new feature or continues an existing feature.
4. Relevant transcripts / notes, if any.
5. Existing prep, core-model, pre-spec, spec draft, final spec, canvas, or source artifacts, if any.
6. Known feature-specific source documents or folders.
7. Whether the user wants only an initial shell or direct working-model content.

If inputs are missing, proceed with a clearly labeled assumption only when safe. Otherwise ask Lyle for the missing source or confirmation.

## 4. Decision Tree

### 4.1 No transcript exists yet

Create only an initial Feature Working Model / Pre-Spec shell.
Do not synthesize detailed product model sections, requirements, Implementation Concepts, draft implementation instructions, implementation assumptions, or meeting prep unless Lyle explicitly provides an initial concept or asks for direct working-model content.

The shell should capture:
- source framing;
- status;
- current goal;
- initial scope provided by Lyle;
- known source materials;
- initial working assumptions;
- first-meeting open questions;
- transcript ingestion status;
- next step.

### 4.2 Transcript is available but not ingested

Produce a Transcript Ingestion Review first.
Do not update the Feature Working Model / Pre-Spec from transcript content until Lyle reviews or confirms the Transcript Ingestion Review, unless Lyle explicitly asks for a direct pre-spec update.

### 4.3 Transcript Ingestion Review is complete and confirmed

Use the Transcript Ingestion Review as the work order for the pre-spec update.

Update the Feature Working Model / Pre-Spec with:
- confirmed decisions;
- likely decisions needing confirmation;
- product-facing open questions;
- conflicts / reversals / pre-spec impacts;
- source-framing changes;
- terminology / product model markers;
- PMR candidates;
- Implementation Concepts introduced, changed, confirmed, deferred, or removed;
- draft implementation instruction impacts;
- codebase / implementation implications;
- Pre Spec Implementation Questions tied to Implementation Concepts where possible;
- Lab Agenda updates, including concept review items when needed.

### 4.4 Existing Feature Working Model / Pre-Spec already exists

Do not create a duplicate pre-spec. Open or identify the existing document, check its Feature-Specific Source Framing / Reference Tree, and continue from the current artifact state.

### 4.5 Feature direction is stable enough for spec drafting

Generate a Spec Sheet Draft from the Feature Working Model / Pre-Spec using Feature Spec Sheet Instructions as the target-output and definition-of-done reference. Do not use the raw transcript as the primary drafting source once a current pre-spec exists. Transcripts remain validation and traceability sources.

### 4.6 Retrospective Feature Lab Reconstruction

Use this branch when a feature lab series predates the structured Lab Agenda / Pre-Spec feedback loop used in newer feature labs.

Route selection:
1. Consolidated pre-historic reconstruction is the default when Lyle calls the series “pre-historic,” asks to work through the full historical series, or provides a bounded multi-transcript corpus that should be reconstructed as one combined product record.
2. Meeting-by-meeting retrospective reconstruction is used only when Lyle explicitly requests individual transcript approvals, when sources arrive incrementally, or when a source gap or material ambiguity makes a consolidated pass unsafe.
3. Do not silently default a pre-historic series to one-transcript-at-a-time ingestion.
4. Record the selected route and source inventory in the initial Pre-Spec shell.

#### 4.6.1 Consolidated Pre-Historic Reconstruction

Purpose:
Reconstruct the feature from the complete historical corpus, allow later meetings to supersede earlier proposals, and present one combined ingestion and initial reconciliation before substantive Pre-Spec development.

Reasoning effort:
Use enough review depth for the full historical corpus and material cross-transcript conflicts. Keep focused cleanup and follow-up passes proportional to the question; no particular Codex model or reasoning setting is a standing process requirement.

Process:
1. Create or identify a feature-specific Feature Working Model / Pre-Spec and mark it Retrospective Draft.
2. Inventory all known transcripts, notes, historical specs, mockups, and directly relevant supporting artifacts before ingestion begins.
3. Establish the chronological source order. Classify historical specs, mockups, and implementation notes as supporting reconstruction evidence unless Lyle explicitly grants them higher authority.
4. Read every known transcript in chronological order during one consolidated working pass.
5. Track confirmed or explicit decisions, strong product direction, assumptions, conflicts, reversals, missing feedback-loop questions, candidate Implementation Concepts, implementation implications, and clarification-meeting candidates across the full corpus.
6. Reconcile earlier discussion against later meetings during the same working pass. Later explicit decisions supersede earlier proposals; preserve material reversals and unresolved conflicts for traceability.
7. Produce one Consolidated Retrospective Transcript Ingestion Review covering the complete transcript set and the initial cross-transcript reconciliation. Do not require separate approval after each historical meeting.
8. Present the consolidated review to Lyle for correction, clarification, and approval.
9. Update the substantive Pre-Spec only after Lyle approves the consolidated review, unless Lyle explicitly requests a direct update.
10. Continue through staged reconciliation passes, pausing for Lyle approval between material passes:
   a. Source chronology, decision status, conflicts, reversals, and supersession.
   b. Product model, terminology, scope boundaries, permissions, object relationships, workflows, and edge cases.
   c. Implementation Concepts, concept statuses, and concept-level draft implementation instructions.
   d. PMR candidates, current codebase implications, technical uncertainties, and Pre Spec Implementation Questions.
   e. Final cross-section consistency, clarification-meeting threshold, and Ready for Spec Draft assessment.
11. Adapt the pass labels to the feature when useful, but preserve the separation between product reconciliation, implementation reconciliation, and readiness review.
12. After all passes are approved, promote the Pre-Spec through the applicable retrospective statuses and proceed under Feature Spec Sheet Instructions.

Consolidated review requirements:
- Identify the complete source set and chronological order.
- Separate transcript-confirmed decisions from likely direction, assumptions, and later post-lab decisions.
- Show where later meetings supersede, narrow, or close earlier discussion.
- Identify legacy artifacts and state their authority.
- Preserve unresolved product questions without inventing answers.
- Identify candidate or reconstructed Implementation Concepts.
- Identify implementation-facing uncertainty without allowing technical references to override product decisions.
- Recommend whether a clarification meeting is required.
- State the proposed next reconciliation pass and its approval checkpoint.

#### 4.6.2 Meeting-by-Meeting Retrospective Reconstruction

Use this route only when individually sequenced review is intentionally selected.

Process:
1. Create or identify a feature-specific Feature Working Model / Pre-Spec before spec drafting.
2. Mark the Pre-Spec status as Retrospective Draft until the transcript set has been ingested and reconciled.
3. Ingest meetings one by one in chronological order when possible.
4. Use a Retrospective Transcript Ingestion Review variant for each meeting.
5. Update the Pre-Spec only after Lyle reviews or confirms the retrospective ingestion review, unless Lyle explicitly requests direct updates.
6. Maintain a running Retrospective Open Questions / Clarification Meeting Candidates section inside the Pre-Spec.
7. After all known transcripts are ingested, perform a reconciliation pass across the full Pre-Spec.
8. Decide whether the Pre-Spec is strong enough for spec drafting or whether a clarification meeting is required.

Retrospective ingestion review additions:
- Retrospective confidence / follow-up needed.
- Confirmed or explicit decisions.
- Strong product direction that appears likely but was not formally decided.
- Assumptions detected from transcript discussion, older drafts, mockups, or implementation notes.
- Conflicts, reversals, or places where later transcript content appears to supersede earlier direction.
- Missing feedback-loop questions that would have gone into a Lab Agenda under the current process.
- Candidate or reconstructed Implementation Concepts that should be confirmed, deferred, removed, or carried as blockers.
- Clarification meeting candidates that materially affect spec quality.

Recommended retrospective Pre-Spec statuses:
1. Retrospective Draft — built from older transcripts and not yet fully reviewed.
2. Reconciled Draft — all known transcripts have been ingested and conflicts/open questions are listed.
3. Confirmed Working Model — Lyle has reviewed the open questions or a clarification meeting has resolved material gaps, including material Implementation Concept gaps.
4. Ready for Spec Draft — stable enough to convert into implementation-facing requirements under Feature Spec Sheet Instructions, with a current Implementation Concepts list and draft implementation instructions for confirmed concepts.

Clarification meeting threshold:
Recommend a clarification meeting when unresolved questions affect the system model, Implementation Concepts, permissions, object relationships, data model, core UX flow, implementation-facing scope, or developer handoff quality. Do not require a clarification meeting for wording-level questions, minor edge cases, design-only choices, QA-only details, or items that can be safely carried as explicit open questions in the spec draft.

## 5. Initial Pre-Spec Shell Structure

Use this structure when initializing a new pre-spec before transcript ingestion.

[Feature Name] — Feature Working Model / Pre-Spec

1. Feature-Specific Source Framing / Reference Tree
Reference Project Settings as the project-wide source hierarchy rather than duplicating all project-wide sources.
List only feature-specific sources, such as:
- relevant Feature Lab transcripts;
- Transcript Ingestion Reviews;
- existing feature working-model / pre-spec / core-model docs;
- current feature spec drafts or final specs;
- related cross-feature specs or pre-specs;
- directly relevant supporting artifacts.

2. Status
Include document type, feature name, current source basis, review state, and current goal.

3. Purpose
Short product/problem statement based only on confirmed user-provided scope or source material.

4. Initial Scope Provided by Lyle
Capture the user-provided scope verbatim or near-verbatim. Do not rewrite into final requirements yet.

5. Known Source Materials
List known feature-specific sources and note whether each has been reviewed, ingested, or is pending review.

6. Initial Working Assumptions
Include only clearly labeled assumptions needed for first discussion prep. Do not treat assumptions as decisions.

7. Open Questions for First Feature Lab
Include focused confirmation questions based on the initial scope. Questions should confirm whether the scope is complete, whether major workflow is missing, what source material is needed, and what product decisions are needed before an implementable spec sheet can be written.

8. Transcript Ingestion Status
State one of:
- No transcript exists yet.
- Transcript is available but not ingested.
- Transcript Ingestion Review is complete and pending Lyle review.
- Transcript Ingestion Review is confirmed.
- Pre-Spec has been reconciled to the confirmed Transcript Ingestion Review.

9. Next Step
State the next process action.

## 6. What Not to Include in an Initial Shell

Do not include the following in a new pre-ingestion shell unless Lyle explicitly requests it:
- detailed product model sections;
- final-sounding decisions;
- implementation surface checklists;
- Implementation Concepts or draft implementation instructions unless explicitly provided by Lyle or supported by confirmed source material;
- detailed data/backend assumptions;
- full permission models;
- final acceptance criteria;
- exhaustive question inventories;
- meeting prep sections;
- speculative workflow steps;
- downstream handoff lists.

The initial shell is a process anchor and source map, not a finished synthesis.

## 7. Transcript Ingestion Review Relationship

The Transcript Ingestion Review is the standard first-pass output after a new Feature Lab transcript is added. A Transcript Ingestion Review should generally be created before updating a Feature Working Model / Pre-Spec.

The review should include:
- decisions confirmed during the current lab from a prior working-decision cycle or through explicit Lyle approval;
- new working decisions / decisions to confirm at the next lab;

- product-facing open questions;
- conflicts / reversals / pre-spec impacts;
- source-framing / reference-tree impacts;
- UI deliverables / mockup needs;
- terminology / product model markers;
- recommended PMR updates;
- Implementation Concepts introduced, changed, confirmed, deferred, or removed;
- draft implementation instruction impacts;
- codebase / implementation implications;
- Pre Spec Implementation Questions tied to Implementation Concepts where possible;
- recommended Feature Working Model / Pre-Spec updates;
- Lab Agenda needs, including concept review items when needed.

### 7.1 Forward-Lab Decision Confirmation Rule

New product decisions made during a Feature Lab are Working Decisions, even when the transcript shows clear agreement. The next Lab Agenda must present them as Decisions to Confirm. They become Confirmed Product Decisions only when the next Feature Lab confirms them or when Lyle explicitly confirms them outside the normal lab cycle.
A first-lab Transcript Ingestion Review ordinarily contains no Confirmed Decisions because there is no prior working-decision set to confirm. Decisions confirmed during the current meeting from a prior Lab Agenda may be listed as Confirmed Decisions; newly made decisions remain Working Decisions to Confirm.
Lyle’s confirmation that a Transcript Ingestion Review is accurate authorizes reconciliation of the review into the Pre-Spec but does not, by itself, promote its Working Decisions to Confirmed Product Decisions unless Lyle explicitly approves those decisions.
New or materially changed Implementation Concepts identified from the meeting remain Proposed or Needs Confirmation until reviewed through the same lab-confirmation cycle or explicitly approved by Lyle.

When reviewing Implementation Concepts and codebase / implementation implications, separate product-facing concept gaps from engineering-facing uncertainties. Product-facing concept gaps go in the Lab Agenda or relevant product-facing open-question section. Engineering-facing uncertainties go in Pre Spec Implementation Questions and should not be placed on the Feature Lab agenda unless answering them requires a product decision.

Pre Spec Implementation Questions format:

Pre Spec Implementation Questions should be written from the running Implementation Concepts list. For each relevant concept, first draft the instructions you would give yourself to implement the concept as discussed and agreed to in the Labs. Use the current Pre-Spec, PMR, and current codebase to identify what remains missing, ambiguous, technically risky, or dependent on engineering confirmation.

Each Pre Spec Implementation Question should use this structure when possible:

Question:
- State the exact implementation fact that must be confirmed.

Why this blocks the spec:
- Explain what concept-level draft implementation instruction cannot be completed, validated, or safely carried into the future Feature Spec Sheet until this is answered.

Likely answers for engineering to confirm:
- Provide the top three most likely answers based on the current Implementation Concept, current Pre-Spec, PMR when relevant, and current codebase.
- Label the most likely / recommended path as option A when there is a clear front-runner.
- Each option must include an Instruction prompt if selected.
- The instruction prompt should be written as concept-level draft implementation instruction text that can be copied or adapted into the Pre-Spec and later condensed into the future Feature Spec Sheet if engineering confirms that option.

Option format:
A. [Most likely answer]
   Instruction prompt if selected:
   [Concept-level draft implementation instruction text for this implementation path.]

B. [Second likely answer]
   Instruction prompt if selected:
   [Concept-level draft implementation instruction text for this implementation path.]

C. [Third likely answer / custom implementation / product decision path]
   Instruction prompt if selected:
   [Concept-level draft implementation instruction text for this implementation path.]

Status:
- Pending engineering confirmation, Confirmed, Rejected, Product decision needed, or Superseded.

Rules:
- Do not use a separate “recommended default” section.
- Do not ask open-ended engineering questions when likely answer options can be inferred from current codebase and the Pre-Spec.
- Do not present product decisions as engineering-only choices. If an option changes the product behavior, mark it as Product decision needed.
- Code review is read-only for Feature Lab work.
- Keep product-facing unresolved questions in the Lab Agenda or product open-question sections; keep engineering-facing implementation facts in Pre Spec Implementation Questions.

## 8. Lab Agenda / Between-Meeting Prep Relationship

Lab Agendas should be generated from the current Pre-Spec and the latest Transcript Ingestion Review when they exist. Older references to "between-meeting prep" refer to this same meeting-facing Lab Agenda artifact.

A Lab Agenda is not a final spec, not a full pre-spec, and not a raw question inventory. It helps the meeting start in the right place, move through concepts in a useful order, and capture product decisions or clarifications needed to keep the Pre-Spec moving toward an implementable Feature Spec Sheet.

Lab Agenda questions should be driven by product-facing gaps that prevent the future Feature Spec Sheet from being implementable.

Standard structure:
1. Transcript pickup point, when the transcript states where to resume.
2. Decisions / working decisions from the last meeting.
3. Implementation Concepts Review, when useful.
4. Discussion blocks / clarification questions based on the last meeting.
5. Specific assigned follow-up / validation, when applicable.
6. Notes for future spec sheet draft, when applicable.

### 8.5 Artifact Boundary Preflight

Before creating, updating, or reconciling any Feature Lab artifact, identify the artifact type first and apply only that artifact's rules.

Required preflight statement, internal or explicit when helpful:
- Artifact type: Transcript Ingestion Review, Feature Working Model / Pre-Spec, Lab Kickoff Agenda, Lab Agenda, Spec Sheet Draft, Final Spec Sheet, PMR Update Proposal, UI Mockup Request, or other named artifact.
- Governing section: the section of this instruction document that controls the artifact.
- Output boundary: what belongs in this artifact and what must stay out.

Hard boundary rules:
1. Do not let Transcript Ingestion Review analysis leak into Lab Agendas.
2. Do not let Pre-Spec maintenance notes leak into Lab Agendas.
3. Do not let PMR commentary or PMR candidate discussion leak into Lab Agendas.
4. Do not let assistant-to-Lyle explanations, process justifications, or artifact-status notes leak into Lab Agendas.
5. Do not create a durable Google Doc for a Lab Agenda unless Lyle explicitly asks for one or the team has intentionally chosen a reusable running agenda doc.
6. By default, Lab Agendas are transient working artifacts and should be produced in canvas/in-chat.
7. If canvas is unavailable or unreliable, use one reusable agenda document for the lab series, either replacing the current agenda or adding the newest agenda at the top. Do not create a new Google Doc for every agenda unless explicitly requested.

Artifact boundary correction rule:
If Lyle identifies that an artifact is drifting into the wrong form, stop editing that artifact, restate the correct artifact type and boundary, update these instructions if needed, and regenerate from the correct artifact rules rather than patching the incorrect structure.

## 9. Lab Agenda Artifact Instructions

### 9.1 Lab Kickoff Agenda

Use a Lab Kickoff Agenda when Lyle is preparing for the first Feature Lab meeting in a new series and has provided initial scope, thoughts, examples, older feature references, suspected use cases, or current-state observations.

Lab Kickoff Agenda structure:
1. Feature Framing Summary.
2. Initial Scope Interpretation.
3. Known Examples / Current-State References to Review.
4. Recommended Starting Point.
5. Recommended Discussion Order.
6. Concept-by-Concept Discussion Framework.
7. Recommended Questions for Meeting 1.

Guardrails:
- Do not treat Lyle's initial scope notes as final decisions unless explicitly stated.
- Do not generate a full requirements model before the first meeting unless Lyle asks for direct pre-spec setup.
- Do prepare likely purpose language, working definitions, and discussion sequence.
- Do propose a starting point and ordering, but label both as recommendations.

### 9.2 Standard Lab Agenda Continuation Structure

Use this format after the first Feature Lab meeting or whenever there is an existing transcript, Transcript Ingestion Review, and current Feature Working Model / Pre-Spec.

A Lab Agenda should read like a live meeting agenda. Use this shape unless Lyle asks for another format:

1. Transcript Pickup Point
   - State where the transcript says the next meeting should resume.
   - If no explicit pickup point exists, use the most natural continuation from where the meeting stopped and what remains unresolved.

2. Decisions to Confirm / Working Decisions
   - Include only decisions newly made, corrected, or materially revised in the last meeting or review cycle.
   - Do not repeat older decisions that were merely reaffirmed.
   - Phrase as meeting confirmation items, not source-analysis notes.
   - Always present Decisions to Confirm / Working Decisions as a numbered list so participants and transcripts can refer to each decision by number. Do not use bullets for this section.

3. Implementation Concepts Review, when useful
   - Include this section when the concept model is new, changed, uncertain, or blocking spec readiness.
   - Keep this section product-facing, not engineering-facing.
   - Use it to review the pickup point, current confirmed Implementation Concepts, newly proposed concepts needing approval, and concepts needing split, merge, rename, deferral, or removal.
   - Ask only the product-facing questions needed to confirm the concept model.
   - Present each concept as IC-# — Concept Name followed by a concise product-facing description of what the concept covers. The description should be short enough for a live agenda, but specific enough for participants and the transcript to understand the concept without opening the Pre-Spec.
   - Use the current Pre-Spec description as the source. Condense it for meeting use without changing the concept boundary or introducing new implementation detail.
   - List each concept using its stable IC-# identifier (for example, IC-1, IC-2, IC-3). The IC-# identifier provides the referenceable numbering; do not add a separate numbered-list sequence unless the concepts do not yet have stable IC identifiers.
   - Before finalizing a Lab Agenda, perform a meeting-readiness formatting pass. Confirm clear title and purpose treatment, consistent heading hierarchy, numbered Decisions to Confirm, stable IC-# labels with concise product-facing descriptions, readable discussion-block separation, concise label formatting, consistent spacing, and clean boundaries between the current agenda and preserved prior agendas.

4. Discussion Blocks
   - Ordered blocks for the live meeting.
   - Each block should include:
     - block title;
     - core question;
     - decision needed;
     - optional short context when needed to start the conversation.
   - Do not include exhaustive “Clarify:” inventories unless Lyle asks for a question bank.

5. Specific Assigned Follow-Up / Validation
   - Include only actual assignments or validation owners established in the transcript or by Lyle.
   - If no owner was assigned, keep the topic as an open discussion block.

6. Notes for Future Spec Sheet Draft
   - Capture only items that affect eventual spec drafting, promotion readiness, implementation clarity, or confirmed Implementation Concepts.
   - Do not use this section for general meeting notes or artifact status updates.

Lab Agenda hard exclusions:
Do not include the following in a Lab Agenda:
- PMR commentary, PMR candidate analysis, or statements about whether a term belongs in PMR;
- Feature Pre-Spec Instructions commentary, process explanations, or notes about why an artifact rule exists;
- assistant-to-Lyle explanations such as “this is why I ordered it this way” or “this belongs in the pre-spec”;
- ingestion-review analysis, source hierarchy explanation, or evidence/classification language;
- full open-question inventories;
- engineering-facing Pre Spec Implementation Questions unless answering the question requires a product decision;
- spec promotion/readiness analysis unless a short note is directly needed to frame a meeting decision;
- durable-document management notes, canvas/tooling notes, or artifact-storage decisions;
- generic owner/department expectations such as “Needed from Product” or “Needed from Engineering” unless the follow-up was specifically assigned.

Lab Agenda tone rules:
- Agenda tone, not memo tone.
- Meeting-facing, not assistant-facing.
- Directive and concise.
- Use “Discuss,” “Confirm,” “Decide,” “Review,” and “Resolve.”
- Avoid “this means,” “this belongs,” “the pre-spec should,” “PMR candidate,” or “source basis” language unless Lyle explicitly requests that analysis.

Lab Agenda ownership / assignment rule:
- Clarification questions should be open-forum discussion prompts unless a specific person, team, or department was explicitly assigned follow-up ownership.
- Engineering validation needs should generally be captured in Pre Spec Implementation Questions, not in the Lab Agenda.
- Use "Specific assigned follow-up" only when there is an actual assigned owner or validation owner.

### 9.3 Lab Agenda Source Rules

Primary sources:
1. Current Feature Working Model / Pre-Spec, if one exists.
2. Latest confirmed Transcript Ingestion Review, if one exists.
3. Lyle's current scope notes or direct instructions.
4. Feature-specific source framing/reference tree.

Supporting sources:
- raw transcripts, for validation or pickup-point recovery;
- Feature Spec Sheet Instructions, for target-output / definition-of-done gaps;
- PMR, for reusable product conventions;
- current codebase, for implementation implications and validation questions;
- related specs/pre-specs, when the feature depends on another feature.

### 9.4 Lab Agenda Naming

Recommended artifact names:
- [Feature Name] - Lab Kickoff Agenda
- [Feature Name] - Lab Agenda - [Date]

## 10. Pre-Spec Maintenance Rules

After each Feature Lab meeting:
1. Add or identify the transcript/notes source.
2. Produce a Transcript Ingestion Review.
3. Let Lyle confirm/correct the review.
4. Update the Feature Working Model / Pre-Spec from the confirmed review.
5. Update the Feature-Specific Source Framing / Reference Tree if the source map changed.
6. Generate or update the Lab Agenda when useful.
7. Keep PMR updates proposed, not applied, until Lyle approves.
8. Use the current `uSked/wde-service` code to flag implementation implications and uncertainty, not to override product decisions. Check the latest `main` or `master` commit and cite relevant implementation files under the [code review standard](code-review-standard.md).
9. Maintain the running Implementation Concepts list and update concept statuses after each confirmed ingestion review or Lab decision.
10. Update draft implementation instructions for confirmed or active Implementation Concepts as product decisions mature.
11. Capture engineering-facing uncertainties in Pre Spec Implementation Questions rather than the Lab Agenda unless a product decision is required.
12. Use Feature Spec Sheet Instructions to evaluate what is still missing before the Pre-Spec can be promoted into an implementable Spec Sheet Draft.

## 11. Formatting Standards

Use the standard Feature Working Model / Pre-Spec formatting pattern:
- clean source framing first;
- status / purpose / scope before detailed content;
- heading hierarchy kept stable;
- body paragraphs remain body text;
- lists are cleanly numbered or bulleted;
- section numbering is updated immediately when sections are inserted or removed;
- exploratory language is kept out of final spec drafts;
- source status is explicit and current.

Draft and edit with cleanup in mind. Maintain clean numbering, heading hierarchy, spacing, list structure, punctuation consistency, and section boundaries as part of the edit rather than as a separate cleanup step.

## 12. Guardrails

Do not treat transcripts as final decisions unless the decision is clear.
Do not treat assumptions as decisions.
Do not duplicate the full project-wide source registry inside every Pre-Spec.
Do not create duplicate Pre-Spec documents when an existing feature Pre-Spec already exists.
Do not promote current-state defects into feature requirements unless Lyle explicitly says they belong in feature scope.
Do not move into Spec Sheet Draft until the Pre-Spec has a stable source map, confirmed decisions, unresolved questions, a current Implementation Concepts list, draft implementation instructions for confirmed concepts, and implementation implications clear enough for developers.

## 13. Source Framing / Reference Tree Procedure

Every Feature Working Model / Pre-Spec should maintain a feature-specific source map. Project Settings remains the authority for project-wide source hierarchy and reference registry. A feature Pre-Spec should reference Project Settings for project-wide sources and list only feature-specific sources inside the Pre-Spec.

Feature-specific sources may include:
1. Relevant Feature Lab transcripts / Gemini notes.
2. Transcript Ingestion Reviews.
3. Existing feature working-model / pre-spec / core-model docs.
4. Current feature spec drafts or final specs.
5. Existing mockups, mockup coverage docs, UI design briefs, QA/test planning docs, or design review artifacts directly related to the feature.
6. Directly related cross-feature specs, pre-specs, or final specs.
7. Feature-specific source drafts or supporting docs provided by Lyle.

Project-wide references should be named in a feature Pre-Spec only when directly implicated by:
1. a feature-specific interpretation;
2. a conflict or source-priority issue;
3. a proposed PMR update;
4. a codebase implementation implication;
5. a design-guide or UI/mockup implication;
6. a source-priority exception.

## 14. Pre-Ingestion Source Scope Check

Before analyzing a new Feature Lab transcript, perform a source scope check:
1. Confirm the feature/topic.
2. Confirm the meeting/transcript date.
3. Confirm whether the meeting starts a new feature or continues an existing feature.
4. Confirm the relevant feature chat/workspace.
5. Identify the current Feature Working Model / Pre-Spec, if one exists.
6. Review the Pre-Spec's Feature-Specific Source Framing / Reference Tree and treat it as the canonical feature source map.
7. Search or check for relevant new feature-specific sources.
8. Identify whether any project-wide references are directly implicated.
9. Identify source-scope changes or state: No source-scope update needed.

## 15. Transcript-to-Pre-Spec Reconciliation Workflow

After a Transcript Ingestion Review is complete and Lyle has reviewed or confirmed it, use the review as the work order for the Pre-Spec update.

Do not update the Pre-Spec directly from transcript content unless Lyle explicitly asks for direct update.

Reconciliation steps:
1. Open the current Pre-Spec and confirm its source-framing status.
2. Compare the Transcript Ingestion Review against the existing Pre-Spec.
3. Add confirmed decisions to the appropriate working-model sections.
4. Add likely decisions as "needs confirmation," not final decisions.
5. Add product-facing open questions to the relevant open-question or Lab Agenda section.
6. Update conflicts, reversals, refinements, or stale sections.
7. Add terminology/product-model markers where they belong.
8. Add PMR candidates as proposed updates only.
9. Add or update Implementation Concepts introduced, changed, confirmed, deferred, removed, split, merged, or renamed by the ingestion review.
10. Update draft implementation instructions for affected Implementation Concepts.
11. Add codebase / implementation implications as concept-level validation items or Pre Spec Implementation Questions.
12. Separate product-facing concept gaps from engineering-facing implementation questions before updating the Lab Agenda.
13. Link Pre Spec Implementation Questions back to the relevant Implementation Concept when possible.
14. Update UI/mockup needs where applicable.
15. Update source framing/reference tree.
16. Update the Lab Agenda if needed, including Implementation Concept Review items when useful.
17. Run a formatting and numbering pass after edits.

## 16. Pre-Spec Update Workflow

A Pre-Spec update should usually follow this order:
1. Update metadata/status/source basis.
2. Update source framing/reference tree.
3. Update decision log or confirmed-decision section.
4. Update working model sections.
5. Update the running Implementation Concepts list.
6. Update concept-level draft implementation instructions.
7. Update product-facing open questions and clarification questions.
8. Update Pre Spec Implementation Questions generated from concept-level instruction gaps.
9. Update PMR candidates, if any.
10. Update UI/mockup tracking, if any.
11. Update the Lab Agenda, if applicable, using only product-facing questions and meeting-facing topics, including Implementation Concept Review items when useful.
12. Run formatting stabilization.

## 17. Implementation Concepts

Purpose:
Implementation Concepts are the bridge between Feature Lab product discussion and the eventual implementation spec.

They are maintained inside the Feature Working Model / Pre-Spec while the feature is still active so that implementation thinking develops in parallel with product decisions, rather than being reconstructed at the end during spec drafting.

The working flow is:
Transcript -> decisions / gaps / implementation concepts -> Pre-Spec -> Lab Agenda / implementation questions -> Spec Sheet

Definition:
An Implementation Concept is a feature-specific build concept that must be understood as a coherent unit in order for the implementation agent or engineering to produce an accurate implementation plan or implementation output.

An Implementation Concept usually connects Lab-confirmed product intent to one or more of the following:
- WDE/Usked 2.0 surfaces;
- user-facing behavior;
- system behavior;
- data or configuration requirements;
- permissions or visibility rules;
- workflow / lifecycle rules;
- UI or interaction patterns;
- technical constraints;
- open engineering confirmations.

An Implementation Concept is not merely a generic category, broad product theme, or engineering task.

What is not an Implementation Concept:
Do not use generic headings like these as Implementation Concepts by default:
- Data
- UX
- Permissions
- Backend
- Frontend
- Requirements
- Edge cases
- Actions
- Workflow
- Implementation notes

Those may appear inside an Implementation Concept when relevant, but they are not usually good concept names.

A good Implementation Concept should name the specific feature concept the implementation agent must understand.

For example, in the History Tabs feature, likely Implementation Concepts included:
- Usked Places
- Timeline Events
- Log Event Types
- Log Event Type Roles
- Timeline Context View
- Quick View For More Details
- Cold Storage Considerations

These are stronger than generic headings because they name coherent parts of the feature's implementation model.

When to identify Implementation Concepts:
Implementation Concepts should be identified during Transcript Ingestion Review and maintained in the Pre-Spec.

During each transcript ingestion, look for:
- a new feature behavior that appears to require its own implementation model;
- a WDE/Usked 2.0 surface that the feature depends on;
- a concept that will likely become a heading in the final implementation spec;
- a recurring product idea that controls data, permissions, display, workflow, configuration, or interaction behavior;
- a product decision that implies a new or changed module/table, context, view, action, wizard, script, route, TSA, field, role mapping, or configuration record;
- a concept that would create implementation risk if left buried in prose;
- a concept that the implementation agent would likely need to reason about separately when producing an implementation plan.

Implementation Concept statuses:
Each Implementation Concept in the Pre-Spec should have a status.

Recommended statuses:
- Candidate - identified from transcript/source material but not yet confirmed.
- Needs Lab Confirmation - product-facing confirmation is needed before the concept should be treated as active.
- Confirmed - accepted as part of the feature model.
- Needs Engineering Confirmation - product concept is stable, but implementation facts are unresolved.
- Draft Instructions In Progress - concept is confirmed enough to begin drafting implementation instructions.
- Ready for Spec Draft - concept has enough confirmed instruction detail to carry into the Feature Spec Sheet.
- Deferred / Out of Scope - concept is recognized but not part of current feature scope.
- Removed / Superseded - concept was rejected, merged, renamed, or replaced.

Running Pre-Spec structure for each Implementation Concept:
Each active Implementation Concept should include the relevant subset of the following fields.

Do not force empty fields, but do maintain enough information for the concept to support Lab Agenda review, Pre Spec Implementation Questions, and eventual spec drafting.

Concept Name:
The feature-specific name of the concept.

Status:
Candidate, Needs Lab Confirmation, Confirmed, Needs Engineering Confirmation, Draft Instructions In Progress, Ready for Spec Draft, Deferred / Out of Scope, or Removed / Superseded.

Source Basis:
Transcript, Pre-Spec section, Lyle instruction, PMR reference, current codebase reference, mockup, related spec, or engineering feedback that introduced or changed the concept.

Lab-Confirmed Product Decisions:
Decisions from Feature Lab that define what this concept must do or not do.

Draft Implementation Instructions:
The instructions you would give yourself to implement this concept as discussed and agreed to in the Labs.

Relevant WDE / Usked 2.0 Surfaces:
Known or likely surfaces involved, using current codebase terminology where possible.

Examples include module/table, record, field, context, context column, context view, detail view, menu item, place, tab, subtab, fifth element, context action, row action, page/GAP action, wizard, Lua script, TSA, trigger, sequence, action, Handlebars view, frontend JavaScript behavior, backend route, notification/email/integration behavior, package/config behavior, or builder configuration.

Known Assumptions:
Assumptions currently being carried, clearly labeled as assumptions rather than decisions.

Product-Facing Gaps:
Questions that require Lab discussion, Lyle/Marvin direction, workflow clarification, UX choice, policy decision, or scope confirmation.

Engineering-Facing Gaps / Pre Spec Implementation Questions:
Questions that can be answered by engineering outside Feature Lab and should not be placed on the Lab Agenda unless they require a product decision.

Related Pre Spec Implementation Questions:
Links or references to the engineering-facing questions generated from this concept.

Last Reviewed / Last Changed:
Meeting date, transcript, or update pass where the concept was last reviewed or changed.

Draft Implementation Instruction rules:
Draft implementation instructions belong in the Pre-Spec when they are tied to an active Implementation Concept.

For each concept, draft the instructions you would give yourself to implement the concept as discussed and agreed to in the Labs.

Use:
- current Pre-Spec decisions;
- Lab-confirmed product direction;
- PMR conventions, when relevant;
- current codebase guidance, when implementation terminology or likely surfaces are needed;
- feature-specific source material.

Draft implementation instructions should:
- use precise WDE/Usked 2.0 terminology where known;
- describe what should be built, changed, reused, renamed, configured, shown, hidden, filtered, triggered, or tested;
- separate confirmed instructions from assumptions;
- identify the WDE/Usked 2.0 surfaces involved;
- state permission, visibility, data, configuration, placement, interaction, and display rules when relevant;
- avoid general product prose when a specific implementation instruction can be written;
- avoid over-prescribing code-level choices that engineering should decide;
- avoid inventing missing product decisions;
- avoid including credentials, private paths, server details, connection strings, or other sensitive implementation details.

If the instruction cannot be completed because a product decision is missing, create or update a product-facing Lab Agenda question.

If the instruction cannot be completed because an engineering fact is missing, create or update a Pre Spec Implementation Question.

Split / merge / rename guidance:
During Pre-Spec maintenance, review whether Implementation Concepts should be split, merged, renamed, deferred, or removed.

Split a concept when:
- it contains more than one coherent build concept;
- it mixes product-facing workflow with unrelated technical behavior;
- it creates multiple unrelated implementation questions;
- one part is confirmed and another part remains uncertain;
- one part belongs in current scope and another part is deferred.

Merge concepts when:
- they always move together;
- they describe the same WDE/Usked 2.0 surface or behavior from different angles;
- keeping them separate would duplicate instructions or questions.

Rename a concept when:
- the name is too generic;
- the name does not match Lab language;
- the name does not match WDE/Usked 2.0 terminology;
- the name would confuse the implementation agent or engineering during implementation planning.

Defer or remove a concept when:
- the Lab excludes it from scope;
- it belongs to a future feature;
- it is only a supporting note, not a build concept;
- it was introduced by speculation and not confirmed.

Relationship to Lab Agendas:
Lab Agendas should review Implementation Concepts when the concept model is new, changed, uncertain, or blocking spec readiness.

A Lab Agenda may include:
- the pickup point;
- decisions made since the last review;
- current confirmed Implementation Concepts;
- newly proposed Implementation Concepts needing approval;
- concepts needing split, merge, rename, deferral, or removal;
- product-facing questions needed to confirm the concept model.

Do not use Lab Agenda time for engineering-facing implementation questions unless answering the question requires a product decision.

Relationship to Pre Spec Implementation Questions:
Pre Spec Implementation Questions should be generated from the running Implementation Concepts list.

For each concept:
1. Review the concept as discussed and agreed to in the Labs.
2. Draft the instructions you would give yourself to implement that concept.
3. Check the PMR and current codebase where relevant.
4. Identify what is missing, ambiguous, technically risky, or dependent on engineering confirmation.
5. Convert those gaps into Pre Spec Implementation Questions.

Do not ask broad exploratory engineering questions. Ask only the questions needed to complete, validate, or correct the draft implementation instructions for the concept.

Relationship to Feature Spec Sheet Drafting:
The Feature Working Model / Pre-Spec should progressively build the implementation concept model before spec drafting begins.

When the feature is ready for a Spec Sheet Draft, the confirmed Implementation Concepts and their draft implementation instructions should become the primary source for Chapter 2: the Implementation Spec.

The final spec sheet should not invent a new concept model at the end. It should condense, clean, and verify the concept model already curated in the Pre-Spec.

### 17.1 Post-Lab Product Decisions

Purpose:
Allow a product decision discovered or resolved during Pre-Spec review to become authoritative without falsely attributing it to a Feature Lab transcript.

Use this decision type when:
- Pre-Spec review, mockup review, implementation vetting, or another post-lab review exposes a product-facing gap that the transcripts do not resolve;
- Lyle makes or approves the product decision outside the Feature Lab series; and
- the decision does not require another Feature Lab meeting under the clarification-meeting threshold.

Statuses:
- Proposed Post-Lab Product Decision — a recommended or user-proposed direction awaiting Lyle’s explicit approval.
- Confirmed Post-Lab Product Decision — an explicitly approved direction that may be incorporated into the Pre-Spec, affected Implementation Concepts, draft implementation instructions, mockup requirements, and eventual Spec Sheet Draft.
- Superseded Post-Lab Product Decision — an earlier post-lab decision replaced by a later approved decision.

Required decision record:
1. Decision status.
2. Decision authority.
3. Decision date.
4. Source conversation, comment, review artifact, or other traceable source.
5. Reason the decision arose.
6. Transcript relationship: directly supported, consistent but not directly discussed, not addressed, or in conflict.
7. Approved product behavior.
8. Affected Pre-Spec sections, Implementation Concepts, draft implementation instructions, questions, mockups, PMR candidates, or downstream artifacts.
9. Approval or supersession history.

Authority and traceability rules:
- A Proposed Post-Lab Product Decision is not a confirmed requirement until Lyle explicitly approves it.
- A Confirmed Post-Lab Product Decision is authoritative for the feature even when no transcript directly supports it.
- Never label or imply that a Post-Lab Product Decision was Lab-confirmed or transcript-supported when it was not.
- Record the decision in the feature’s current Pre-Spec; do not create a second source of truth unless Lyle explicitly requests a separate decision artifact.
- If the decision conflicts with a transcript, existing confirmed decision, PMR convention, related spec, or another authoritative source, surface the conflict and obtain explicit resolution before incorporation.
- If the decision establishes a reusable product convention, record a PMR candidate; do not update the PMR without Lyle’s approval.
- If the decision materially changes the system model, permissions, object relationships, data model, core UX flow, implementation-facing scope, or another participant’s decision authority, recommend a clarification meeting rather than treating it as a routine post-lab decision.

Relationship to Implementation Concepts:
Update each affected Implementation Concept’s Source Basis to identify the Confirmed Post-Lab Product Decision and its traceable source. Keep Lab-Confirmed Product Decisions separate from Post-Lab Product Decisions so provenance remains visible during spec drafting.

## 18. Pre Spec Implementation Questions

Purpose:
Pre Spec Implementation Questions are the running engineering-facing question list inside the Feature Working Model / Pre-Spec. They capture implementation uncertainties that arise while drafting concept-level implementation instructions from the current Implementation Concepts list. They may originate during transcript ingestion, PMR review, current codebase review, Feature Spec Sheet Instructions gap review, or pre-spec drafting, but should not consume Feature Lab agenda time unless they require a product decision.

Core rule:
Separate product-facing questions from engineering-facing questions.

Product-facing questions belong in the Lab Agenda or the relevant product-facing open-question section when they require Lyle, Marvin, Feature Lab discussion, workflow clarification, UX choice, policy decision, or scope confirmation.

Engineering-facing questions belong in Pre Spec Implementation Questions when they can be answered by engineering outside Feature Lab.

Key references:
1. Feature Spec Sheet Instructions, for target-output / definition-of-done gaps that must be resolved before implementation handoff.
2. PMR, for reusable product conventions, terminology, permissions, recipient patterns, action patterns, object context, messaging distinctions, and product-model assumptions.
3. current codebase, for likely WDE/Usked 2.0 implementation surfaces and technical architecture implications. Use repository CLAUDE.md and relevant documents/ files for navigation, then inspect implementation code at the current main or master commit.

When to add a Pre Spec Implementation Question:
Add a question when:
1. an Implementation Concept has draft implementation instructions that cannot be completed, validated, or safely carried forward without engineering input;
2. Feature Spec Sheet Instructions indicate the future spec will need implementation detail that the current Pre-Spec cannot yet support;
3. the transcript or Pre-Spec implies a likely WDE/Usked 2.0 surface, but the exact approach is unclear;
4. current codebase suggests multiple possible implementation paths or leaves uncertainty about the correct implementation surface;
5. PMR conventions appear relevant, but engineering must confirm how they are supported technically;
6. a concept may depend on existing modules/tables, fields, contexts, row actions, page/GAP actions, wizards, Lua scripts, TSAs, Handlebars views, frontend JavaScript, backend routes, notifications, email, integrations, or builder configuration;
7. the question can be answered by engineering without requiring Feature Lab product discussion.

Recommended format:
1. Related Implementation Concept.
2. Draft implementation instruction gap.
3. Question.
4. Why it matters.
5. Likely reference area: current Pre-Spec, PMR, current codebase, Feature Spec Sheet Instructions, or any combination.
6. Possible implementation surface.
7. Source trigger.
8. Engineering response: blank until answered.
9. Resolution / Pre-Spec impact.

### 18.1 Temporary Implementation Feedback Handling Rule

For now, do not create a separate Implementation Questions instruction document. Keep the feedback workflow lightweight while the team observes the first one or two rounds of engineering responses to Pre Spec Implementation Questions.

Implementation feedback should live in the relevant feature Pre-Spec unless Lyle explicitly asks for a separate artifact. Capture engineering responses in the Engineering response field for each question, then update the Resolution / Pre-Spec impact field to show whether the answer changes the Pre-Spec, updates a related Implementation Concept, changes draft implementation instructions, confirms the current direction, affects the eventual Spec Sheet Draft, creates a PMR candidate, or suggests a codebase follow-up.

Watch for recurring feedback patterns, including repeated engineering answer formats, repeated implementation surfaces, common uncertainty types, repeated source/freshness issues in current codebase, and whether responses arrive as comments, chat notes, implementation review notes, issue tickets, or direct engineering replies.

Revisit whether a standalone Implementation Questions Instructions document is needed after one or two engineering feedback cycles. Create a separate instruction document only if the feedback workflow becomes stable enough to require reusable rules for intake, triage, status, engineering response format, resolution handling, source updates, or cross-feature implementation-question conventions.

## 19. UI / Mockup Tracking Inside the Pre-Spec

The Feature Working Model / Pre-Spec is the canonical internal place to track UI Deliverables / Mockup Requirements while a feature is being shaped.

Mockups may be required when the feature introduces or materially changes:
1. a screen or page;
2. navigation pattern;
3. context/table/card/detail view;
4. wizard flow;
5. modal;
6. fifth-element detail surface;
7. badge/count behavior;
8. recipient-selection pattern;
9. permission-dependent visibility;
10. interaction state that cannot be clearly specified in text alone.

Pre-Spec UI/mockup tracking should include:
1. whether mockups are required: Yes / No / TBD;
2. why they are or are not required;
3. required screens/components/states;
4. fidelity needed;
5. approval owner;
6. status;
7. spec sections blocked by missing UI decisions;
8. Design Guide impacts or reusable UI decisions.

## 20. Promotion from Pre-Spec to Spec Sheet Draft

A feature is ready to move from Feature Working Model / Pre-Spec to Spec Sheet Draft when the Pre-Spec has been checked against Feature Spec Sheet Instructions and:
1. The source framing/reference tree is current.
2. Relevant transcripts have been ingested or explicitly marked as not required.
3. Confirmed decisions are separated from likely decisions and open questions.
4. Scope boundaries are stable enough for implementation drafting.
5. The product model is coherent enough to write developer-facing requirements.
6. The running Implementation Concepts list is current.
7. Candidate or newly proposed Implementation Concepts are confirmed, deferred, removed, or explicitly marked as blockers.
8. Confirmed Implementation Concepts have draft implementation instructions sufficient to support Chapter 2 of the future Spec Sheet Draft.
9. Major permission, workflow, lifecycle, messaging, data, and edge-case gaps are either answered or explicitly listed as open questions.
10. codebase / implementation implications have been reviewed enough to avoid vague or impossible implementation language, and engineering-facing uncertainties have been captured in Pre Spec Implementation Questions where applicable.
11. UI/mockup needs are resolved, not required, or explicitly marked as blocking/open.
12. Lyle has approved or requested movement into spec drafting.

When drafting the Spec Sheet Draft:
- Use the current Pre-Spec as the primary working source.
- Use confirmed Implementation Concepts and their draft implementation instructions as the primary source for Chapter 2 of the Spec Sheet Draft.
- Use Feature Spec Sheet Instructions as the target-output / definition-of-done reference.
- Use transcripts for validation, traceability, conflict resolution, and clarification.
- Do not invent new Implementation Concepts during final spec drafting without flagging the gap for Lyle review.
- Do not include exploratory meeting history.
- Include unresolved open questions only when they are still relevant to implementation or approval.

## 21. Canvases, Prep Docs, and Derivative Artifacts

Canvases and prep docs are working spaces. They should not become a second source of truth.

Use a canvas or prep artifact when:
1. the topic is complex and needs iterative shaping before being added to the Pre-Spec;
2. the team needs a Lab Agenda or meeting guide;
3. a subset of content needs to be easier to review or revise separately;
4. a future spec section needs to be drafted before insertion into the Google Doc.

After the canvas/prep content is accepted, move the approved language into the Pre-Spec or spec draft as appropriate.

Derivative artifacts should generally use the current Pre-Spec as their primary source, including UI Mockup Request / Design Briefs, mockup coverage docs, QA/test planning docs, design review notes, implementation review notes, handoff summaries, and support artifacts.

## 22. What Stays Out of the Pre-Spec

Do not include:
1. raw transcript dumps;
2. full meeting chronology unless needed for decision traceability;
3. unfiltered brainstorms;
4. unrelated current-state defects;
5. implementation secrets or sensitive infrastructure details;
6. final spec language before decisions are stable;
7. full project-wide source registry;
8. detailed PMR text unless it is a proposed PMR candidate;
9. broad engineering handoff lists that are not tied to Implementation Concepts, feature questions, validation needs, draft implementation instruction gaps, or Pre Spec Implementation Questions;
10. code-level engineering plans that go beyond concept-level draft implementation instructions unless Lyle explicitly requests them;
11. old exploratory content after it has been resolved, superseded, or promoted.

## 23. Relationship to Project Settings, Feature Spec Sheet Instructions, PMR, and current codebase

Project Settings:
Project Settings remains the project-wide authority for artifact lifecycle, source priority, command registry, configured source locations, and cross-document routing.

Feature Pre-Spec Instructions:
This document is the detailed operating manual for Feature Working Model / Pre-Spec work.

Feature Spec Sheet Instructions:
spec-sheet-instructions.md
Use Feature Spec Sheet Instructions as the target-output and definition-of-done reference for implementable spec sheets. Pre-Specs, Lab Agendas, Implementation Concepts, draft implementation instructions, and Pre Spec Implementation Questions should be shaped by what the eventual spec sheet must contain. Feature Spec Sheet Instructions assume the Implementation Concepts list has already been curated in the Pre-Spec and should use continuity checks rather than redefine the concept model.

PMR:
Use the PMR for reusable Usked product/system conventions. A Pre-Spec may propose PMR candidates, but the PMR is not updated until Lyle approves.

Current codebase:
Use the latest `main` or `master` branch of `uSked/wde-service` to identify likely implementation surfaces and uncertainty. Its `CLAUDE.md` and relevant `documents/` files help locate code; inspect implementation files and record the commit before making a technical claim. Code does not override Feature Lab product decisions. Name code files in a Pre-Spec only when they directly inform a feature-specific implication or question.

## 24. Recommended Project Settings Pointer

Feature Pre-Spec Instructions:
pre-spec-instructions.md
Reusable instruction document for initializing, maintaining, reconciling, formatting, and promoting Feature Working Model / Pre-Spec artifacts.

Feature Spec Sheet Instructions:
spec-sheet-instructions.md
Reusable instruction document defining the target output, required structure, and definition of done for implementable Feature Spec Sheets.

## 25. Closeout Status

Migration draft. This document retains the Implementation Concept, draft instruction, implementation-question, retrospective reconstruction, and promotion rules. Its header and Git history become the instruction freshness source after cutover.
