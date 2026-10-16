---
name: systematic-literature-review
description: Guide Systematic Literature Reviews (SLRs) and related secondary studies in Computer Science, Information Technology, and Software Engineering. Use for SLR topic formulation, PICOC, research questions, review protocols, search strategies, inclusion and exclusion criteria, quality assessment or risk of bias, screening, snowballing, data extraction, synthesis, PRISMA flow reporting, SEGRESS reporting, and evaluating review methodology.
---

# Systematic Literature Review (SLR) Skill for Computer Science / Software Engineering

## Purpose

Use this skill when helping with a **Systematic Literature Review (SLR)**, systematic mapping study, tertiary study, or closely related secondary study in Computer Science, Information Technology, or Software Engineering.

The goal is to make the review **systematic, auditable, reproducible, and appropriately scoped**, not merely to collect many papers.

This skill is based primarily on:

- Kitchenham & Charters' Software Engineering SLR guidelines.
- Current Evidence-Based Software Engineering (EBSE) guidance.
- Kitchenham, Madeyski & Budgen's **SEGRESS** reporting guidelines (2023).
- **PRISMA 2020** for transparent reporting and study-flow documentation.
- Wohlin's snowballing guidance.
- Later Software Engineering research on search validation and quality assessment.

---

# 1. Core Principles

Always apply these principles.

1. **Research Questions drive everything.**
   - Search strategy must be capable of finding evidence relevant to the RQs.
   - Inclusion/exclusion criteria must align with the RQs.
   - Data extraction fields must collect what is needed to answer the RQs.
   - Synthesis must directly answer the RQs.

2. **Write the protocol before doing the full review.**
   Define the intended procedure first so decisions are not changed merely because of the papers that happen to be found.

3. **Pilot before committing.**
   Test the RQs, search strings, eligibility criteria, QA/Risk-of-Bias questions, and extraction form on a small set of known papers.

4. **Record decisions.**
   A good SLR leaves an audit trail showing what was searched, when, what was found, why papers were excluded, what data was extracted, and how conclusions were produced.

5. **Prefer reproducibility over convenience.**
   Save exact queries, database names, search dates, result counts, deduplication rules, screening decisions, exclusion reasons, QA results, extraction data, and analysis scripts when applicable.

6. **Do not confuse SLR with meta-analysis.**
   - SLR = systematic review process.
   - Meta-analysis = a statistical synthesis technique that may be used inside an SLR when sufficiently comparable quantitative evidence exists.
   - An SLR does **not** need a meta-analysis.

7. **PRISMA is primarily a reporting guideline, not the methodology for conducting the review.**
   Use it to improve transparency, especially the flow diagram and reporting checklist. For Software Engineering reporting, prefer **SEGRESS**, which adapts modern reporting guidance to SE secondary studies.

8. **Do not optimize for the number of included papers.**
   A smaller set of relevant, defensible studies is better than a large noisy set.

9. **Do not invent methodological rigor.**
   If the review is performed by one student, say so and mitigate the limitation instead of pretending that two independent reviewers existed.

10. **AI may assist, but humans remain responsible for evidence.**
    AI can help generate synonyms, organize papers, propose classifications, or perform a first-pass extraction, but every citation, screening decision, extracted datum, and synthesized claim must be verifiable against the actual paper.

---

# 2. First Decision: Is SLR the Right Type of Study?

Before designing the review, classify the intended secondary study.

## Use a Systematic Mapping Study when

The question is broad and primarily asks things such as:

- What research exists on topic X?
- What methods, domains, tools, datasets, or publication trends exist?
- How has research on X evolved?
- Where are the research gaps?

Typical output: categories, trends, research clusters, evidence gaps.

## Use a conventional SLR when

The question asks for a synthesized answer to a focused issue, for example:

- What benefits and limitations of X have been reported?
- What factors influence X?
- How effective is X compared with Y?
- What evidence supports the use of X in context Y?

Typical output: synthesized findings answering explicit RQs.

## Use a meta-analysis only when

The included studies are sufficiently comparable in:

- intervention/exposure,
- population/context,
- outcome definition,
- study design,
- quantitative effect measure.

