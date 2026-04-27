# Discipline Overrides

Use these emphases to avoid forcing one field's norms onto another.

## Computer Science / AI / Data Mining

Prioritize:
- Clear task definition, datasets, metrics, baselines, ablations, error analysis, reproducibility.
- Fair comparison with current or standard methods.
- Data leakage, train/test split, hyperparameter tuning, random seed, compute budget.
- Statistical or repeated-run evidence when variance matters.
- Code/data availability and exact preprocessing.

Common blockers:
- Baselines are missing or outdated.
- Results use a private split without justification.
- The method description cannot be implemented.
- Claims of state of the art are not verified against current leaderboards or papers.

## Mathematical Modeling / Operations Research

Prioritize:
- Assumptions, variables, constraints, objective functions, solution method, sensitivity analysis.
- Dimensional consistency and interpretation of parameters.
- Feasibility, optimality, robustness, and validation against data or scenarios.

Common blockers:
- Model assumptions are hidden or unrealistic.
- Constraints do not match the problem statement.
- Sensitivity analysis is absent for key parameters.

## Economics / Finance / Management

Prioritize:
- Identification strategy, endogeneity, omitted variables, robustness checks, sample construction.
- Data provenance, variable definitions, model specification, standard errors.
- Economic significance, not only statistical significance.

Common blockers:
- Causal language without identification.
- No robustness checks for core result.
- Variable construction is ambiguous.

## Biomedical / Public Health

Prioritize:
- Study design, population, inclusion/exclusion criteria, ethics approval, consent, outcomes, confounders.
- Reporting guidelines such as CONSORT, STROBE, PRISMA, STARD when applicable.
- Effect sizes, confidence intervals, adverse events, limitations.

Common blockers:
- Missing ethics or consent statement.
- Unsupported clinical recommendation.
- Systematic review lacks transparent search and screening.

## Social Sciences / Education

Prioritize:
- Theoretical framework, construct validity, sampling, measurement reliability, coding protocol.
- Reflexivity and positionality where relevant.
- Quantitative/qualitative method fit.

Common blockers:
- Constructs are undefined or poorly operationalized.
- Claims exceed sample or context.
- Qualitative coding lacks reliability or audit trail.

## Humanities

Prioritize:
- Thesis clarity, textual evidence, historiography or scholarly context, interpretive logic.
- Primary-source handling, translation choices, conceptual precision.
- Alternative interpretations and scope conditions.

Common blockers:
- Evidence is quoted but not interpreted.
- Argument is descriptive rather than analytical.
- Secondary literature is absent or only decorative.

## Law / Policy

Prioritize:
- Jurisdiction, legal authority, doctrinal accuracy, policy tradeoffs, evidentiary basis.
- Distinguish law as it is from normative proposal.
- Currentness of statutes, cases, regulations, and policy documents.

Common blockers:
- Outdated legal rule.
- Confuses jurisdictions.
- Normative recommendation lacks feasibility analysis.
