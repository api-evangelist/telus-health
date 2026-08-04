# TELUS Health (telus-health)

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

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