If studies are heterogeneous, use narrative, thematic, descriptive, vote-counting-with-caution, or other appropriate synthesis instead of forcing a meta-analysis.

---

# 3. The Three Main SLR Phases

Use this mental model throughout the project.

## Phase A: Planning

1. Justify the need for the review.
2. Define scope and objectives.
3. Formulate RQs.
4. Build PICOC or another question-framing model when useful.
5. Define the protocol.
6. Define search strategy.
7. Define inclusion/exclusion criteria.
8. Define screening process.
9. Define QA / Risk-of-Bias process.
10. Define data extraction.
11. Define synthesis.
12. Pilot the protocol and revise it before the full search.

## Phase B: Conducting

1. Execute searches exactly as documented.
2. Export all records.
3. Deduplicate.
4. Screen title/abstract.
5. Retrieve full text.
6. Screen full text.
7. Record exclusion reasons.
8. Perform QA / Risk-of-Bias assessment.
9. Extract data.
10. Synthesize evidence.
11. Record deviations from protocol.

## Phase C: Reporting

1. Report the full methodology.
2. Show paper counts at each stage.
3. Use a PRISMA-style flow diagram where appropriate.
4. Present characteristics of included studies.
5. Answer every RQ with traceable evidence.
6. Discuss limitations of both the review process and the evidence base.
7. Report protocol deviations.
8. Provide supplementary data when possible.

---

# 4. Research Questions (RQs)

## Rules for good RQs

A good SLR RQ should be:

- answerable from existing literature,
- neither extremely broad nor impossibly narrow,
- specific enough to determine relevance,
- connected to the intended synthesis,
- phrased without assuming a desired result.

Avoid vague questions such as:

> What is the best DevOps method?

Prefer:

> RQ1. What benefits of DevOps adoption in software development organizations are reported in empirical studies?
>
> RQ2. What challenges or barriers to DevOps adoption are reported?
>
> RQ3. What organizational or technical factors are associated with successful DevOps adoption?

## Keep RQ count manageable

For a student SLR, **2–4 strong RQs** is usually more manageable than many overlapping questions.

Every RQ should have a clear mapping to extraction fields.

Example:

| RQ | Required extraction fields |
|---|---|
| RQ1 Benefits | reported benefit, metric/evidence, study context |
| RQ2 Challenges | challenge, cause, consequence, context |
| RQ3 Success factors | factor, evidence, context, reported effect |

If an RQ has no clear extraction fields, it is probably too vague.

---

# 5. PICOC

PICOC is useful for structuring the problem, particularly for comparison or intervention-style questions.

- **P – Population**: Who/what is being studied?
- **I – Intervention**: Technology, method, practice, treatment, approach.
- **C – Comparison**: Alternative intervention/baseline, if applicable.
- **O – Outcome**: Desired effect or measured result.
- **C – Context**: Environment, domain, organization, project setting.

Example:

Topic: DevOps and deployment performance.

| Element | Example |
|---|---|
| Population | software development teams / organizations |
| Intervention | DevOps practices |
| Comparison | traditional siloed development/operations or no explicit comparison |
| Outcome | deployment frequency, lead time, failure rate, recovery time |
| Context | industrial software engineering projects |

Possible RQ:

> How do DevOps practices affect software delivery performance in industrial software-development contexts?

### Important nuance

Do **not** mechanically convert every PICOC element into a search block.

A search string built from all five PICOC elements may become so restrictive that it misses relevant papers. Later SE methodology research recommends validating search strings against known relevant studies rather than assuming a mechanically derived structured string is sufficient.

Use PICOC to understand the question. Use evidence and pilot searches to build the search string.

---

# 6. Review Protocol

Prepare the protocol **before the full search**.

Minimum protocol sections:

1. Title / topic.
2. Background and motivation.
3. Objective.
4. Research Questions.
5. PICOC or equivalent framing, if relevant.
6. Search sources/databases.
7. Search strings for each source.
8. Search period/date limits and justification.
9. Inclusion criteria.
10. Exclusion criteria.
11. Deduplication rule.
12. Screening stages.
13. Reviewer procedure / disagreement handling.
14. QA or Risk-of-Bias instrument.
15. QA scoring/threshold, if used.
16. Data extraction form.
17. Data synthesis plan.
18. Tools used.
19. Expected limitations.
20. Protocol-change policy.

