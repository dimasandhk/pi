# CLAUDE.md

This repository holds an IEEE conference manuscript (`main.tex`, `references.bib`) for a Systematic Literature Review: *The Impact of Generative AI Coding Assistants on Developer Code Comprehension in Software Development and Maintenance*. Supporting review material lives in `supplementary/`.

## SLR methodology

For any work on this review — research questions, PICOC, protocol, search strategy, inclusion/exclusion criteria, screening, quality assessment / risk of bias, data extraction, synthesis, PRISMA/SEGRESS reporting, or methodology review — follow the project skill at `.claude/skills/systematic-literature-review/SKILL.md` (`systematic-literature-review`). Load it before working on any of these.

Non-negotiables from that skill:

- Never fabricate or guess citations, DOIs, or extracted findings; every claim must be verifiable against the actual paper.
- Never claim reviewer procedures (e.g., dual screening, agreement measures) that did not actually happen.
- Synthesize across studies by RQ/theme, not paper-by-paper, and avoid causal language the study designs don't support.
- Keep eligibility criteria separate from quality assessment, and record protocol deviations instead of silently changing criteria.

## SLR planning workbook (Google Sheets)

The review's working data lives in a Google Sheets workbook, the source of truth for counts, criteria, and per-study decisions:
https://docs.google.com/spreadsheets/d/162IHqoPQfsasatsZEHM1L3B6uDObZ_qKp4ygc5z2Yx8/edit

- Spreadsheet ID: `162IHqoPQfsasatsZEHM1L3B6uDObZ_qKp4ygc5z2Yx8`. Read it with the Google Sheets connector tools (`mcp__claude_ai_Google_Sheets__*`).
- Start with the `README` tab: it records the workflow, the QA scoring rule and threshold, and the **current review stage**. Don't rely on counts remembered from earlier sessions.
- Active workflow tabs: `PICOC_RQs` → `Search_Strategy` → `Protocol_Criteria` → `Raw_Articles` → `Initial_Screening` → `Full_Text_Screening` → `Quality_Assessment` → `Final_Papers` → `PRISMA_Counts`. The `Screening` and `Pilot_*` tabs are hidden audit/calibration history and are not part of the active workflow.
- Numbers in `main.tex` (record counts, PRISMA flow, QA results) must match the workbook. Where they differ, flag it rather than silently picking one.
- QA scores in `Quality_Assessment` may be AI-assisted drafts. Check the README for whether human confirmation is done before reporting them as final.
- Read-only by default. Don't write to the workbook unless explicitly asked.

## Manuscript conventions

- Unresolved placeholders use `\todo{...}` (rendered red); search for `\todo` to find them.
