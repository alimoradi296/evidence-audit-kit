---
name: audit-prove
description: Investigate an existing audit claim with evidence. Use when causality or runtime behavior remains uncertain.
---

# Audit prove

Read `docs/workflow.md` from the kit root. When used in another project, use its explicit configuration and acceptance sources.

Read the finding and its evidence. Select a discriminating check for competing explanations. Prefer a synthetic reproduction when practical. Respect access boundaries and avoid production writes. Record environment, revision, capture time, observed results, rejected hypotheses, and limits. Append the judgment change to the audit history. In latency investigations, distinguish component timing from user-visible elapsed time.