## Protocol-change policy

Changes are allowed after piloting or when an unforeseen issue appears, but:

- document what changed,
- document why,
- document when,
- explain whether the change could bias the result.

Never silently rewrite criteria after seeing inconvenient results.

---

# 7. Search Strategy

## Recommended search-source approach for CS / IT / SE

A defensible combination often includes:

- Scopus and/or Web of Science as broad indexing systems.
- IEEE Xplore for engineering/computing.
- ACM Digital Library for computing.
- Optional publisher databases such as ScienceDirect or SpringerLink if justified.
- Google Scholar mainly as a complementary discovery tool rather than the only reproducible database.
- Backward and forward snowballing for completeness.

The exact set depends on institutional access and the course requirements.

## Build search concepts

Identify 2–4 central concept groups.

Example:

**Concept A: DevOps**

- "DevOps"
- "continuous delivery"
- "continuous deployment"

**Concept B: adoption**

- adoption
- implementation
- transition
- transformation

**Concept C: software organization**

- "software development"
- "software engineering"
- "software team"

Then construct:

```text
("DevOps" OR "continuous delivery" OR "continuous deployment")
AND
(adoption OR implementation OR transition OR transformation)
AND
("software development" OR "software engineering" OR "software team")
```

## Search-string rules

- Use **OR** for synonyms within one concept.
- Use **AND** between different concepts.
- Use parentheses explicitly.
- Quote multi-word phrases when the database supports it.
- Consider spelling variants and abbreviations.
- Do not add terms merely because they sound academic.
- Avoid overly specific Outcome terms if they cause known relevant papers to disappear.
- Adapt syntax to each database. Do not assume one query syntax works identically everywhere.

## Quasi-Gold Standard / Known Studies

Before finalizing the search, identify several papers that are already known to be relevant through:

- preliminary Google Scholar exploration,
- lecturer/supervisor suggestions,
- related SLRs,
- highly cited seed papers.

Use these as **known studies** to test the search.

Ask:

- Does the query retrieve each known study?
- If not, why?
- Is an important synonym missing?
- Is a concept block too restrictive?
- Is the paper not indexed by the database?

Do not simply tune the search forever to retrieve one weirdly titled paper. Understand *why* it was missed.

If possible, use one known set to help construct the query and another independent set to validate it.

## Search log

For every search, save:

| Field | Example |
|---|---|
| Database | Scopus |
| Search date | 2026-09-04 |
| Search fields | TITLE-ABS-KEY |
| Exact query | ... |
| Filters | English, 2018–2026 |
| Results | 428 |
| Export format | CSV/RIS/BibTeX |
| Notes | query version v3 |

This table is part of the reproducibility evidence.

---

# 8. Snowballing

Snowballing complements database search and can sometimes be the primary search strategy.

## Backward snowballing

Inspect the reference lists of included/seed studies to identify older relevant work.

## Forward snowballing

Inspect later papers that cite included/seed studies.

## Iteration

For a snowballing-driven review:

1. Start with a defensible seed set.
2. Perform backward + forward snowballing.
3. Screen new candidates.
4. Repeat from newly included papers.
5. Stop when an iteration finds no new relevant studies.

Record:

- seed set,
- iteration number,
- candidate count,
- included count,
- duplicate count,
- stopping rule.

Do not perform undocumented citation browsing and call it systematic snowballing.

---

# 9. Inclusion and Exclusion Criteria

## Principle

Eligibility criteria determine **relevance to the review**.

They are not the same as Quality Assessment.

### Inclusion criteria answer

> Does this study belong in the evidence set for my RQ?

### Quality / Risk-of-Bias answers

> How trustworthy is the evidence in this included study?

## Write criteria before screening

Each criterion should be:

- objective enough to be applied consistently,
- justified,
- non-redundant,
- traceable to the RQ or practical scope.

