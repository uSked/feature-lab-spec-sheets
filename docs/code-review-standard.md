# Code review during Feature Lab ingestion

Inspect the current default branch of [`uSked/wde-service`](https://github.com/uSked/wde-service) when transcript ingestion introduces or changes an Implementation Concept, technical assumption, or likely engineering question. The default branch is currently `master`; if it is renamed, use `main`. Do not base an ingestion review on a feature branch, PR diff, or an uncommitted local tree.

Before making technical claims, fetch the branch tip and record the repository, branch, and full commit SHA. Start with the repo's `AGENTS.md` pointer, `CLAUDE.md`, and relevant `documents/` files to find implementation surfaces. Search and inspect the code that implements the behavior. Treat `documents/plans/` as proposals. If documentation and code disagree, describe the discrepancy and rely on the code for what the inspected commit implements.

For each affected Implementation Concept, report:

- What the current code demonstrates, with file and function references.
- The likely implementation surface and any dependency or constraint relevant to the concept.
- What remains an inference, including behavior dependent on runtime configuration, migrated data, permissions, deployment state, or another repository.
- Likely IC engineering questions, with answer options grounded in code where possible.
- Product choices that should be resolved in the next Feature Lab, separately from engineering facts to confirm.

Code review is read-only. It cannot create or confirm a product decision, change an Implementation Concept status, or automatically update the PMR or Pre-Spec. Do not copy credentials, personal paths, connection details, or customer data into Feature Lab artifacts.
