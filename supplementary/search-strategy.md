# Supplementary SLR Search Strategy

**Executed:** 17 September 2026. **Protocol publication window:** 2021–2026, subject in practice to availability by the actual search date. **Language:** English. **Study types:** peer-reviewed journal articles and conference papers (ScienceDirect interface: Research articles).

These exact queries and audit counts are based on the review team's Search_Strategy log. Their inclusion here supports reproducibility and does not imply that uncompleted review steps have been finished.

## Scopus — SC-S1

**Field:** TITLE-ABS-KEY. **Filters:** Article + Conference paper; English.

    TITLE-ABS-KEY ( ( "generative AI" OR "generative artificial intelligence" OR "large language model*" OR LLM OR GPT OR ChatGPT OR Copilot OR Codex OR "AI assistant*" OR "coding assistant*" OR "programming assistant*" OR "AI pair programm*" ) AND ( comprehension OR comprehend* OR "code understanding" OR "program understanding" OR "understanding code" OR "understanding the code" OR explanat* OR "mental model*" OR "cognitive load" ) AND ( code OR program* OR software ) ) AND PUBYEAR > 2020

**Counts:** raw export 3,265; after publication-type filter 2,979; after English-language filter 2,948. Removed 43 records dated 2027 to enforce the protocol cutoff, leaving **2,905** for global merging.

**Known search limitation:** an initial overly broad comprehension-query pilot was narrowed because general-purpose terms retrieved many unrelated papers. The reduction in recall for a validation study was logged as a search-strategy change.

## IEEE Xplore — IE-S1

**Field:** All Metadata. **Filters:** year 2021–2026; Conferences and Journals.

    (("All Metadata":"generative AI" OR "All Metadata":"large language model*" OR "All Metadata":LLM OR "All Metadata":GPT OR "All Metadata":ChatGPT OR "All Metadata":Copilot OR "All Metadata":Codex OR "All Metadata":"coding assistant*" OR "All Metadata":"programming assistant*") AND ("All Metadata":comprehension OR "All Metadata":comprehend* OR "All Metadata":"code understanding" OR "All Metadata":"program understanding" OR "All Metadata":explanat* OR "All Metadata":"mental model*" OR "All Metadata":"cognitive load") AND ("All Metadata":code OR "All Metadata":program* OR "All Metadata":software))

**Counts:** 1,694 initial; **1,591** after filters. Exported across seven batches; no missing abstract, 30 missing DOI, and three same-normalized-title groups flagged for manual examination.

## ScienceDirect — SD-S1 through SD-S5

**Field:** Title, abstract or author-specified keywords. **Filters:** 2021–2026, English, Research articles.

### SD-S1 — 68 hits

    ("generative AI" OR "large language model" OR LLM) AND (comprehension OR "code understanding") AND (code OR software)

### SD-S2 — 10 hits

    (ChatGPT OR Copilot OR Codex) AND (comprehension OR "code understanding") AND (code OR software)

### SD-S3 — 1 hit

    ("AI assistant" OR "coding assistant" OR "programming assistant") AND (comprehension OR "code understanding") AND (code OR software)

### SD-S4 — 10 hits

    ("generative AI" OR "large language model" OR LLM) AND ("mental model" OR "cognitive load") AND (code OR software)

### SD-S5 — 3 hits

    (ChatGPT OR Copilot OR Codex) AND ("mental model" OR "cognitive load") AND (code OR software)

**Count:** 92 query hits, including within-ScienceDirect overlap. The exported metadata contained 82 unique DOI values, seven repeated DOI groups, and ten repeated occurrences. All 92 hits entered the global merge to preserve the Identification audit trail.

## ACM Digital Library

The original protocol listed ACM Digital Library, but the search was **not executed** because access was unavailable. This deviation was logged. Subsequent backward and forward citation searching is planned as a partial recall mitigation, not a guarantee of complete coverage of ACM-only studies.

## Working study-selection audit (snapshot of review workbook)

| Stage | Count | Evidence status |
|---|---:|---|
| Database records merged | 4,588 | Recorded |
| Duplicate records marked | 845 | Recorded |
| Unique records initially screened | 3,743 | AI-assisted criteria decisions |
| Excluded on title/abstract | 3,713 | AI-assisted criteria decisions |
| Full-text candidate reports | 30 | Recorded |
| Reports included after full-text | 24 | Recorded |
| Reports excluded after full-text | 6 | Recorded |
| Preliminary QA scored | 24 | AI-assisted; human review pending |
| Human QA confirmed | 0 | Not completed in recorded worksheet |
| AI-assisted extracted entries | 24 | Human verification pending |
| Snowballing records | 0 | Not yet executed |

Do not equate records, reports, and independent empirical studies in the final PRISMA diagram without checking any publication-version overlap. The protocol describes an independent four-reviewer pilot and double screening, but the pilot reviewer decision cells currently do not document its completion; no Krippendorff alpha is reported.

**Working protocol and evidence:** https://docs.google.com/spreadsheets/d/162IHqoPQfsasatsZEHM1L3B6uDObZ_qKp4ygc5z2Yx8/edit

**Writing caution:** The main manuscript's existing abstract contains final-sounding study-effect counts; these were not newly verified for this methodology draft and should be reconciled with the final human-reviewed extraction before submission.
