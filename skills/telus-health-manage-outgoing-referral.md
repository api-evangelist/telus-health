---
name: Create and track an outgoing referral
description: Create an outgoing referral for a patient, assign it to a waiting list, and add a comment via the CHR Enterprise GraphQL API.
api: graphql/telus-health-chr-enterprise.graphql
operations: [createOutgoingReferralRecord, referralRecord, assignReferralRecordToWaitingList, addReferralRecordComment]
generated: '2026-07-24'
method: generated
---

# Create and track an outgoing referral

Operating instructions for an agent using the **TELUS CHR Enterprise API** (GraphQL). Every operation is a real root field in `graphql/telus-health-chr-enterprise.graphql`.

## Prerequisites
- Per-domain GraphQL endpoint and an RS512 JWT bearer token (see `authentication/telus-health-authentication.yml`).

## Steps
1. **Create the referral** — mutation `createOutgoingReferralRecord` with the patient, target facility/practitioner, priority, and reason. Capture the referral `id`.
2. **Assign to a waiting list** — mutation `assignReferralRecordToWaitingList` with the referral `id` and target waiting list.
3. **Annotate** — mutation `addReferralRecordComment` to record follow-up notes.
4. **Track status** — query `referralRecord(id: ...)` (or the `referralRecords` connection) to read current status and comments.

## Conventions & error handling
- `referralRecords`, `referralWaitingLists`, and `referralStatuses` are Cursor Connections (default 50 / max 100).
- No idempotency key: re-running `createOutgoingReferralRecord` creates a duplicate — verify via `referralRecords` before retrying.
- Handle the GraphQL `errors[]` envelope; there is no RFC 9457 problem+json.
