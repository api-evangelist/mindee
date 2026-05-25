# Mindee (mindee)
Mindee is a document parsing and intelligent document processing platform. Its REST API (`api-v2.mindee.net`) provides asynchronous inference across five model families — Extraction, Classification, Crop, OCR, and Split — plus a unified Jobs endpoint for polling. Mindee ships prebuilt models for invoices, receipts, passports, IDs, resumes, bank statements, and barcodes, along with customer-configurable extraction models with their own Data Schemas. Native SDKs cover Python, Node.js, Java, PHP, Ruby, and .NET, and front-end vision SDKs cover React and Vue. Mindee also stewards the open-source docTR OCR library.

**URL:** [Visit APIs.json](https://raw.githubusercontent.com/api-evangelist/mindee/refs/heads/main/apis.yml)

**Run:** [Capabilities Using Naftiko](https://github.com/naftiko/fleet?utm_source=api-evangelist&utm_medium=readme&utm_campaign=company-api-evangelist&utm_content=repo)

## Tags

- Document Parsing, OCR, IDP, AI, Machine Learning, Invoices, Receipts, IDs, Computer Vision

## Timestamps

- **Created:** 2026-05-25
- **Modified:** 2026-05-25

## Pattern

Mindee follows a consistent asynchronous enqueue/poll pattern across every model family:

1. `POST /v2/products/{family}/enqueue` (or `POST /v2/inferences/enqueue` for extraction) — submit a file with a `model_id`. Returns `202 Accepted` and a `polling_url`.
2. `GET /v2/jobs/{job_id}` — poll for status: `Waiting`, `Processing`, `Failed`, or `Success`.
3. `GET /v2/products/{family}/results/{inference_id}` — fetch the structured inference result once the job succeeds.

A webhook URL can be supplied at enqueue time to receive completion events instead of polling.

Authentication is an API key passed in the `Authorization` header. Create keys at [app.mindee.com/api-keys](https://app.mindee.com/api-keys).

## APIs

### Mindee Extraction API
Extract structured fields from invoices, receipts, IDs, passports, resumes, bank statements, and any other document type via Mindee's configurable extraction models. Output shape is driven by the model's Data Schema.

**Human URL:** [https://docs.mindee.com/extraction-models/data-schema](https://docs.mindee.com/extraction-models/data-schema)

- [OpenAPI](openapi/mindee-extraction-api-openapi.yml)
- [JSON Schema — Inference](json-schema/mindee-inference-schema.json)
- [JSON Structure — Extraction](json-structure/mindee-extraction-structure.json)
- [JSON-LD](json-ld/mindee-context.jsonld)
- [Example — Enqueue](examples/mindee-extraction-enqueue-example.json)
- [Example — Result](examples/mindee-extraction-result-example.json)
- [Naftiko Capability — Extraction](capabilities/extraction-extraction.yaml)

### Mindee Classification API
Classify documents into predefined categories so they can be routed to the appropriate downstream extraction model.

- [OpenAPI](openapi/mindee-classification-api-openapi.yml)
- [Naftiko Capability — Classification](capabilities/classification-classification.yaml)

### Mindee Crop API
Detect, isolate, and crop the document area inside a larger scanned image. Useful for cleaning up phone-captured documents prior to classification or extraction.

- [OpenAPI](openapi/mindee-crop-api-openapi.yml)
- [Naftiko Capability — Crop](capabilities/crop-crop.yaml)

### Mindee OCR API
Run full-page optical character recognition on a document and return the raw text plus bounding polygons.

- [OpenAPI](openapi/mindee-ocr-api-openapi.yml)
- [Naftiko Capability — OCR](capabilities/ocr-ocr.yaml)

### Mindee Split API
Split a multi-document PDF or image batch into individual documents that can each be classified and extracted independently.

- [OpenAPI](openapi/mindee-split-api-openapi.yml)
- [Naftiko Capability — Split](capabilities/split-split.yaml)

### Mindee Jobs API
Poll the status of asynchronous Mindee inference jobs across every model family.

- [OpenAPI](openapi/mindee-jobs-api-openapi.yml)
- [JSON Schema — Job](json-schema/mindee-job-schema.json)
- [Naftiko Capability — Jobs](capabilities/jobs-jobs.yaml)

## Plans

| Plan | Monthly | Credits | Overage | Highlights |
|---|---|---|---|---|
| Starter | EUR 44 | 500 | EUR 0.05 | Unlimited models; community support |
| Pro | EUR 179 | 2,500 | EUR 0.04 | Live chat; team members; data localization; RAG (20 docs); polygons |
| Business | EUR 584 | 10,000 | EUR 0.035 | Unlimited RAG; confidence scores; boosted accuracy |
| Enterprise | Contact | Custom | Custom | Dedicated AM; custom SLAs; custom models |

Annual billing offers a 10 percent discount. Full reconciled definition: [plans/mindee-plans-pricing.yml](plans/mindee-plans-pricing.yml).

## Operational Artifacts

- [Plans — API Commons Plans 0.1](plans/mindee-plans-pricing.yml)
- [Rate Limits — API Commons Rate Limits 0.1](rate-limits/mindee-rate-limits.yml)
- [FinOps — FOCUS 1.3 / FinOps Framework](finops/mindee-finops.yml)
- [Vocabulary](vocabulary/mindee-vocabulary.yml)
- [Spectral Rules](rules/mindee-rules.yml)

## SDKs and Tooling

- [Python SDK](https://github.com/mindee/mindee-api-python)
- [Node.js SDK](https://github.com/mindee/mindee-api-nodejs)
- [Java SDK](https://github.com/mindee/mindee-api-java)
- [PHP SDK](https://github.com/mindee/mindee-api-php)
- [Ruby SDK](https://github.com/mindee/mindee-api-ruby)
- [.NET SDK](https://github.com/mindee/mindee-api-dotnet)
- [React Computer Vision SDK](https://github.com/mindee/react-mindee-js)
- [Vue Computer Vision SDK](https://github.com/mindee/vue-mindee-js)
- [docTR — Open-source OCR](https://github.com/mindee/doctr)
- [Zapier Integration](https://github.com/mindee/integration-zapier)

## Sources

- [mindee.com](https://mindee.com)
- [docs.mindee.com](https://docs.mindee.com)
- [Mindee V2 OpenAPI](https://api-v2.mindee.net/openapi.json)
- [Pricing](https://mindee.com/pricing)
- [GitHub — mindee](https://github.com/mindee)
