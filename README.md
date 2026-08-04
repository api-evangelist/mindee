# Mindee (mindee)

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

Mindee is a document parsing and intelligent document processing platform. Its REST API (api-v2.mindee.net) provides asynchronous inference across five model families — Extraction, Classification, Crop, OCR, and Split — plus a unified Jobs endpoint for polling. Mindee ships prebuilt models for invoices, receipts, passports, IDs, resumes, bank statements, and barcodes, along with customer-configurable extraction models with their own Data Schemas. Native SDKs cover Python, Node.js, Java, PHP, Ruby, and .NET, and front-end vision SDKs cover React and Vue. Mindee also stewards the open-source docTR OCR library.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/mindee/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/mindee/refs/heads/main/apis.yml)

## Scope

- **Position:** Consuming
- **Access:** 3rd-Party

## Tags

- Document Parsing
- OCR
- IDP
- AI
- Machine Learning
- Invoices
- Receipts
- IDs
- Computer Vision

## Timestamps

- **Created:** 2026-05-25
- **Modified:** 2026-05-25

## APIs

### Mindee Extraction API

Extract structured fields from invoices, receipts, IDs, passports, resumes, bank statements, and any other document type via Mindee's configurable extraction models. Enqueue a file at POST /v2/inferences/enqueue (or POST /v2/products/extraction/enqueue), reference your model_id, and retrieve the structured JSON result from GET /v2/inferences/{inference_id}. Supports RAG, raw text, polygons, and confidence scores depending on plan.

