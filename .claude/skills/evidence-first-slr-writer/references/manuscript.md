# Manuscript blueprint and paragraph moves

These are **recommended patterns**, not mandatory named sections. Follow journal/course formatting when specified.

## Front matter
- **Title:** states topic, population/outcome/scope as practical, and 'Systematic Literature Review'.
- **Abstract:** Background/Context (why); Objective/Aims (what RQs); Method (actual data sources/search date and verified final study count); Results (key evidence answers, not merely PRISMA count); Conclusion (qualified implication). Write last.
- **Keywords:** domain concepts, intervention, outcome, method.

## 1 Introduction: six moves
1. Concrete engineering problem + stakes.
2. New technology / workflow and competing claims.
3. Why outcome deserves separate attention (e.g. code comprehension vs speed).
4. Existing primary evidence and existing secondary reviews, fairly characterized.
5. Gap clearly bounded by population, tasks, outcome, dates and/or method.
6. Objective, RQs, contributions + brief roadmap.

Evidence requirement: cite supporting literature, particularly for broad claims, and do not self-declare novelty without verification.

## 2 Background and related reviews
- Define central constructs operationally, especially direct comprehension vs close proxies.
- Present relevant prior SLRs in a **comparison table**:
  `Review | Time window | Population | Intervention | Outcome | Context | How present review differs`.
- Avoid equating the previous review's absence of your exact title with absence of prior coverage.
- Keep Background explanatory, not a rehearsal of Results.

## 3 Method / Review design
3.1 Protocol, reporting framework, changes and availability.
3.2 RQs and PICOC / scope.
3.3 Sources, exact search date and date window.
3.4 Search-string derivation/pilot, per-platform queries, limits and search validation.
3.5 Record management, dedup and multiple reports.
3.6 IC/EC eligibility and screening; how many independent reviewers, conflict resolution, automation.
3.7 Full text retrieval and exclusions.
3.8 Quality appraisal / RoB (actual instrument and threshold justification, reviewer confirmation).
3.9 Extraction template and procedure, treatment of missing data.
3.10 Synthesis method, planned grouping, contradictions/heterogeneity and any certainty assessment.
3.11 Snowballing/completeness and deviations.
- Link supplementary assets: search log, raw exports, screening decision logs, QA ledger, extraction sheet, code/notebooks.
- Do not label unaudited or uncompleted steps as performed.

## 4 Results: evidence first
4.1 Study selection with PRISMA flow and stage-by-stage counts.
4.2 Characteristics of included studies (year, participant experience, design, task, tool, outcome measure, industry/student distinctions).
4.3 RQ1 **effects on developer comprehension**: group by direct/proxy measure, AI vs control where possible, direction of reported effect, context, uncertainty and contradictions.
4.4 RQ2 **assistant and support forms**: group into grounded tool families and interaction modes; counts only with a well-defined denominator.
4.5 RQ3 **study designs and measurement**: direct vs proxies, participant characteristics, codebase/task realism, strength/limitation of evidence.
4.6 RQ4 **challenges and mechanisms**: code qualitative reports into themes, show contributing study IDs and counterexamples.
4.7 Optional cross-RQ synthesis: e.g. which support form in which tasks/experience settings yielded which measured consequences (only if evidence).

Do not have a subsection that consists solely of one paragraph per paper.

## 5 Discussion: inference and scope
- Answer each RQ at a higher conceptual level, with explicit boundaries.
- Explain heterogeneity; seek moderators such as task, expertise, model mode, generated vs existing code, direct vs self-report outcome.
- Discuss contradictions and negative/null results.
- Distinguish *strength/certainty of a synthesized claim* from per-paper QA.
- Derive **conditional** implications for practitioners and **testable** research directions.
- Avoid claims of causality when primary studies are observational or survey-only.

## 6 Limitations
A. Review process: source choice, access gaps, English-only, date truncation, selection/AI assistance, screening independence, incomplete full texts, extraction, synthesis choices and possible missing negative results.
B. Included primary studies: small samples, student-only populations, artificial tasks, weak measures, single tools/models, short duration, uncontrolled confounders, publication bias.

## 7 Conclusion
- Answers the question(s) directly, no new empirical fact.
- Distinguish what evidence supports vs what remains uncertain.
- Give a bounded recommendation/future agenda.

## Figures and tables
1. PRISMA 2020 flow with correct unit (records/reports/studies).
2. Included study overview (study ID, design, participants, task, assistant, outcome measure).
3. Evidence matrix (direct/proxy × positive/null/mixed/negative × task/participant group).
4. Quality appraisal table (instrument criteria and results).
5. Thematic challenge map with study provenance where supported.
Keep figures readable in grayscale and do not invent data to fill empty cells.

## Writing tone
Scientific, clear, precise, transparent and restrained. Prefer 'reported', 'observed', 'associated with' over 'proved', unless causal design justifies stronger language. Use exact sample sizes and effect direction when supported, without confounding timing/performance with comprehension.