## Example Inclusion Criteria

```text
IC1. The study investigates [target topic/intervention].
IC2. The study reports empirical evidence relevant to at least one RQ.
IC3. The study is a peer-reviewed journal or conference paper.
IC4. The full text is available.
IC5. The paper is written in English.
IC6. The paper was published between YYYY and YYYY.
```

Only use IC3–IC6 if they are appropriate for the assignment, and justify restrictions such as language/date/publication type.

## Example Exclusion Criteria

```text
EC1. The paper is not relevant to the review topic after full-text inspection.
EC2. The paper is a secondary/tertiary study when the target evidence is primary empirical research.
EC3. The paper is editorial, tutorial, poster abstract, slide deck, or other non-eligible publication type.
EC4. The paper does not report sufficient empirical evidence to answer any RQ.
EC5. The paper is a duplicate record.
EC6. Multiple papers report the same empirical study; link the reports under one study ID rather than double-counting the study.
```

### Important duplicate nuance

Two database records of the same article are duplicates and one record should be removed.

But a conference paper and later journal paper may be **different reports of the same study**. Do not blindly discard one version. Link both reports to one study identifier and extract complementary details without double-counting the study.

---

# 10. Screening Process

Recommended stages:

## Stage 0: Deduplication

Remove duplicate bibliographic records.

Record:

- records before deduplication,
- duplicates removed,
- records after deduplication.

## Stage 1: Title + Abstract screening

Classify each record as:

- Include / potentially relevant,
- Exclude,
- Uncertain.

When uncertain, prefer moving the paper to full-text review rather than excluding it too early.

## Stage 2: Full-text screening

Apply IC/EC to the full paper.

For every exclusion at full-text stage, record one primary exclusion reason.

Examples:

- wrong population/context,
- wrong intervention/topic,
- no empirical evidence,
- wrong publication type,
- secondary study,
- duplicate study report.

## Reviewer reliability

Ideal:

- at least two independent reviewers screen each candidate,
- disagreements are resolved by discussion or a third reviewer,
- agreement is measured during the process.

For a solo undergraduate review:

- pilot a sample with the lecturer/supervisor or teammate if possible, **or**
- perform a test-retest: rescreen a random sample after several days without looking at the original decision,
- report this limitation transparently.

Do not claim dual screening unless it actually happened.

---

# 11. Quality Assessment (QA) / Risk of Bias (RoB)

Modern SEGRESS terminology favors **Risk of Bias** over the generic term **Quality Assessment**, although many courses and older papers still use QA.

Use whichever terminology your course requires, but understand the distinction.

## QA principles

- QA criteria should reflect the study designs you expect to include.
- Pilot the instrument.
- Do not judge a survey by the exact same methodological details as an experiment if those details are not applicable.
- Require evidence/explanation for each score.
- Do not use journal ranking as a substitute for methodological quality.

## A practical undergraduate QA checklist

For mixed empirical SE papers, the following is a reasonable **starting template**, not a universal standard:

### QA1. Clarity of objective

Is the study objective / research question clearly stated?

### QA2. Method appropriateness

Is the research method appropriate and adequately described?

### QA3. Data/sample transparency

Are participants, dataset, projects, cases, or sampling procedures sufficiently described?

### QA4. Analysis rigor

Is the data-analysis procedure clear and appropriate for the data?

### QA5. Evidence supports conclusions

Are the claims/conclusions supported by the reported results?

### QA6. Limitations / threats

Does the study discuss relevant limitations, threats to validity, or potential sources of bias?

### QA7. Reproducibility / traceability

Is enough methodological information reported for the study to be understood or reasonably replicated?

### QA8. Relevance to the target context

Is the evidence relevant to the population/context represented by the review question?

## Simple scoring option

If your lecturer requires numeric QA scoring:

```text
Yes / clearly satisfied        = 1.0
Partially / unclear            = 0.5
No / not satisfied             = 0.0
Not applicable                 = N/A
```

Calculate percentage over **applicable** items, not over N/A items.

Example:

```text
QA percentage = obtained score / maximum applicable score × 100%
```

## Threshold rule

