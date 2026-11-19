---
name: fix-done
description: Review verification, deployment, and acceptance of a scoped fix. Use before claiming closure or after a correction.
---

# Fix done

Read `docs/workflow.md` from the kit root. When used in another project, use its explicit configuration and acceptance sources.

Read the complete fix and parent acceptance source. Compare every authorized change and exclusion with the current implementation. Run proportionate authorized checks. After any correction, revisit all in-scope acceptance criteria. Record revision, environment, results, and gaps. Report implementation, verification, deployment, and acceptance separately. Keep closure open when required checks fail or remain unchecked. Never infer acceptance from CI or merge status.