- **Human URL:** [https://docs.mindee.com/extraction-models/data-schema](https://docs.mindee.com/extraction-models/data-schema)

#### Tags

- Document Parsing
- OCR
- Extraction
- Invoices
- Receipts
- IDP

#### Properties

- [Documentation](https://docs.mindee.com/extraction-models/data-schema)
- [Documentation](https://docs.mindee.com/integrations/api-overview)
- [OpenAPI](openapi/mindee-extraction-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/mindee-extraction-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/mindee-extraction-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [JSON Schema](json-schema/mindee-inference-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Structure](json-structure/mindee-extraction-structure.json)
- [JSON-LD](json-ld/mindee-context.jsonld) — [JSON-LD](https://www.w3.org/TR/json-ld11/)
- [Example](examples/mindee-extraction-enqueue-example.json)
- [Example](examples/mindee-extraction-result-example.json)

### Mindee Classification API

Classify documents into predefined categories so they can be routed to the appropriate downstream extraction model. Enqueue at POST /v2/products/classification/enqueue and retrieve the label from GET /v2/products/classification/results/{inference_id}.

- **Human URL:** [https://docs.mindee.com/classification-models/classification-overview](https://docs.mindee.com/classification-models/classification-overview)

#### Tags

- Document Parsing
- Classification
- Routing
- IDP

#### Properties

- [Documentation](https://docs.mindee.com/classification-models/classification-overview)
- [OpenAPI](openapi/mindee-classification-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/mindee-classification-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/mindee-classification-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Mindee Crop API

Detect, isolate, and crop the document area inside a larger scanned image. Useful for cleaning up phone-captured documents prior to classification or extraction. Async enqueue/results pattern at /v2/products/crop/.

- **Human URL:** [https://docs.mindee.com/crop-models/crop-overview](https://docs.mindee.com/crop-models/crop-overview)

#### Tags

- Document Parsing
- Cropping
- Preprocessing
- IDP

#### Properties

- [Documentation](https://docs.mindee.com/crop-models/crop-overview)
- [OpenAPI](openapi/mindee-crop-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/mindee-crop-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/mindee-crop-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Mindee OCR API

Run full-page optical character recognition on a document and return the raw text plus bounding polygons. Enqueue at POST /v2/products/ocr/enqueue and retrieve the OCR payload from GET /v2/products/ocr/results/{inference_id}.

- **Human URL:** [https://docs.mindee.com/ocr-models/ocr-overview](https://docs.mindee.com/ocr-models/ocr-overview)

#### Tags

- OCR
- Document Parsing
- Text Extraction

#### Properties

- [Documentation](https://docs.mindee.com/ocr-models/ocr-overview)
- [OpenAPI](openapi/mindee-ocr-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/mindee-ocr-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/mindee-ocr-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Mindee Split API

Split a multi-document PDF or image batch into individual documents that can each be classified and extracted independently. Async enqueue/results pattern at /v2/products/split/.

- **Human URL:** [https://docs.mindee.com/split-models/split-overview](https://docs.mindee.com/split-models/split-overview)

#### Tags

- Document Parsing
- Splitting
- Preprocessing
- IDP

#### Properties

- [Documentation](https://docs.mindee.com/split-models/split-overview)
- [OpenAPI](openapi/mindee-split-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/mindee-split-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/mindee-split-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Mindee Jobs API

Poll the status of asynchronous Mindee inference jobs across every Mindee model family via GET /v2/jobs/{job_id}. Jobs return Waiting, Processing, Failed, or Success states and a polling_url plus optional result_url and webhook_url.

- **Human URL:** [https://docs.mindee.com/integrations/polling-for-results](https://docs.mindee.com/integrations/polling-for-results)

#### Tags

- Document Parsing
- Jobs
- Async
- Polling

#### Properties

- [Documentation](https://docs.mindee.com/integrations/polling-for-results)
- [Documentation](https://docs.mindee.com/integrations/webhooks)
- [OpenAPI](openapi/mindee-jobs-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/mindee-jobs-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/mindee-jobs-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [JSON Schema](json-schema/mindee-job-schema.json) — [JSON Schema](https://json-schema.org/specification)

## Common Properties

- [Arazzo Workflows](arazzo/) — [Arazzo Specification](https://spec.openapis.org/arazzo/latest.html)
- [Portal](https://mindee.com)
- [Documentation](https://docs.mindee.com)
- [Getting Started](https://docs.mindee.com/getting-started/quick-start)
- [Documentation](https://docs.mindee.com/integrations/api-overview)
- [Authentication](https://docs.mindee.com/integrations/api-keys)
- [Webhooks](https://docs.mindee.com/integrations/webhooks)
- [Documentation](https://docs.mindee.com/integrations/polling-for-results)
- [Errors](https://docs.mindee.com/integrations/problem-database)
- [Rate Limits](https://docs.mindee.com/integrations/technical-limitations)
- [Documentation](https://docs.mindee.com/integrations/response-times)
- [OpenAPI](https://api-v2.mindee.net/openapi.json) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Sign Up](https://app.mindee.com)
- [Authentication](https://app.mindee.com/api-keys)
- [Status Page](https://status.mindee.com)
- [Pricing](https://mindee.com/pricing)
- [Blog](https://mindee.com/blog)
- [About Us](https://mindee.com/about)
- [Careers](https://mindee.com/careers)
- [Contact](https://mindee.com/contact)
- [LinkedIn](https://www.linkedin.com/company/mindee)
- [Twitter](https://twitter.com/mindee_official)
- [GitHub Organization](https://github.com/mindee)
- [SDK](https://github.com/mindee/mindee-api-python)
- [SDK](https://github.com/mindee/mindee-api-nodejs)
- [SDK](https://github.com/mindee/mindee-api-java)
- [SDK](https://github.com/mindee/mindee-api-php)
- [SDK](https://github.com/mindee/mindee-api-ruby)
- [SDK](https://github.com/mindee/mindee-api-dotnet)
- [SDK](https://github.com/mindee/react-mindee-js)
- [SDK](https://github.com/mindee/vue-mindee-js)
- [Open Source](https://github.com/mindee/doctr)
- [Integration](https://github.com/mindee/integration-zapier)
- [Integration](https://github.com/mindee/integration-microsoft-flow)
- [Documentation](https://github.com/mindee/platform-docs)
- [Plans](plans/mindee-plans-pricing.yml)
- [Rate Limits](rate-limits/mindee-rate-limits.yml)
- [Fin Ops](finops/mindee-finops.yml)
- [Vocabulary](vocabulary/mindee-vocabulary.yml)
- [Spectral Rules](rules/mindee-rules.yml)
- [Features](undefined)

## Maintainers

**FN:** Kin Lane
**Email:** info@apievangelist.com
**URL:** https://apievangelist.com
