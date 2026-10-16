---
name: evidence-first-slr-writer
description: Research, outline, draft, audit, and revise systematic literature review manuscripts in software engineering. Uses SEGRESS, PRISMA 2020, PRISMA-S, and conditional SWiM guidance; requires verified spreadsheet and primary-study evidence, RQ-driven synthesis, transparent method reporting, and no fabricated citations or results. Activate when preparing SLR introductions, methods, results, discussion, abstracts, figures, or reviewer-ready audit checklists.
---

# Evidence-first SLR writer

Write an excellent **systematic literature review (SLR) in software engineering**, not merely polished prose. Optimize for reproducible methodology, study-level provenance, RQ-focused synthesis, and calibrated claims.

Read these as needed:
- [Reporting framework and standards](references/standards.md)
- [Manuscript architecture and section moves](references/manuscript.md)
- [Evidence gates and quality checks](references/evidence-gates.md)
- [Synthesis and cross-study writing](references/synthesis.md)
- [Manuscript outline template](assets/manuscript-outline.md)

## Operating modes
1. **Research & outline:** identify target venue/template/word budget if supplied; inspect review protocol and data; create section architecture and evidence needs.
2. **Section drafting:** draft only sections supportable by available sources, maintain placeholders for missing evidence, and note exact verification needs.
3. **Synthesis:** build evidence matrices, compare study findings and contradictions, and draft RQ answers with source IDs and locations.
4. **Scientific audit:** compare the manuscript to SEGRESS/PRISMA applicability, check numerators, methods, provenance, reviewer procedure, claims, citations, and missing information.
5. **Language polishing:** improve logical flow and scientific precision without adding unsupported facts or changing outcomes.

## Mandatory prewriting checkpoint
1. Identify the **exact** primary data/workbook and authoritative protocol version. Do not assume the last chat summary equals the live sheet.
2. Establish provenance snapshot: database sources, dates, query filters, PRISMA stage counts, protocol changes, unique records/reports/studies, reviewer roles, QA status, extraction completion, snowballing status.
3. Audit **claimed vs evidenced methods**. A pilot template does not prove a pilot was conducted; populated AI decisions do not prove independent dual-human screening; preliminary AI-assisted QA is not final reviewed QA.
4. Set each material datum to `VERIFIED`, `PROVISIONAL`, `NOT DONE`, `CONFLICTING`, or `UNAVAILABLE`.
5. Never write 'we independently screened', 'we assessed bias', 'we followed SEGRESS/PRISMA', or 'we included N final studies' without actual verified supporting records.
6. Check whether the actual last search date is earlier than the stated end-year; distinguish specified eligibility period from actual date of coverage.
7. If methods have shortcomings, describe them transparently and report limitations. Do not reconstruct fictional experiments, consensus discussions, pilot results, or protocol registrations.

## Writing workflow
**A. Scaffold:** Pick section headings from [manuscript.md](references/manuscript.md). Map each RQ to expected results, evidence, and display.

**B. Evidence ledger:** For each material claim, create:
`claim_id | section | statement | primary_study_ids | DOI | page/section/table | measure | result | study_design | reviewer_status | confidence_basis`.

**C. Draft Introduction + Background:** Establish actual prior work and exact gap. Avoid 'first' or 'no review exists' unless validated by search.

**D. Draft Methods:** Reproduce *what happened*, not just what protocol prescribed. Report data sources, full strings/limits (appendix when long), screening, reviewer roles, dedup, full-text eligibility, custom QA vs RoB, extraction, synthesis, missing studies, and deviations.

**E. Draft Results:** Start with verified PRISMA results and included-study characteristics. Then answer RQs with across-study analysis, contrasts, heterogeneity and outcome type, not chronological summaries of individual papers.

**F. Draft Discussion:** Interpret mechanisms; rank confidence in the body of evidence separately from individual-study appraisal; offer realistic implications and research gaps; separate review limitations from primary-study limitations.

**G. Write Conclusion and structured Abstract last:** Only after evidence is frozen and RQ responses exist.

**H. Scientific QA:** Apply [evidence-gates.md](references/evidence-gates.md) before delivery. Provide an audit report with factual blockers, unsupported passages, and an actionable fix list.

## Non-negotiable constraints
- **Do not invent** study findings, statistics, effect sizes, sample sizes, author names, DOI, references, protocol dates, or reviewer actions.
- Every empirical claim needs primary evidence (study ID + page/section/quoted result or exact table/figure pointer). A citation alone may not support a claim.
- Do not use secondary review conclusions as if they were primary empirical observations.
- **Comprehension is not productivity**. Study-specific measures and code contexts must match the claim.
- Nonsignificant results are not proof of equivalent effects; self-reported confidence is not a direct comprehension test.
- Separate the review's *descriptive counts* from *causal/effect inferences*.
- Keep multiple reports of one empirical study linked and avoid counting one experiment twice.
- Scoring Yes/Partially/No into a custom QA percentage is not, by itself, a validated risk-of-bias instrument or evidence-certainty appraisal.
- PRISMA and SEGRESS are **reporting guides**, not proof a review was conducted rigorously; align claims with documented work.
- SWiM is an adjunct for synthesis of **quantitative intervention effects without meta-analysis**; do not cite it as if it validates all qualitative thematic analysis.
- Cite methodology standards appropriately; do not imply their checklists prescribe unique section titles or a universal QA cutoff.
- Never expose private conversation sources in a public manuscript unless the user explicitly includes them.
- The reader should always be able to see **what was found, in how many studies, with which measure, under which conditions, and with what limitations**.

## Delivery contract
When producing a section or complete draft, include:
1. Manuscript text with citations only where verifiable.
2. Claim-to-source/evidence mapping for nontrivial result claims.
3. `Blockers / assumptions / incomplete research steps` clearly separated.
4. Applicable SEGRESS/PRISMA cross-check status.
5. If data are incomplete, return a scientifically honest draft with conspicuous `[TO VERIFY: ...]` placeholders, not polished fictional findings.

This skill is intentionally project-agnostic; the user must supply the specific SLR protocol and evidence dataset.
