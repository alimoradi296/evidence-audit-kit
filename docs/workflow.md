# Workflow

This workflow is designed for an AI coding agent working with a developer. The agent can inspect authorized sources, gather proportionate evidence, maintain the audit record, and perform authorized implementation and checks. The developer and agent should make access boundaries and authorization clear before action. A written audit record is the shared account of the work; it does not replace the source, runtime evidence, or human decisions.

## Evidence model

Each finding has a stable ID, claim, affected revision, impact, evidence references, confidence, and disposition.
Each reference records its origin, capture time, environment, and retention location.
Label unavailable raw evidence as unarchived and independently unreproducible.
A hash supports integrity checking; it does not prove a claim is true.

Use confidence labels: hypothesis, source-confirmed, locally-reproduced, runtime-observed, or operator-reported.
These describe different evidence types, not a universal ranking. Record limits alongside each label.

## Lifecycle

1. The agent inspects the authorized source and records the assessed revision.
2. The agent records findings and competing explanations without implementing fixes during diagnosis.
3. The agent gathers proportionate evidence and states what remains unknown.
4. The agent recommends a disposition: investigate, fix, defer, accept risk, reject, or supersede. Record who made the decision.
5. For selected work, the agent writes a scoped fix with exclusions and observable acceptance criteria.
6. The agent implements only authorized work and records verification results.
7. Record deployment and full acceptance separately, with the responsible source or person's confirmation.

Do not assume the agent has permission to access a system, change code, deploy, or accept risk. Follow the user's existing authorization and the project's access rules. Diagnosis alone does not authorize a fix.

Use severity for impact and urgency. Use change risk for blast radius and reversibility.
Estimate effort separately. A small fix does not automatically have high priority.
Avoid numerical maturity scores unless a documented rubric supports them.

## Status authority

The finding record is the current status authority. Indexes should link to it rather than repeat mutable status.
Record these dimensions independently:

| Dimension | Values |
|---|---|
| Implementation | not-started, in-progress, implemented, reverted |
| Verification | unchecked, passed, failed, blocked |
| Deployment | not-required, not-deployed, deployed, unknown |
| Acceptance | unchecked, passed, failed, blocked, not-applicable |

For not-applicable, record a reason. Name the checked revision and environment.
After a correction, reread the complete in-scope acceptance source.
A finding may close as fixed only when required verification and acceptance pass.
Record other closure reasons explicitly, including accepted risk and rejected hypothesis.

## Revisions

Keep historical observations intact. Append dated changes with new evidence and changed judgments.
A new judgment does not establish that the assessed implementation changed.

## Privacy

Collect only necessary evidence. Prefer synthetic reproductions and redacted summaries.
Keep raw evidence private. Never request production dumps by default.
Before publishing, inspect every included file, metadata, archive, link, and Git history.
Secret scans cannot establish that business information is safe to disclose.
