# Enterprise Prompt Engineering Studio

A hands-on collection for designing, refining, and reviewing reusable prompts for business tasks. Explore customer support, HR, finance, product recommendations, contract summarization, and technical documentation using small, simulated enterprise datasets.

The collection brings together **11 prompt files**, **8 datasets**, a reusable template, evaluation materials, and a detailed lab guide. It is a documentation-based learning lab: prompts are used manually in an AI tool of your choice.

> **Project status:** Learning materials and supplied example records. Existing scores and approval statements are historical lab entries, not independently verified benchmarks or production approval. See [review notes](docs/review-notes.md) for evidence limits and inconsistencies.

## Start here

1. Download or clone this repository and open it in VS Code or another text editor.
2. Read the [original lab guide](instructions/Lab%201%20Enterprise%20Prompt%20Engineering%20Studio.docx).
3. Try the [customer-support walkthrough](docs/customer-support-walkthrough.md), which includes the complete ticket and FAQ context.
4. Compare prompt versions using the same inputs, model, and settings.
5. Save each response and assess it with the [quality rubric](Lab/evaluation/prompt_quality_rubric.md). Record your own findings separately from the supplied examples.

You need a Markdown/text viewer, a DOCX-compatible viewer for the guide, and access to an AI chat tool for manual practice. There is no Python application, dependency installation, API integration, or automated evaluation runner in this repository. The original guide lists Python 3.11 as a prerequisite, but the supplied files do not require Python for manual use.

## What you can practice

- Define roles, objectives, constraints, and output formats.
- Supply source documents so responses can be checked against evidence.
- Compare prompts without examples with prompts containing examples.
- Track prompt revisions and review response quality consistently.
- Explore prompt ownership, review, versioning, and deployment planning.

## Business prompt catalog

| Domain | Prompt | Supporting input | Practice task |
| --- | --- | --- | --- |
| Customer support | [Starter](Lab/prompts/customer_support.md) and v1–v5 below | [Customer queries](Lab/datasets/customer_queries.csv), [support FAQ](Lab/datasets/support_faq.txt) | Summarize a ticket and suggest a supported next action |
| HR | [hr.md](Lab/prompts/hr.md) | [HR policy](Lab/datasets/hr_policy.txt), optional [handbook](Lab/datasets/employee_handbook.txt) | Answer questions from the supplied policy |
| Finance | [finance.md](Lab/prompts/finance.md) | [Invoice records](Lab/datasets/invoice_records.csv) | Summarize payment statuses and follow-up items |
| Marketing / sales | [marketing.md](Lab/prompts/marketing.md) | [Product catalog](Lab/datasets/product_catalog.csv), user-supplied needs and budget | Recommend a product with a factual justification |
| Legal | [legal.md](Lab/prompts/legal.md) | User-supplied contract clauses; none are bundled | Summarize clauses neutrally |
| Developer / IT | [developer.md](Lab/prompts/developer.md) | User-supplied technical documents or logs; none are bundled | Explain technical material using supplied evidence |

Additional context files: [meeting notes](Lab/datasets/meeting_notes.txt) and [security policy](Lab/datasets/security_policy.txt). These short documents simulate business records; they are not current employer policies.

The CSV datasets contain **10 customer queries**, **6 invoices**, and **5 products**. Invoice amounts and product prices have no specified currency. Payment statuses are supplied labels, not a live calculation as of today's date.

## Customer-support prompt progression

| File | Main change |
| --- | --- |
| [customer_support.md](Lab/prompts/customer_support.md) | Short starter instruction |
| [customer_support-v1.md](Lab/prompts/customer_support-v1.md) | Adds ticket attributes and a 2–3 sentence response limit |
| [customer_support-v2.md](Lab/prompts/customer_support-v2.md) | Adds a specialist role and professional tone |
| [customer_support-v3.md](Lab/prompts/customer_support-v3.md) | Adds source-grounding and no-assumption constraints |
| [customer_support-v4.md](Lab/prompts/customer_support-v4.md) | Adds missing-evidence handling and five output fields |
| [customer_support-v5.md](Lab/prompts/customer_support-v5.md) | Provides three examples: a few-shot prompt |

Always attach or paste the relevant dataset content. A query ID or a filename alone does not provide a model with access to this repository. The v4 request for a root cause can exceed the available evidence; report it as unknown when the source does not establish one.

## Templates, evaluation, and reports

| Resource | Purpose |
| --- | --- |
| [Prompt template](Lab/templates/prompt_template.md) | Role, business context, objective, instructions, constraints, format, and success criteria |
| [Quality rubric](Lab/evaluation/prompt_quality_rubric.md) | Seven criteria rated from 1 to 5; includes a supplied example total |
| [Evaluation matrix](Lab/evaluation/prompt_matrix.md) | Supplied P1.1–P1.4 scores for three criteria |
| [Review checklist](Lab/evaluation/prompt_review_checklist.md) | Supplied review example; approval text is not production authorization |
| [Baseline response](Lab/outputs/baseline_response.md) | Supplied Microsoft Copilot response for ticket 1002 |
| [Prompt scorecard](Lab/reports/prompt_scorecard.md) | Supplied P1.1–P1.4 ratings and observations |
| [Version history](Lab/reports/prompt_versions.md) | Supplied revision log; incomplete relative to the prompt files |
| [Prompt library template](Lab/reports/prompt_library.md) | Blank catalog for learners to complete |
| [Best practices](Lab/reports/prompt_best_practices.md) | Prompt design recommendations |
| [Deployment guidelines](Lab/reports/deployment_guidelines.md) | Governance topics and readiness checklist |

Only one saved model response is included. Later-version scores lack matching saved outputs, and cross-model comparisons are not supplied. No new model executions or performance measurements were performed while preparing this repository.

For a new evaluation, save the exact prompt, source context, test record, provider/model identity, date, available settings, raw response, and criterion-level scores. Use several tickets and repeated runs before drawing conclusions about quality or consistency.

## Repository layout

- `instructions/` — original DOCX lab guide
- `Lab/datasets/` — three CSVs and five text context files
- `Lab/prompts/` — six support prompts and five other domain prompts
- `Lab/templates/` — reusable prompt template
- `Lab/outputs/` — supplied baseline response
- `Lab/evaluation/` — rubric, matrix, and review checklist
- `Lab/reports/` — scorecard, history, catalog template, and guidance
- `docs/` — preparation notes and a new practice walkthrough

## Source and reuse

Prepared from the supplied `6Benterprise_prompting.zip` training archive. Original materials are retained, except that the baseline response's personal SharePoint citation was replaced with a link to the included CSV and an explanatory note. macOS archive metadata was excluded.

Original document metadata and attribution are preserved. The archive did not include a collection-wide license or complete authorship information; no license has been assigned to third-party training materials. AI provider access and behavior depend on the tool you choose.
