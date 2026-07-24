---
name: Register a patient and book an appointment
description: Create a patient record in a TELUS CHR domain and schedule an appointment for them via the CHR Enterprise GraphQL API.
api: graphql/telus-health-chr-enterprise.graphql
operations: [createPatient, patient, createAppointment, appointment]
generated: '2026-07-24'
method: generated
---

# Register a patient and book an appointment

Operating instructions for an agent using the **TELUS CHR Enterprise API** (GraphQL). Every operation below is a real root field in the published schema (`graphql/telus-health-chr-enterprise.graphql`).

## Prerequisites
- The per-domain GraphQL endpoint (CHR **Settings > Enterprise API > API Endpoint**).
- An **RS512-signed JWT** presented as `Authorization: Bearer {jwt}`, `iss` matching the API Consumer, `exp` within 15 minutes. See `authentication/telus-health-authentication.yml`.
- All calls are `POST` with the GraphQL document as the JSON body.

## Steps
1. **Create the patient** — mutation `createPatient` with the patient demographics input. Capture the returned patient `id`.
2. **Confirm the record** — query `patient(id: ...)` to verify the created record and read back identifiers.
3. **Book the appointment** — mutation `createAppointment`, referencing the patient `id`, the provider/location, and the start time.
4. **Verify** — query `appointment(id: ...)` to confirm scheduling.

## Conventions & error handling
- List reads (e.g. `patients`, `appointments`) use GraphQL **Cursor Connections** (`first`/`after`, default 50, max 100) — see `conventions/telus-health-conventions.yml`.
- Errors return the standard GraphQL top-level `errors[]` array alongside partial `data`; there is **no idempotency key**, so guard against duplicate `createPatient`/`createAppointment` calls on retry.
- `respondent` fields/mutations are **deprecated** — always use `patient` / `createPatient` (see `lifecycle/telus-health-lifecycle.yml`).