There is **no magical universal QA threshold** that automatically makes a paper scientifically valid.

If the course requires a threshold:

1. define it in the protocol before completing QA,
2. justify it,
3. pilot it on known studies,
4. consider whether any criterion should be mandatory regardless of total score.

Example classroom rule:

```text
Include in synthesis if QA >= 60%
AND QA5 (evidence supports conclusions) is not 0.
```

Treat that as a **review-specific operational rule**, not an international SLR law.

## Better modern alternative

When your lecturer allows it, an ordinal Risk-of-Bias judgment may be more meaningful than summing unrelated QA questions:

- Critical
- Serious
- Moderate
- Low
- Very low

Each judgment should have a written rationale.

Do not pretend numeric precision is objective when the underlying assessment is subjective.

## Sensitivity analysis

Instead of only deleting low-QA papers, consider:

- synthesizing all eligible studies,
- then re-checking conclusions after removing high-risk / low-quality studies.

If conclusions change substantially, report that explicitly.

---

# 12. Data Extraction

Never start full extraction without a predefined form.

## Basic bibliographic fields

- Study ID
- Paper ID/report ID
- Title
- Authors
- Year
- Venue
- DOI/URL
- Publication type

## Study-characteristic fields

- Country/region
- Domain/industry
- Study design
- Population/participants
- Sample size
- Dataset
- Technology/method studied
- Comparison/baseline
- Context

## Evidence fields

Create fields directly from each RQ.

Example:

```text
RQ1 finding
RQ1 supporting evidence/metric
RQ2 challenge
RQ2 cause
RQ2 consequence
RQ3 success factor
RQ3 reported effect
Author-stated limitations
Reviewer notes
QA/RoB result
```

## Extraction rules

- Prefer structured fields over one giant notes column.
- Save page/section location for important extracted claims.
- Distinguish authors' conclusions from your interpretation.
- Do not double-count a study reported in multiple papers.
- Pilot the form on several different study types.

If two reviewers exist, independently extract at least a sample, compare, then resolve disagreements.

---

# 13. Data Synthesis

Choose synthesis based on the RQ and evidence, not because a method sounds sophisticated.

## Descriptive synthesis

Useful for:

- papers per year,
- venues,
- study methods,
- countries,
- domains,
- datasets,
- tools.

Output: tables, counts, plots.

## Narrative synthesis

Useful when evidence is heterogeneous.

Structure around:

- RQs,
- themes,
- types of evidence,
- contexts,
- agreements/disagreements.

Do not merely summarize Paper A, then Paper B, then Paper C. Synthesize *across* studies.

Weak:

> Study A found X. Study B found Y. Study C found X.

Better:

> X was reported in 7 of 10 studies, particularly in large industrial teams, while three small academic studies reported no clear improvement. Differences appear related to context and measurement method.

## Thematic synthesis / coding

Useful for qualitative findings such as benefits, challenges, adoption factors, or practitioner perceptions.

Process:

1. extract relevant statements/findings,
2. code them,
3. group similar codes,
4. define themes,
5. iteratively refine theme definitions,
6. count studies supporting each theme where appropriate,
7. preserve contextual differences.

Count **studies**, not repeated mentions inside one verbose study, unless your analysis explicitly needs within-study frequency.

## Meta-analysis

Use only if appropriate.

Before pooling, check:

- compatible outcome definitions,
- compatible effect measures,
- study-design comparability,
- independence,
- heterogeneity,
- missing statistics.

If you cannot justify pooling, do not pool.

---

# 14. Reporting with PRISMA and SEGRESS

## PRISMA flow

At minimum report counts for:

1. Records identified.
2. Duplicates removed.
3. Records screened.
4. Records excluded after title/abstract.
5. Full texts assessed.
6. Full texts excluded, with reasons.
7. Studies included.

Keep the unit clear:

- **record/report/article** is not always the same as
- **empirical study**.

## SEGRESS

For Software Engineering, use SEGRESS as the main reporting checklist when possible.

The report should make clear:

