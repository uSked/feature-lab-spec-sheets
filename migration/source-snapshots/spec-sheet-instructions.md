# Source snapshot: spec-sheet-instructions

Source: https://docs.google.com/document/d/1GfK0HnXye0cSW5VN8U7owAHx39muEQhYfMNre5ceHvE
Captured: 2026-09-24
Status: Migration reference only. Do not treat this copy as the active operating guide.

---

1. Feature Spec Sheet Instructions
   2. Last Updated: 2026-06-04 (America/New_York)
   3. Updated By: Lyle / ChatGPT-assisted
   4. Change Summary: Added Pre-Spec continuity checks for confirmed Implementation Concepts, clarified Chapter 2 handoff from Pre-Spec draft implementation instructions, and reinforced that Feature Pre-Spec Instructions own the Implementation Concept model.
   5. Authority / Use: Project-wide instruction document defining the target output, implementation-readiness expectations, drafting standards, and definition of done for Usked Feature Spec Sheets.
   6. Status: Current; under active refinement based on History Tabs engineering implementation feedback.
   7. Update Permission: Editable by Lyle / ChatGPT-assisted at Lyle's direction. Do not update automatically from engineering implementation feedback without Lyle approval.
   8. Primary Governing Source: Feature Lab Spec Sheets — Project Settings (Current).
   9. Directly Related Instruction Docs: Feature Pre-Spec Instructions; PMR; Agents Docs folder / root AGENTS.md and AGENTS-CHANGELOG.md when implementation guidance is needed.
   10. Freshness Source: This document header is the freshness source for this instruction document. Project Settings remains the registry checkpoint.
   11.    12. 0. Freshness and Use Controls
   13. Before using this document for Spec Sheet Draft or Final Spec Sheet work:
   14. 1. Confirm the document title is Feature Spec Sheet Instructions.
   15. 2. Check Last Updated, Change Summary, Status, Authority / Use, and Update Permission.
   16. 3. Confirm Project Settings is current and still points to this document for Spec Sheet Draft / Final Spec Sheet work.
   17. 4. Use this document as the target-output / definition-of-done reference for implementable Feature Spec Sheets.
   18. 5. Use Feature Pre-Spec Instructions for Pre-Spec, Lab Agenda, Transcript Ingestion Review, and Pre Spec Implementation Question workflows.
   19. 6. Use PMR for reusable Usked product conventions and Agents Docs for WDE/Usked 2.0 implementation-vetting references.
   20. 7. When Agents Docs informs spec guidance, check root AGENTS.md, AGENTS-CHANGELOG.md, and the relevant focused doc's Last updated line before relying on that information.
   21. 8. Treat engineering implementation feedback as process evidence only after Lyle approves it for use in this instruction document.
   22. 9. Do not treat full engineering implementation conversations as standing instruction sources unless Lyle explicitly promotes them.
   23. 10. Do not copy credentials, private paths, server details, connection strings, SSH/database details, or other sensitive infrastructure details into feature specs or user-facing summaries.
   24.    25. 1. Purpose and Target Output Model
   26. 1.1 Purpose
   27. Feature Spec Sheets are the final development-facing output of the Feature Lab Spec Sheets workflow.
   28.    29. A Feature Spec Sheet exists to translate confirmed product decisions into a clear, compact, implementable build target for Usked engineering and AI-assisted development.
   30.    31. The spec sheet should be optimized for AI-assisted implementation and engineering review. It should not be optimized as a long human product narrative.
   32.    33. 1.2 Two-Chapter Spec Sheet Model
   34. Feature Spec Sheets should use two main chapters:
   35.    36. Chapter 1: Dev Review Cover Sheet
   37. The cover sheet is the human-facing review layer. It exists so a developer, Lyle, QA, or another reviewer can quickly check Claude's plan and output against the approved product intent, source basis, scope, and known blockers.
   38.    39. Chapter 2: Claude-Ingestible Implementation Spec
   40. The implementation spec is the core build artifact. It exists to give Claude, engineering, or another implementation agent only the information needed to produce an implementation plan, implement the feature, or review implementation readiness.
   41.    42. The Claude-ingestible implementation spec should be compact, precise, and written in WDE/Usked 2.0 terminology. Less is more. Do not add general product-description language when a specific WDE/2.0 implementation term or surface can be named.
   43.    44. 1.3 Primary Design Principle
   45. The Feature Spec Sheet should separate human review context from implementation instructions.
   46.    47. The human cover sheet may explain why the feature exists, what sources were used, what is approved, and what should be checked during review.
   48.    49. The implementation spec should give Claude exactly what it needs to do the work: build target, WDE/Usked 2.0 surfaces, behavior, configuration/data requirements, constraints, open confirmations, and acceptance/test requirements.
   50.    51. 1.4 Relationship to Other Reference Documents
   52. Project Settings defines the project-wide lifecycle, source priority, configured reference locations, and artifact routing.
   53.    54. Feature Pre-Spec Instructions define how Feature Working Model / Pre-Spec artifacts are initialized, maintained, reconciled after transcript ingestion, used to identify and curate Implementation Concepts, used to draft concept-level implementation instructions, used to generate Lab Agendas and Pre Spec Implementation Questions, and promoted toward spec drafting.
   55.    56. Feature Spec Sheet Instructions define the target output that the Pre-Spec process is trying to produce.
   57.    58. PMR defines reusable Usked product/system conventions that should inform spec language without cluttering individual specs.
   59.    60. Agents Docs is the current folder-based WDE/Usked 2.0 technical architecture and implementation reference. Use it for implementation clarity, not as a product-decision source. Root AGENTS.md is the navigation hub; AGENTS-CHANGELOG.md and relevant focused docs under documents/ must be checked for freshness when implementation guidance is needed.
   61.    62. 1.5 What This Document Governs
   63. This document governs:
   64. 1. the two-chapter Feature Spec Sheet model;
   65. 2. the difference between human review context and Claude-ingestible implementation instructions;
   66. 3. definition of implementable / implementation-ready;
   67. 4. WDE/2.0 terminology precision expectations;
   68. 5. required spec structure at the chapter level;
   69. 6. Pre-Spec readiness signals for promotion into Spec Sheet Draft;
   70. 7. final cleanup and definition of done.
   71.    72. 1.6 What This Document Does Not Govern
   73. This document does not replace:
   74. 1. Project Settings for project-wide routing and source priority;
   75. 2. Feature Pre-Spec Instructions for transcript ingestion, Pre-Spec maintenance, Implementation Concept definition and curation, draft implementation instruction rules, Lab Agenda generation, or Pre Spec Implementation Questions;
   76. 3. PMR for reusable product conventions;
   77. 4. Agents Docs for current WDE/Usked 2.0 technical architecture;
   78. 5. engineering-owned implementation planning, migration planning, or code-level execution workflows.
   79.    80. 2. Definition of Implementable / Implementation-Ready
   81. 2.1 Implementable Spec Definition
   82. A Feature Spec Sheet is implementable when the Claude-ingestible implementation spec is specific enough for Claude or engineering to derive a credible implementation plan without reconstructing product intent from transcripts or asking avoidable product questions.
   83.    84. An implementable spec should include:
   85. 1. clear build target and scope;
   86. 2. confirmed product decisions separated from open questions;
   87. 3. precise WDE/Usked 2.0 terminology;
   88. 4. user-facing and system behavior;
   89. 5. likely WDE/Usked 2.0 surfaces;
   90. 6. data, configuration, permission, and visibility requirements;
   91. 7. constraints and known non-goals;
   92. 8. setup, acceptance, and test requirements;
   93. 9. explicit unresolved product blockers or engineering confirmations.
   94.    95. 2.2 What Engineering Should Be Able to Derive
   96. The implementation spec should provide enough structure for engineering to derive a credible implementation plan without rediscovering product intent.
   97.    98. The implementation spec should make clear:
   99. 1. feature goal and user-facing behavior;
   100. 2. launch points and object context;
   101. 3. likely modules/tables, records, fields, relationships, contexts, context columns, views, actions, routes, scripts, or configuration surfaces;
   102. 4. permission and visibility expectations;
   103. 5. setup and testing expectations;
   104. 6. open implementation confirmations still needed.
   105.    106. 2.3 What a Spec Should Not Over-Prescribe
   107. A Feature Spec Sheet should not attempt to become the full engineering implementation plan.
   108.    109. Do not over-prescribe:
   110. 1. code-level architecture unless explicitly required;
   111. 2. exact implementation mechanics that engineering should choose;
   112. 3. sensitive infrastructure details;
   113. 4. engineering-owned handoff or session-continuity workflows;
   114. 5. general descriptive product language that makes Claude infer implementation from prose.
   115.    116. 2.4 Open Questions / Blockers Standard
   117. Open questions should be explicit. They should not be hidden inside requirements.
   118.    119. Product questions should identify the product decision needed.
   120.    121. Engineering questions should identify the implementation confirmation needed.
   122.    123. A spec can remain useful with explicit unresolved blockers, but it should not present unresolved blockers as final requirements.
   124.    125. 3. Source Basis and Drafting Authority
   126. 3.1 Primary Drafting Source
   127. Once a current Feature Working Model / Pre-Spec exists, use it as the primary source for drafting a Spec Sheet Draft.
   128.    129. Before drafting, verify that the Pre-Spec contains a current Implementation Concepts list and draft implementation instructions for confirmed concepts. Feature Pre-Spec Instructions own the definition, status model, curation process, and draft instruction rules for Implementation Concepts.
   130.    131. If the Pre-Spec does not contain a current Implementation Concepts list, or if the list appears stale, incomplete, or unresolved, flag the gap before drafting Chapter 2. Do not invent new Implementation Concepts during final spec drafting without surfacing the gap for Lyle review.
   132.    133. 3.2 Supporting Sources
   134. Use Feature Lab transcripts for validation, conflict resolution, reversals, and traceability, not as the primary drafting source when a current Pre-Spec exists.
   135.    136. Use the PMR for reusable product conventions, terminology, menu/action patterns, permissions, messaging distinctions, recipient-selection patterns, and object-context rules.
   137.    138. Use Agents Docs for likely WDE/Usked 2.0 implementation surfaces, terminology, and implementation-vetting questions.
   139.    140. Use current feature mockups, UI briefs, QA/test planning docs, implementation review notes, and related cross-feature specs as supporting references according to the feature source map.
   141.    142. 3.3 Agents Docs Freshness Rule
   143. When Agents Docs is used, check root AGENTS.md, AGENTS-CHANGELOG.md, and the relevant focused doc's Last updated line before relying on the information.
   144.    145. Prefer the most current relevant focused doc over older or broader language when the two conflict. Flag meaningful discrepancies for Lyle rather than silently resolving them.
   146.    147. 3.4 Engineering Feedback as Process Evidence
   148. Engineering implementation feedback may be used to improve this instruction document only after Lyle approves the feedback as process evidence.
   149.    150. Use mapped feedback artifacts carefully:
   151. 1. Spec input given to an implementation agent may inform target spec-sheet shape.
   152. 2. Follow-up implementation questions may inform future Pre Spec Implementation Questions.
   153. 3. Generated implementation plans may inform the definition of implementation-ready.
   154. 4. Full engineering conversations are supporting evidence and traceability, not standing instruction sources unless Lyle explicitly promotes them.
   155.    156. 3.5 Sensitive Implementation Detail Guardrail
   157. Do not include credentials, passwords, SSH keys or paths, private server paths, developer-specific database names, connection strings, or other sensitive implementation details in spec sheets or user-facing summaries.
   158.    159. 4. Required Feature Spec Sheet Structure
   160. This section now defines the required chapter-level structure. The detailed contents of each chapter will be refined in later passes.
   161.    162. 4.1 Chapter 1: Dev Review Cover Sheet
   163. Purpose:
   164. The Dev Review Cover Sheet is the human-facing review layer. It exists so a developer, Lyle, QA, or another reviewer can check Claude's plan and output against the approved product intent, source basis, scope, known blockers, and testing expectations.
   165.    166. Use the cover sheet to capture review context, not implementation instructions. Anything Claude needs in order to build should live in Chapter 2: Claude-Ingestible Implementation Spec.
   167.    168. Required cover sheet sections:
   169. 1. Feature / Status Snapshot
   170. 2. Source Basis
   171. 3. Feature Summary
   172. 4. Scope / Non-Scope
   173. 5. Approved Product Decisions
   174. 6. Feature-Specific Review Risks / Watchouts
   175. 7. Known Blockers / Open Review Items
   176. 8. Links / Attachments
   177.    178. 1. Feature / Status Snapshot
   179. Purpose: Identify the spec and its current state.
   180.    181. Include:
   182. - Feature name
   183. - Spec status
   184. - Last updated
   185. - Updated by
   186. - Monday item, if applicable
   187.    188. Do not include:
   189. - Approval status
   190. - Approval owner
   191. - Related Pre-Spec
   192. - Product area / licensee
   193.    194. 2. Source Basis
   195. Purpose: Show what sources the spec was built from so the developer can understand the review trail if needed.
   196.    197. Include:
   198. - Current Feature Working Model / Pre-Spec
   199. - Key Transcript Ingestion Reviews, if relevant
   200. - Relevant final transcripts, if needed for traceability
   201. - Mockup / UI references, if applicable
   202. - PMR references, if directly implicated
   203. - Agents Docs references, if used to shape WDE terminology or likely implementation surfaces
   204. - Related specs or cross-feature references
   205.    206. Rule: Keep this as a source list, not a source summary. Do not restate the Pre-Spec.
   207.    208. 3. Feature Summary
   209. Purpose: Give the reviewer the human-readable product intent before they evaluate Claude's technical plan or output.
   210.    211. Include:
   212. - what the feature does;
   213. - where it fits in Usked / WDE / the relevant workflow;
   214. - what user-facing problem or workflow gap it addresses;
   215. - what outcome the user should experience.
   216.    217. Rule: Keep this short. Feature area, licensee/package context, or product context can appear here naturally if relevant.
   218.    219. 4. Scope / Non-Scope
   220. Purpose: Give the reviewer a fast boundary check so Claude's plan/output does not expand the feature.
   221.    222. Include:
   223. - in scope;
   224. - out of scope;
   225. - phase boundaries, if applicable;
   226. - explicit non-goals.
   227.    228. Rule: Focus on boundaries that matter for review.
   229.    230. 5. Approved Product Decisions
   231. Purpose: Let the reviewer quickly compare Claude's plan/output against decisions that are already settled.
   232.    233. Include only decisions that materially affect implementation or review, such as:
   234. - product behavior decisions;
   235. - UX decisions;
   236. - permission / visibility decisions;
   237. - scope decisions;
   238. - data/model decisions that affect product behavior.
   239.    240. Do not include:
   241. - raw meeting history;
   242. - exploratory discussion;
   243. - stale decisions;
   244. - implementation details that belong only in Chapter 2.
   245.    246. 6. Feature-Specific Review Risks / Watchouts
   247. Purpose: Identify likely places where Claude, engineering, or a reviewer could misunderstand the feature, overbuild it, underbuild it, or implement the wrong WDE/Usked 2.0 pattern.
   248.    249. Include only when useful:
   250. - likely pitfalls specific to this feature;
   251. - edge cases that are easy to miss;
   252. - product decisions Claude might accidentally reverse or generalize;
   253. - WDE/Usked 2.0 surfaces that are especially important to preserve;
   254. - places where similar WDE terminology could be confused;
   255. - out-of-scope work Claude may be tempted to add;
   256. - known implementation assumptions that should be checked against Chapter 2;
   257. - feature-specific review questions for the developer.
   258.    259. Do not include:
   260. - a generic Claude review checklist;
   261. - internal dev workflow steps;
   262. - broad "make sure it works" checks;
   263. - generic code-quality checks;
   264. - generic QA checklist items.
   265.    266. 7. Known Blockers / Open Review Items
   267. Purpose: Prevent the reviewer from assuming everything is resolved.
   268.    269. Include only active items:
   270. - product blockers;
   271. - design / mockup blockers;
   272. - engineering confirmation blockers;
   273. - QA / test setup blockers;
   274. - approval or sequencing blockers, if relevant.
   275.    276. Rule: Resolved items should not remain here.
   277.    278. 8. Links / Attachments
   279. Purpose: Keep the cover sheet brief by pushing supporting material into links.
   280.    281. Include:
   282. - Pre-Spec
   283. - Mockups
   284. - Monday item
   285. - Transcript folder or specific transcripts
   286. - Related specs
   287. - Engineering feedback doc, only if relevant and approved as process evidence
   288.    289. Rule: Use links rather than duplicating source content.
   290.    291. Cover sheet writing rule:
   292. Keep the cover sheet brief. It may be human-readable, but it should not become a second product spec or duplicate the implementation spec.
   293.    294. 4.2 Chapter 2: Claude-Ingestible Implementation Spec
   295. Purpose:
   296. The Claude-Ingestible Implementation Spec is the core build artifact. It should be compact, precise, and specific enough for Claude to produce an implementation plan or implementation output without relying on broad product prose.
   297.    298. Chapter 2 should be drafted from the confirmed Implementation Concepts and draft implementation instructions already curated in the Pre-Spec. Carry forward the implementation intent, terminology, constraints, and open confirmations from the Pre-Spec, then finalize them into the required Feature Spec Sheet structure. Do not recreate the implementation model from scratch, and do not invent new Implementation Concepts during spec drafting without flagging the gap for Lyle review.
   299.    300. Use the implementation spec to provide implementation instructions, not meeting history or broad rationale.
   301.    302. Working content areas:
   303. 1. build target;
   304. 2. confirmed Implementation Concepts from the Pre-Spec;
   305. 3. in-scope and out-of-scope behavior;
   306. 4. WDE/Usked 2.0 surfaces;
   307. 5. behavior requirements;
   308. 6. configuration / data requirements;
   309. 7. permissions / visibility requirements;
   310. 8. implementation constraints / open confirmations;
   311. 9. acceptance / test requirements.
   312.    313. Implementation spec writing rule:
   314. Use precise WDE/Usked 2.0 terminology from current Agents Docs. Name likely surfaces directly when known. Avoid general language such as "add a page," "show a list," "create an action," or "store the data" when the correct WDE term is known, such as menu item, place, tab, context, context column, context action, row action, page/GAP action, module/table, record, field, Handlebars view, Lua script, TSA, backend route, or frontend JavaScript behavior.
   315.    316. 4.3 Compactness Rule
   317. The Claude-Ingestible Implementation Spec should be as short as possible while still being implementation-ready.
   318.    319. Do not include:
   320. 1. raw meeting history;
   321. 2. long rationale;
   322. 3. repeated Pre-Spec discussion;
   323. 4. stale open questions;
   324. 5. implementation choices that engineering should make;
   325. 6. unsupported assumptions;
   326. 7. generic product description that forces Claude to infer WDE implementation details.
   327.    328. 5. WDE / Usked 2.0 Terminology Precision
   329. 5.1 Principle
   330. Use WDE/Usked 2.0 terminology carefully and specifically. The goal is to reduce the chance that Claude implements from generic product language rather than the intended WDE/2.0 pattern.
   331.    332. 5.2 Preferred Terms
   333. Prefer precise terms such as:
   334. 1. module / table when referring to a WDE data structure;
   335. 2. record when referring to one row/object instance;
   336. 3. field when referring to a stored column on a module;
   337. 4. context when referring to a configured data query/display source;
   338. 5. context column when referring to a displayed/queryable column in a context;
   339. 6. context view / detail view when referring to WDE view rendering tied to a context or object;
   340. 7. context action when referring to an action available from a context toolbar;
   341. 8. row action when referring to an action available on a row;
   342. 9. page action / GAP action when referring to object-level actions exposed through the page-action menu;
   343. 10. menu item / place / tab / subtab / fifth element when referring to navigation placement;
   344. 11. wizard when referring to a multi-step WDE workflow;
   345. 12. Lua script when referring to Lua-based implementation logic;
   346. 13. TSA / trigger / sequence / action when referring to event-driven automation;
   347. 14. Handlebars view when referring to server-rendered UI;
   348. 15. frontend JavaScript behavior when referring to browser-side dynamic behavior;
   349. 16. backend route when referring to route/controller behavior;
   350. 17. package / builder configuration when referring to configurable records rather than custom code.
   351.    352. 5.3 Avoid Vague Terms
   353. Avoid vague use of object, table, action, view, wizard, screen, page, workflow, database, or automation when a more precise WDE/Usked 2.0 term is known.
   354.    355. If the precise term is not known, capture that as a Pre Spec Implementation Question rather than guessing.
   356.    357. 6. Chapter-Writing Standards
   358. 6.1 Chapter 1: Dev Review Cover Sheet Standards
   359. The cover sheet may use human-readable language, but it should remain brief and review-focused.
   360.    361. It should help the developer check Claude's plan and output against approved scope, source basis, intended product behavior, known non-goals, active blockers, testing expectations, and feature-specific review risks.
   362.    363. The cover sheet should not contain a generic Claude review checklist. Include review guidance only when it is specific to the feature and helps prevent a likely misunderstanding, overbuild, underbuild, wrong WDE/Usked 2.0 pattern, missed edge case, or known implementation assumption.
   364.    365. 6.2 Chapter 2: Claude-Ingestible Implementation Spec Standards
   366. The implementation spec should use short, direct statements.
   367.    368. Chapter 2 Feature Details should use the confirmed Implementation Concepts from the Pre-Spec as the organizing structure where applicable. Each concept section should carry forward the finalized implementation instructions needed to build that concept, using precise WDE/Usked 2.0 terminology and preserving explicit open confirmations.
   369.    370. Use structured lists, tables, and explicit labels where helpful.
   371.    372. Write for Claude and engineering, not for a broad business audience.
   373.    374. Each requirement should be traceable to a build behavior, WDE/Usked 2.0 surface, configuration requirement, permission requirement, or test requirement.
   375.    376. Avoid conversational or speculative phrasing.
   377.    378. 6.3 Acceptance Criteria and Testing
   379. Acceptance criteria should be written so a tester can determine pass/fail without reconstructing intent from the Pre-Spec or transcript.
   380.    381. Acceptance criteria should cover:
   382. 1. trigger or starting condition;
   383. 2. user or system action;
   384. 3. expected system behavior;
   385. 4. expected data/configuration result;
   386. 5. expected UI result, if applicable;
   387. 6. permission/visibility expectations;
   388. 7. relevant edge cases.
   389.    390. 7. Pre-Spec Readiness and Question Generation
   391. 7.1 Pre-Spec Readiness Checklist
   392. Before promoting a Feature Working Model / Pre-Spec into a Spec Sheet Draft, check whether the Pre-Spec has enough information to produce both chapters and whether the Implementation Concepts list is current enough to support Chapter 2.
   393.    394. The Pre-Spec is ready for spec drafting when:
   395. 1. source framing is current;
   396. 2. relevant transcripts have been ingested or explicitly marked as not required;
   397. 3. confirmed decisions are separated from likely decisions and open questions;
   398. 4. scope boundaries are stable enough for implementation drafting;
   399. 5. the product model is coherent;
   400. 6. user flows and launch contexts are sufficiently clear;
   401. 7. permissions and visibility are sufficiently clear;
   402. 8. data/backend/configuration implications are identified;
   403. 9. UI/mockup needs are resolved, not required, or explicitly open;
   404. 10. the running Implementation Concepts list is current;
   405. 11. candidate or newly proposed Implementation Concepts are confirmed, deferred, removed, or explicitly marked as blockers;
   406. 12. confirmed Implementation Concepts have draft implementation instructions sufficient to support Chapter 2;
   407. 13. Agents Docs-informed implementation implications are reviewed, with freshness checked through root AGENTS.md, AGENTS-CHANGELOG.md, and relevant focused doc Last updated lines when Agents Docs is used;
   408. 14. Pre Spec Implementation Questions have captured engineering-facing uncertainties;
   409. 15. remaining open questions are explicit and do not hide inside requirements;
   410. 16. Lyle has approved or requested movement into spec drafting.
   411.    412. 7.2 Lab Agenda Product Question Rules
   413. Lab Agenda questions should be generated by comparing the current Pre-Spec against what the two-chapter spec must eventually contain.
   414.    415. Add a question to the Lab Agenda when the missing information prevents the eventual spec from being implementable and requires product direction, workflow clarification, UX choice, policy decision, scope confirmation, or Feature Lab discussion.
   416.    417. Do not add engineering-facing implementation questions to the Lab Agenda unless answering them requires a product decision.
   418.    419. 7.3 Pre Spec Implementation Question Rules
   420. Pre Spec Implementation Questions should be generated from the current Pre-Spec's Implementation Concepts and draft implementation instructions, then checked against this document, the PMR, and current Agents Docs.
   421.    422. Add a question to Pre Spec Implementation Questions when missing information prevents the Claude-ingestible implementation spec from being implementation-ready but can be answered by engineering outside Feature Lab.
   423.    424. Implementation questions should identify:
   425. 1. related Implementation Concept;
   426. 2. draft implementation instruction gap;
   427. 3. likely reference area;
   428. 4. possible WDE/Usked 2.0 implementation surface;
   429. 5. source trigger;
   430. 6. how the answer may affect the Pre-Spec or concept-level draft implementation instructions;
   431. 7. whether the answer may affect the eventual Claude-Ingestible Implementation Spec.
   432.    433. 7.4 When to Promote to Spec Sheet Draft
   434. Promote to Spec Sheet Draft only when the Pre-Spec is stable enough to produce the Dev Review Cover Sheet and Claude-Ingestible Implementation Spec.
   435.    436. If major product, permission, workflow, lifecycle, messaging, data, UX, or implementation-readiness gaps remain unresolved, either keep the feature in Pre-Spec or carry the gaps as explicit open blockers.
   437.    438. 8. Final Spec Sheet Cleanup / Definition of Done
   439. Before treating a Spec Sheet Draft as final or implementation-ready, perform a cleanup pass.
   440.    441. Confirm that:
   442. 1. both chapters are present when applicable;
   443. 2. the cover sheet is brief and review-focused;
   444. 3. the implementation spec is compact and Claude-ingestible;
   445. 4. Chapter 2 carries forward confirmed Implementation Concepts and finalized implementation instructions from the Pre-Spec;
   446. 5. no new Implementation Concepts were invented during spec drafting without being flagged for Lyle review;
   447. 6. exploratory meeting history has been removed;
   448. 7. source basis is current;
   449. 8. requirements are clear and testable;
   450. 9. decisions are not mixed with open questions;
   451. 10. all open questions are explicit;
   452. 11. terms match PMR and current Agents Docs terminology where relevant;
   453. 12. WDE/Usked 2.0 surfaces are named precisely where known;
   454. 13. implementation notes clarify likely surfaces without exposing sensitive details;
   455. 14. edge cases and warnings are included where they affect build or testing;
   456. 15. testing instructions and pass/fail criteria are complete;
   457. 16. formatting, numbering, headings, and list structure are clean;
   458. 17. any remaining blockers are clearly identified for Lyle, engineering, QA, or design.
   459.    460. 9. Feedback and Revision Handling
   461. 9.1 Purpose
   462. This section prevents future feedback from bloating this document or being promoted into standing instruction too quickly.
   463.    464. 9.2 Engineering Feedback Rule
   465. Engineering implementation feedback can inform this document only after Lyle approves it as process evidence.
   466.    467. Do not automatically convert engineering-owned implementation notes, migration notes, handoff notes, or implementation conversation transcripts into Feature Spec Sheet Instructions.
   468.    469. 9.3 Full Implementation Conversation Rule
   470. Full engineering implementation conversations are supporting evidence only. Use them to understand why earlier feedback artifacts mattered, but do not treat them as standing instruction sources unless Lyle explicitly promotes them.
   471.    472. 9.4 Agents Docs Update Boundary
   473. Agents Docs updates are consumed through the Agents Docs folder, root AGENTS.md, AGENTS-CHANGELOG.md, and relevant focused docs.
   474.    475. Do not copy engineering-owned Agents Docs feedback into this document unless it directly changes Feature Spec Sheet drafting standards and Lyle approves the change.
   476.    477. 9.5 Current Active Process Sample
   478. The History Tabs engineering implementation feedback is the current active process sample for refining this document.
   479.    480. Use it in later passes to define detailed contents for the Dev Review Cover Sheet, detailed contents for the Claude-Ingestible Implementation Spec, implementation-ready expectations, WDE-heavy feature expectations, and the connection between spec structure and Pre Spec Implementation Questions.
   481.
