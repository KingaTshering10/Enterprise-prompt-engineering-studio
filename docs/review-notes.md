# Review and preparation notes

## Scope

Inspected all 30 substantive files in `6Benterprise_prompting.zip`: 29 text/CSV/Markdown files and one DOCX guide. Read the guide's extracted paragraph text and checked its OOXML ZIP integrity. Embedded images and page layout were not visually reviewed. Parsed all three CSVs and checked record IDs and row structure. No LLM prompts were executed and no new scores or approvals were generated.

## Changes made for this package

- Removed macOS resource-fork metadata from the archive.
- Added the root README, `.gitignore`, this review record, and a self-contained customer-support practice walkthrough.
- Replaced the personal SharePoint citation in `Lab/outputs/baseline_response.md` with a local CSV link. Retained the response text and added a preparation note so the original citation is not mistaken for a model-generated local reference.
- Preserved every other original file byte-for-byte, including the DOCX guide, supplied scores, and unfinished templates.

## What the supplied records establish

- The customer-support sequence contains a starter and five numbered prompt files.
- The supplied baseline response identifies Microsoft Copilot, ticket 1002, and a July 8, 2026 date. It follows the three-sentence limit. Its troubleshooting and manual-reset suggestions go beyond the FAQ's password-reset entry.
- Scorecards and the matrix report improving P1.1–P1.4 scores, but only the baseline output is saved. Model build, settings, repeated runs, later raw responses, and independent grading are absent. These records do not establish reproducibility or measured production performance.
- The matrix evaluates three criteria; the scorecard lists four; the rubric defines seven. Their totals are not interchangeable. Matrix P1.3 reports 4.6 for a mean of 14/3 (about 4.67), while P1.2 uses one-decimal 4.3. Original values remain unchanged.
- The rubric's 30/35 and 4.3/5 example assessment is not tied to a named prompt with seven recorded criterion scores.

## Inconsistencies and unfinished work

1. `prompt_versions.md` still marks P1.4 as planned, although v4 and v5 files exist. It describes two output sections for P1.4, while v4 requests five fields. Its ordering is oldest-first despite its newest-first instruction.
2. `prompt_review_checklist.md` describes two output sections and marks P1.4 approved. That differs from the actual five-field prompt. Treat the approval as a supplied lab example.
3. The scorecard's P1.4 text omits the missing-document fallback found in the actual v4 file. It recommends production adoption without supporting later raw outputs or deployment validation.
4. v4 combines five output fields with a 2–3 sentence limit. It asks for a root cause that the ticket does not establish. The new walkthrough explicitly handles missing evidence and uses a consistent format.
5. v5 contains three examples, making it few-shot. The lab also requests one-shot testing, but no separate one-shot result or comparison is included. Example recommendations such as billing adjustments and API escalation are not all stated in the supplied FAQ; they should not be treated as approved policy.
6. `prompt_library.md` is a blank template. The root README provides a navigable catalog without inventing owners, version dates, or approvals.
7. The lab's marketing exercise requests product descriptions, whereas the supplied marketing prompt performs product selection. The README describes the actual prompt.
8. Contract clauses, technical logs, and customer product requirements are not supplied. Learners must provide suitable inputs for those tasks. The guide's cross-model comparison is an optional exercise with no supplied results.

## Dataset checks

| CSV | Data rows | Columns | ID field |
| --- | --- | --- | --- |
| `customer_queries.csv` | 10 | 5 | `query_id` |
| `invoice_records.csv` | 6 | 6 | `invoice_id` |
| `product_catalog.csv` | 5 | 5 | `product_id` |

IDs are unique within each CSV. All rows have the expected columns and no empty values. The guide describes the records as simulated enterprise data. Currency is unspecified; do not infer a currency symbol. Invoice status should be analyzed as recorded rather than reclassified against the current date without an explicit task instruction.

## Source context

The guide's modification metadata names Pauroosh Kaushal. This is source metadata, not an ownership or licensing determination. No collection-wide license was supplied, and packaging the materials does not transfer authorship or establish redistribution rights. The original ZIP remains the source of record.