- why the review was needed,
- what RQs were used,
- the protocol,
- eligibility criteria,
- complete search strategy,
- selection procedure,
- extraction procedure,
- RoB/QA procedure,
- synthesis procedure,
- evidence for each RQ,
- limitations,
- protocol deviations,
- implications/recommendations.

## Limitations section

Discuss limitations at two levels.

### Limitations of the review process

Examples:

- only one reviewer,
- limited database access,
- English-only restriction,
- date restriction,
- possible search-string bias,
- no grey literature,
- extraction subjectivity.

### Limitations of the evidence base

Examples:

- small samples,
- mostly academic experiments,
- little industrial validation,
- geographically concentrated studies,
- inconsistent metrics,
- high risk of bias,
- contradictory findings.

Do not hide limitations. Explain their likely effect on conclusions.

---

# 15. Suggested SLR Spreadsheet / Dataset Schema

Use columns similar to these.

```text
record_id
study_id
title
authors
year
venue
doi
source_database
search_batch
duplicate_of
stage_1_decision
stage_1_reason
stage_2_decision
stage_2_reason
inclusion_criteria_met
exclusion_criterion
qa1
qa2
qa3
qa4
qa5
qa6
qa7
qa8
qa_total
qa_percentage
risk_of_bias
study_design
population
sample_size
context
intervention
comparison
outcomes
rq1_data
rq2_data
rq3_data
limitations
extractor_notes
```

Keep raw search results separate from the cleaned master dataset.

---

# 16. Minimum Student Workflow

When the course timeline is short, do **not** delete methodological steps. Simplify their scale.

A practical workflow:

1. Pick a focused topic.
2. Find 3–8 initial known relevant papers.
3. Formulate 2–4 RQs.
4. Build PICOC if appropriate.
5. Write IC/EC.
6. Build and pilot search strings.
7. Decide databases.
8. Write QA/RoB questions and scoring rule.
9. Write extraction table.
10. Freeze protocol v1.
11. Run all searches.
12. Export + deduplicate.
13. Title/abstract screening.
14. Full-text screening.
15. Record exclusion reasons.
16. QA/RoB.
17. Extract RQ data.
18. Synthesize across studies.
19. Build PRISMA flow.
20. Write methods + results + limitations.
21. Check every conclusion against extracted evidence.

---

# 17. Quality Gates

Before allowing the review to proceed to the next stage, check these gates.

## Gate A: Topic → Protocol

Pass only if:

- the topic is suitable for an SLR rather than a vague literature review,
- RQs are answerable,
- scope is realistic,
- each RQ has defined data needs.

## Gate B: Protocol → Full Search

Pass only if:

- search sources are named,
- exact queries exist,
- known studies were used to pilot the query,
- IC/EC are operational,
- QA/RoB is defined,
- extraction fields exist,
- synthesis plan exists.

## Gate C: Search → Screening

Pass only if:

- search date/query/result count are saved for every source,
- records are exported,
- deduplication method is documented.

## Gate D: Screening → Extraction

Pass only if:

- full-text exclusion reasons are recorded,
- included set is finalized,
- multiple reports of one study are linked.

## Gate E: Extraction → Synthesis

Pass only if:

- extraction form is complete,
- every RQ has sufficient data or is explicitly reported as under-evidenced,
- QA/RoB is complete,
- obvious extraction conflicts are resolved.

## Gate F: Synthesis → Submission

Pass only if:

- every major conclusion is supported by included studies,
- conflicting evidence is not hidden,
- limitations are discussed,
- flow counts reconcile,
- search strategy is reproducible,
- no citation is fabricated or unverified.

---

# 18. Common Mistakes to Flag

Immediately warn the user when any of these occur.

## Methodological mistakes

- Starting the search before defining RQs.
- Changing the RQ to fit whatever papers were found without documenting the change.
- Calling a normal narrative review an SLR because it used Google Scholar.
- Using one unexplained search string in one source and claiming completeness.
- Creating search strings solely by mechanically joining all PICOC elements.
- Including/excluding studies based on whether their conclusions agree with expectations.
- Using journal quartile/impact factor as the only measure of study quality.
- Mixing inclusion/exclusion criteria with QA criteria.
- Inventing a QA threshold after seeing paper scores.
- Treating all conference/journal versions as separate independent studies.
- Performing meta-analysis merely because numeric values exist.
- Listing papers individually instead of synthesizing evidence.
- Failing to record full-text exclusion reasons.
- Reporting only included papers and hiding the screening funnel.

