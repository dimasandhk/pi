# Cross-study synthesis workflow

## Step 1: Normalize extraction
For each *independent empirical study*, record:
`ID, report IDs, task, participant population, intervention, comparator, outcome construct, actual measurement, design, n, effects/statistics, limitations, exact source location`.
The review paper is a secondary source, not a primary empirical study.

## Step 2: Identify grouping schema BEFORE summarizing results
For code comprehension:
- **Direct comprehension:** explanation accuracy, code-logic questions, code behavior quiz, appropriately designed debugging/modification performance when explicitly validated as comprehension.
- **Close proxies:** cognitive load, knowledge retention, perceived understanding, developers' confidence, self-reported sense-making; distinguish rather than automatically collapse.
- **Other outcomes:** completion time, productivity and code quality *not evidence of comprehension alone*.
- Key contexts: professional vs advanced students; existing vs generated code; maintenance/debugging/review/feature development; inline vs chat/visual scaffolding/agents.

## Step 3: Extract competing evidence
For each claim:
`supports | contradicts | unclear | not measured`.
Never infer 'no effect' from missing significance without confidence interval/design considerations.

## Step 4: Build RQ-specific matrices
- **RQ1:** study × comparator × outcome × direction × measure validity × design × n.
- **RQ2:** tool × model × assistance form × contexts, preserving unknown version.
- **RQ3:** outcome instrument × direct/proxy classification × sample/developer experience × task realism.
- **RQ4:** verbatim supporting excerpt/author paraphrase × barrier × mechanism × consequence × study ID.
Use the team's coding taxonomy and log its development, not an unreviewed model-generated taxonomy.

## Step 5: Synthesize, don't catalogue
Each paragraph follows:
1. Position a bounded cross-study claim.
2. Name key contributing studies and concrete study results.
3. Present exceptions/discordant evidence.
4. Discuss measure/context/design differences explaining the tension where supported.
5. State what the evidence can and cannot conclude.

Illustrative *structure only*, not factual claims:
'In [k] studies of [population and task], [outcome as operationalized] was [direction]. [Studies Pxx and Pyy] used [direct instrument] and observed [source-backed numeric/statistical result], whereas [Pzz] reported [contrasting result]. Because [source-backed design/context limitation], these findings support [bounded interpretation], not [broader causal assertion].'

## Step 6: Report certainty and robustness honestly
- 'More papers say X' does not establish the magnitude or truth of X. Never simply count significant p values to claim consensus.
- If grouping by direction of effect, distinguish descriptive tabulation from a formal effect synthesis. Only invoke SWiM for quantitative intervention-effect synthesis, reporting its requirements.
- Consider sensitivity of conclusions to weak measures, small samples, limited realism and preliminary QA.
- If a certainty rubric is not actually applied, describe limitations of confidence rather than invent 'high/moderate/low' formal ratings.

## Step 7: Evidence trace
Keep an explicit mapping:
`manuscript claim -> extraction row -> primary paper ID -> section/page/table -> exact measure/result -> verification status`.
Every figure cell should be auditable to one or more source rows.
