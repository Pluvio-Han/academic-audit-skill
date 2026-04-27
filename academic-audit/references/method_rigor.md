# Method Rigor

Use the shared `BLOCKER` / `MAJOR` / `MINOR` / `STYLE` severity system defined in `SKILL.md`.

## Universal Method Questions

- Does the method answer the research question?
- Are assumptions stated and justified?
- Are inputs, procedures, and outputs clear enough to reproduce?
- Are comparison standards fair?
- Are limitations and threats to validity acknowledged?
- Does the evidence support the scope of the conclusion?

## Empirical Quantitative Work

Check:
- Sample/dataset construction.
- Inclusion and exclusion criteria.
- Variable definitions and measurement validity.
- Missing data handling.
- Statistical test choice and assumptions.
- Effect sizes and confidence intervals where appropriate.
- Multiple comparison handling where relevant.
- Robustness checks and sensitivity analysis.

## Machine Learning / Data Science

Check:
- Dataset provenance, licensing, preprocessing, split protocol.
- Leakage risks, duplicate records, temporal leakage.
- Baseline choice, hyperparameter search fairness, compute budget.
- Metrics aligned with task and costs.
- Ablation studies isolate claimed components.
- Error analysis explains failure modes.
- Repeated runs or uncertainty where stochasticity matters.

## Qualitative Work

Check:
- Corpus/sample selection.
- Coding scheme, inter-coder reliability or reflexive justification.
- Saturation or stopping rationale.
- Audit trail from raw evidence to themes.
- Alternative interpretations.

## Theoretical / Formal Work

Check:
- Definitions, assumptions, theorem statements, proof completeness.
- Boundary cases and counterexamples.
- Relationship between formal result and real-world interpretation.
- Notation consistency.

## Reproducibility Minimums

When relevant, expect:
- Data source and version.
- Code or algorithm details.
- Environment, package versions, hardware.
- Random seeds and split files.
- Parameter settings and prompt templates.
- Evaluation scripts or exact metric formula.
