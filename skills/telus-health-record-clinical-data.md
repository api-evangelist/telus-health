---
name: Record medications and allergies on a patient chart
description: Add medication records and drug/non-drug allergy records to a patient chart, and upsert structured patient data via the CHR Enterprise GraphQL API.
api: graphql/telus-health-chr-enterprise.graphql
operations: [addMedicationRecord, addDrugAllergyRecord, addNonDrugAllergyRecord, upsertPatientDataItem, patient]
generated: '2026-07-24'
method: generated
---

# Record medications and allergies on a patient chart

Operating instructions for an agent using the **TELUS CHR Enterprise API** (GraphQL). Every operation is a real root field in `graphql/telus-health-chr-enterprise.graphql`.

## Prerequisites
- Per-domain GraphQL endpoint and an RS512 JWT bearer token (see `authentication/telus-health-authentication.yml`).
- A known patient `id` (from `patient` / `patients` or `createPatient`).

## Steps
1. **Add a medication** — mutation `addMedicationRecord` referencing the patient `id`.
2. **Add a drug allergy** — mutation `addDrugAllergyRecord`; for non-drug allergies use `addNonDrugAllergyRecord`.
3. **Upsert structured data** — mutation `upsertPatientDataItem` for template-driven patient data fields.
4. **Verify** — query `patient(id: ...)` and read back `medicationRecords`, `allergyRecords`, and `patientDataItems`.

## Conventions & error handling
- Chart collections (`medicationRecords`, `allergyRecords`, `patientDataItems`) are exposed as connections/lists on the `Patient` entity (see `data-model/telus-health-data-model.yml`).
- `upsert*` mutations are the safe path for repeatable writes; the plain `add*` mutations are **not idempotent**, so verify before retrying.
- Handle the standard GraphQL `errors[]` envelope.