## AI-specific mistakes

- Generating nonexistent DOI/citations.
- Classifying a paper from title only when full text is required.
- Extracting a result without locating it in the paper.
- Claiming two-reviewer agreement when AI acted as one reviewer without disclosure.
- Letting AI rewrite authors' claims into stronger causal claims.

---

# 19. How the AI Assistant Should Help

When this skill is active, follow this operating procedure.

## If the user gives only a topic

Produce:

1. Topic assessment: SLR vs mapping study.
2. Suggested scope.
3. 2–4 candidate RQs.
4. PICOC where useful.
5. Candidate search-concept blocks.
6. Candidate IC/EC.
7. Candidate QA/RoB questions.
8. Candidate extraction fields.
9. Likely synthesis approach.
10. Key methodological risks.

Do not immediately generate a huge final search string without first checking whether the scope and RQs make sense.

## If the user gives an RQ

Check:

- Is it answerable?
- Is it too broad/narrow?
- What data would answer it?
- Which study designs could answer it?
- Does it imply comparison/effectiveness or qualitative synthesis?

Then refine it only when necessary.

## If the user gives a search string

Review it for:

- concept coverage,
- synonyms,
- acronym ambiguity,
- restrictive terms,
- missing historical terminology,
- Boolean logic,
- database-specific syntax,
- whether known studies are retrieved.

Do not rate a search string only by how many results it returns.

## If the user provides candidate papers

For each paper, separately assess:

1. duplicate status,
2. eligibility based on IC/EC,
3. reason for inclusion/exclusion,
4. QA/RoB if eligible,
5. extraction data,
6. which RQ(s) it informs.

Never infer unseen evidence.

## If the user asks for QA scoring

Return a table with:

```text
Study | QA1 | QA2 | ... | Score | % | Decision | Evidence/Rationale
```

Every nontrivial score should have a short evidence-based rationale.

## If the user asks for synthesis

Synthesize by RQ/theme, not paper-by-paper.

Use wording such as:

- "Across N studies..."
- "The evidence consistently indicates..."
- "Findings were mixed..."
- "This pattern appeared primarily in..."
- "Evidence is limited because..."

Avoid causal language unless the underlying study designs support causality.

---

# 20. Quick Protocol Template

Copy and fill this before conducting the full review.

```markdown
# SLR Protocol

## 1. Title

## 2. Background

## 3. Objective

## 4. Research Questions
- RQ1:
- RQ2:
- RQ3:

## 5. PICOC
- Population:
- Intervention:
- Comparison:
- Outcome:
- Context:

## 6. Search Strategy
### Sources
- Scopus
- IEEE Xplore
- ACM Digital Library
- ...

### Search concepts
- Concept A:
- Concept B:
- Concept C:

### Exact search strings
#### Scopus
...

#### IEEE Xplore
...

#### ACM DL
...

### Search dates
...

### Known studies / validation set
...

### Snowballing strategy
...

## 7. Inclusion Criteria
- IC1:
- IC2:

## 8. Exclusion Criteria
- EC1:
- EC2:

## 9. Selection Process
- Deduplication:
- Title/abstract screening:
- Full-text screening:
- Reviewer procedure:
- Disagreement procedure:

## 10. Quality Assessment / Risk of Bias
- QA1:
- QA2:
- Scoring:
- Threshold (if required):

## 11. Data Extraction
| Field | Definition | Related RQ |
|---|---|---|
| ... | ... | ... |

## 12. Synthesis Plan
- RQ1:
- RQ2:
- RQ3:

## 13. Tools

## 14. Limitations anticipated

## 15. Protocol change log
| Date | Change | Reason | Possible impact |
|---|---|---|---|
```

---

# 21. Final Pre-Submission Checklist

Answer **yes** to as many as legitimately applicable.

## Planning

