# TELUS Health (telus-health)

TELUS Health is the digital-health division of TELUS, one of Canada's largest telecommunications and technology companies, and the country's leading health-IT provider. It operates the PS Suite, Med Access, and cloud-native Collaborative Health Record (CHR) electronic medical records used across Canadian primary care, along with pharmacy management, virtual care, and employer/benefits health services. Its documented public integration surface is the CHR Enterprise API (GraphQL) plus the TELUS Patient Chart FHIR R4 implementation guide for standards-based patient-record exchange. Home market is Canada.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/telus-health/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/telus-health/refs/heads/main/apis.yml)

## Tags

- Healthcare
- Canada
- EMR
- EHR
- FHIR
- HL7
- Interoperability
- GraphQL
- e-Prescribing
- Pharmacy
- Digital Health
- Clinical Data

## Timestamps

- **Created:** 2026-07-24
- **Modified:** 2026-07-24

## APIs

### TELUS CHR Enterprise API

GraphQL API for the TELUS Collaborative Health Record (CHR) that lets partners build integrations against clinic data. Queries retrieve and mutations create or update CHR records (patients, appointments, encounters, clinical documents and more), following the GraphQL Cursor Connections spec. Authenticated with RS512-signed JSON Web Tokens presented as Bearer tokens (15-minute expiry). The GraphQL endpoint URL is provisioned per CHR domain, so no single fixed base host is published.

- **Human URL:** [https://help.inputhealth.com/en/articles/6483215-chr-enterprise-api](https://help.inputhealth.com/en/articles/6483215-chr-enterprise-api)

#### Tags

- GraphQL
- EMR
- Healthcare
- Interoperability

#### Properties

- [Documentation](https://help.inputhealth.com/en/articles/6483215-chr-enterprise-api)
- [API Reference](http://apidocs.inputhealth.com/voyager.html)
- [GraphQL Voyager Schema Explorer](http://apidocs.inputhealth.com/voyager.html)
- [Getting Started](https://help.inputhealth.com/en/articles/6368814-enterprise-api-onboarding-overview)
- [Authentication](https://help.inputhealth.com/en/articles/6483223-making-requests-to-the-api)

### TELUS Patient Chart FHIR API

TELUS Patient Chart FHIR R4 implementation guide, published by TELUS, containing 89 StructureDefinition profiles and extensions under the `http://telus.com/fhir/patientChart` canonical. Profiles cover patient-chart resources including AllergyIntolerance, CarePlan, ClinicalImpression, Composition, Condition, DiagnosticReport, DocumentReference, Encounter, MedicationRequest, and a large set of medication/prescribing extensions, used to exchange patient-record data exported from TELUS EMRs. No TELUS CapabilityStatement or SMART-on-FHIR configuration is published.

- **Human URL:** [https://simplifier.net/teluspatientchart](https://simplifier.net/teluspatientchart)
- **Base URL:** `https://fhir.simplifier.net/TELUSPatientChart`

#### Tags

- FHIR
- HL7
- Interoperability
- Healthcare

#### Properties

- [Documentation](https://simplifier.net/teluspatientchart)
- [FHIR StructureDefinitions (89 profiles)](fhir/telus-patient-chart-structuredefinitions.json)

## Common Properties

- [Website](https://www.telus.com/en/health)
- [Developer Portal](https://help.inputhealth.com/en/articles/6483215-chr-enterprise-api)
- [Documentation](https://help.inputhealth.com/en/articles/6483215-chr-enterprise-api)
- [API Reference](http://apidocs.inputhealth.com/voyager.html)
- [Getting Started](https://help.inputhealth.com/en/articles/6368814-enterprise-api-onboarding-overview)
- [LinkedIn](https://www.linkedin.com/company/telus-health)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
