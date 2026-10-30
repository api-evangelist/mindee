# Mindee

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
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
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

**Areas:** Document Parsing · OCR · Intelligent Document Processing · Artificial Intelligence · Machine Learning · Invoices · Receipts · IDS · Computer Vision

## Mindee on APIs.io

Everything profiled for Mindee is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/mindee/](https://apis.io/providers/mindee/)** — or go straight to one of the APIs or properties below.

### APIs (6)

- [Mindee Extraction API](https://apis.io/apis/mindee/mindee-extraction-api/) — Extract structured fields from invoices, receipts, IDs, passports, resumes, bank statements, and any other document type via Mindee's configurable…
- [Mindee Classification API](https://apis.io/apis/mindee/mindee-classification-api/) — Classify documents into predefined categories so they can be routed to the appropriate downstream extraction model. Enqueue at POST…
- [Mindee Crop API](https://apis.io/apis/mindee/mindee-crop-api/) — Detect, isolate, and crop the document area inside a larger scanned image. Useful for cleaning up phone-captured documents prior to classification or…
- [Mindee OCR API](https://apis.io/apis/mindee/mindee-ocr-api/) — Run full-page optical character recognition on a document and return the raw text plus bounding polygons. Enqueue at POST /v2/products/ocr/enqueue and…
- [Mindee Split API](https://apis.io/apis/mindee/mindee-split-api/) — Split a multi-document PDF or image batch into individual documents that can each be classified and extracted independently. Async enqueue/results pattern…
- [Mindee Jobs API](https://apis.io/apis/mindee/mindee-jobs-api/) — Poll the status of asynchronous Mindee inference jobs across every Mindee model family via GET /v2/jobs/{job_id}. Jobs return Waiting, Processing, Failed,…

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### Arazzo workflows (14)

Multi-step workflows that chain operations into a business task.

- [Mindee Bank Statement Extraction](https://apis.io/arazzos/mindee/mindee-bank-statement-extraction-workflow/)
- [Mindee Classify Document Type](https://apis.io/arazzos/mindee/mindee-classify-document-type-workflow/)
- [Mindee Classify Then Extract](https://apis.io/arazzos/mindee/mindee-classify-then-extract-workflow/)
- [Mindee Crop Document](https://apis.io/arazzos/mindee/mindee-crop-document-workflow/)
- [Mindee Custom Document Extraction](https://apis.io/arazzos/mindee/mindee-custom-document-extraction-workflow/)
- [Mindee Extract From URL](https://apis.io/arazzos/mindee/mindee-extract-from-url-workflow/)
- [Mindee Invoice Extraction](https://apis.io/arazzos/mindee/mindee-invoice-extraction-workflow/)
- [Mindee OCR Full Text](https://apis.io/arazzos/mindee/mindee-ocr-full-text-workflow/)
- [Mindee OCR Then Extract](https://apis.io/arazzos/mindee/mindee-ocr-then-extract-workflow/)
- [Mindee Passport and ID Extraction](https://apis.io/arazzos/mindee/mindee-passport-id-extraction-workflow/)
- [Mindee Poll Job With Failure Branch](https://apis.io/arazzos/mindee/mindee-poll-job-with-failure-branch-workflow/)
- [Mindee Receipt Extraction](https://apis.io/arazzos/mindee/mindee-receipt-extraction-workflow/)
- [Mindee Split Multi-Document File](https://apis.io/arazzos/mindee/mindee-split-multi-document-workflow/)
- [Mindee Split Then Extract](https://apis.io/arazzos/mindee/mindee-split-then-extract-workflow/)

#### Agentic access (1)

Which operations an agent can call, which act, and which need a human in the loop.

- [Mindee Agentic Access](https://apis.io/agentic-access/mindee/mindee-agentic-access/)

#### JSON Schema (2)

The data models the API reads and writes.

- [Mindee Inference](https://apis.io/schemas/mindee/mindee-inference/)
- [Mindee Job](https://apis.io/schemas/mindee/mindee-job/)

#### JSON Structure (1)

Data models expressed in JSON Structure.

- [Mindee Extraction Structure](https://apis.io/json-structure/mindee/mindee-extraction-structure/)

#### JSON-LD (1)

Linked-data contexts for the provider's vocabulary.

- [Mindee Context](https://apis.io/jsonld/mindee/mindee-context/)

#### Vocabulary (1)

The provider's domain terms, defined.

- [Mindee Vocabulary](https://apis.io/vocabularies/mindee/mindee-vocabulary/)

#### Examples (2)

Example requests and responses.

- [Mindee Extraction Enqueue Example](https://apis.io/examples/mindee/mindee-extraction-enqueue-example/)
- [Mindee Extraction Result Example](https://apis.io/examples/mindee/mindee-extraction-result-example/)

#### Collections (12)

Postman and Open Collection request collections.

- [Mindee Classification API](https://apis.io/collections/mindee/open-mindee-classification-api/)
- [Mindee Classification Crop API](https://apis.io/collections/mindee/open-mindee-crop-api/)
- [Mindee Classification Extraction API](https://apis.io/collections/mindee/open-mindee-extraction-api/)
- [Mindee Classification Jobs API](https://apis.io/collections/mindee/open-mindee-jobs-api/)
- [Mindee Classification Ocr API](https://apis.io/collections/mindee/open-mindee-ocr-api/)
- [Mindee Classification Split API](https://apis.io/collections/mindee/open-mindee-split-api/)
- [Mindee Classification API](https://apis.io/collections/mindee/postman-mindee-classification-api/)
- [Mindee Crop API](https://apis.io/collections/mindee/postman-mindee-crop-api/)
- [Mindee Extraction API](https://apis.io/collections/mindee/postman-mindee-extraction-api/)
- [Mindee Jobs API](https://apis.io/collections/mindee/postman-mindee-jobs-api/)
- [Mindee OCR API](https://apis.io/collections/mindee/postman-mindee-ocr-api/)
- [Mindee Split API](https://apis.io/collections/mindee/postman-mindee-split-api/)

#### Governance rules (2)

Spectral rulesets for the provider's contracts.

- [Mindee — jsonschema rules](https://apis.io/rules/mindee/mindee-jsonschema-spectral-rules/)
- [Mindee API Rules](https://apis.io/rules/mindee/mindee-rules/)

#### Security (2)

Authentication, trust centre, and vulnerability disclosure.

- [Mindee Authentication](https://apis.io/security/mindee/mindee-authentication/)
- [Mindee Domain Security](https://apis.io/security/mindee/mindee-domain-security/)

#### Plans and pricing (1)

Published plans, tiers and prices.

- [Mindee Plans Pricing](https://apis.io/plans/mindee/mindee-plans-pricing/)

#### Rate limits (1)

Published request limits.

- [Mindee Rate Limits](https://apis.io/rate-limits/mindee/mindee-rate-limits/)

#### FinOps (1)

What the API costs to run, by operation.

- [Mindee Finops](https://apis.io/finops/mindee/mindee-finops/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://www.mindee.com/)
- [Documentation](https://docs.mindee.com)
- [Getting started](https://docs.mindee.com/getting-started/quick-start)
- [Pricing](https://mindee.com/pricing)
- [Blog](https://mindee.com/blog)
- [GitHub](https://github.com/mindee)
- [Status](https://status.mindee.com)

## API Evangelist rating

**Kin Score 50.0** — developing · rubric 0.25.0 · scored 2026-10-23

| Facet | Score |
|---|---|
| Discoverability | 62.5 |
| Contract quality | 67.2 |
| Contract governance | 27.3 |
| Operational transparency | 28.9 |
| Developer ergonomics | 63.1 |
| Access clarity | 39.5 |

**Agent readiness 31.3** — agent-ready

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | yes |
| Agentic Access | derived (partial credit) |
| Reversibility Documented | — |
| MCP Server | — |
| Auth Clarity | bearer (partial credit) |
| Idempotency | — |
| Error Semantics | verified |
| OpenAPI Examples | partial |
| Rate Limit Signal | documented (partial credit) |
| Event Surface Described | unknown |
| Agent Skills | — |
| Well Known Catalog | — |
| Consent Identity | — |
| Agent Card | — |
| Dry Run Mode | — |
| Delegated Identity | — |
| Protected Resource Metadata | — |
| Dynamic Client Registration | — |
| Agentic Commerce | — |
| Pagination Ratio | na |
| Operation Distinctiveness | — |

**Regulatory alignment 15.5** — Horizontal (data, software, accessibility, platform)

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/mindee/](https://apis.io/providers/mindee/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for Mindee: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/mindee/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