- [ ] Need for the SLR is justified.
- [ ] RQs are explicit.
- [ ] Scope is realistic.
- [ ] Protocol existed before full conduct.
- [ ] Search was piloted.
- [ ] Eligibility criteria were piloted.
- [ ] QA/RoB was piloted.
- [ ] Extraction form was piloted.

## Search

- [ ] Multiple appropriate sources were searched or a justified snowballing strategy was used.
- [ ] Exact query for every source is preserved.
- [ ] Search dates are recorded.
- [ ] Search result counts are recorded.
- [ ] Known relevant studies were used to assess search coverage.
- [ ] Snowballing was considered.
- [ ] Duplicate handling is documented.

## Selection

- [ ] IC/EC are explicit.
- [ ] Title/abstract and full-text stages are distinguishable.
- [ ] Full-text exclusion reasons are recorded.
- [ ] Reviewer reliability was addressed honestly.
- [ ] Multiple reports of the same study are linked.

## QA / RoB

- [ ] QA is separate from eligibility.
- [ ] Criteria fit the included study designs.
- [ ] Scoring rule existed before scoring all studies.
- [ ] Threshold, if any, is justified.
- [ ] Assessments have rationales.

## Extraction and synthesis

- [ ] Extraction fields map to RQs.
- [ ] Important extracted values are traceable to source locations.
- [ ] Synthesis is across studies, not a sequence of paper summaries.
- [ ] Contradictory evidence is represented.
- [ ] Meta-analysis is used only if justified.
- [ ] Study quality/risk is reflected in conclusions.

## Reporting

- [ ] Flow counts reconcile.
- [ ] PRISMA-style flow is included where appropriate.
- [ ] SEGRESS reporting principles are considered for SE/CS work.
- [ ] Protocol deviations are reported.
- [ ] Review-process limitations are discussed.
- [ ] Evidence-base limitations are discussed.
- [ ] Every citation has been verified.
- [ ] Supplementary search/extraction data are preserved when possible.

---

# 22. References / Methodological Basis

Use these as starting points when a formal methodology citation is needed.

1. Kitchenham, B., & Charters, S. (2007). *Guidelines for performing Systematic Literature Reviews in Software Engineering*. EBSE Technical Report EBSE-2007-01.

2. Kitchenham, B., Brereton, O. P., & Budgen, D. (2013). *A systematic review of systematic review process research in software engineering*. Information and Software Technology, 55(12), 2049–2075. https://doi.org/10.1016/j.infsof.2013.07.010

3. Zhang, H., Babar, M. A., & Tell, P. (2011). *Identifying relevant studies in software engineering*. Information and Software Technology, 53(6), 625–637. https://doi.org/10.1016/j.infsof.2010.12.010

4. Wohlin, C. (2014). *Guidelines for snowballing in systematic literature studies and a replication in software engineering*. EASE 2014. https://doi.org/10.1145/2601248.2601268

5. Kitchenham, B., Madeyski, L., & Budgen, D. (2023). *SEGRESS: Software Engineering Guidelines for REporting Secondary Studies*. IEEE Transactions on Software Engineering, 49(3), 1273–1298. https://doi.org/10.1109/TSE.2022.3174092

6. Page, M. J., et al. (2021). *The PRISMA 2020 statement: an updated guideline for reporting systematic reviews*. BMJ, 372:n71. https://doi.org/10.1136/bmj.n71

7. Zhou, Y., Zhang, H., Huang, X., Yang, S., Babar, M. A., & Tang, H. (2021). *Quality Assessment in Systematic Literature Reviews: A Software Engineering Perspective*. Information and Software Technology, 130, 106397. https://doi.org/10.1016/j.infsof.2020.106397

8. Evidence-Based Software Engineering (EBSE), Durham University. Current systematic review guidance, planning/conduct/reporting resources and templates: https://ebse.webspace.durham.ac.uk/

9. PRISMA 2020 official resources: https://www.prisma-statement.org/prisma-2020

---

# 23. One-Sentence Rule

> A defensible SLR is one where another researcher can understand **why each study was found, why it was included, how its evidence was judged and extracted, and how that evidence produced each final conclusion**.
