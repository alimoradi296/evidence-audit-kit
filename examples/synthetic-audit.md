# Synthetic example: duplicate reads

All names and measurements below are invented. No commands were executed.

- Audit: EXAMPLE-001
- Revision: fictional-revision-a
- Scope: fictional task list screen

## Finding EXAMPLE-F1

Claim: opening the task list triggers two identical reads.
Impact: unnecessary request load; severity medium in this fictional scenario.
Confidence: locally-reproduced in the fictional narrative only.
Evidence: invented trace shows two reads per navigation; no real trace exists.
Competing explanation: automatic retry. Rejected in the narrative because both responses succeed and neither request follows a failure.
Disposition: fix.
Implementation: implemented in fictional-revision-b.
Verification: passed in the fictional local scenario; one read per navigation.
Deployment: not-deployed.
Acceptance: unchecked; navigation recovery and slow-network behavior remain unchecked.
Closure: open. Local success does not satisfy the complete acceptance scope.

## Scoped fix

Remove the duplicate loader subscription. Preserve refresh and retry behavior.
Exclude cache changes and API redesign. Revert the subscription change if navigation fails.

## Revision history

Synthetic revision 1: duplicate reads proposed as a hypothesis.
Synthetic revision 2: fictional trace supports duplicate subscriptions; retry explanation rejected.
Synthetic revision 3: fictional local fix passes one-read check; full acceptance remains open.
