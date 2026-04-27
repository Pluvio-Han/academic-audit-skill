# Competition Paper Audit

Use for data mining, mathematical modeling, innovation contests, research competitions, and rubric-based papers.

## Competition Type Profiles

When competition type is not specified, infer it from manuscript content and state the assumed type. If the official rubric is unavailable, use the profile below as default priority weighting and say: "Auditing against inferred competition type: [type]. Provide the official rubric for a more precise audit."

| Type | Examples | Highest-Weight Audit Areas |
|---|---|---|
| Mathematical modeling | MCM/ICM, 全国大学生数学建模竞赛 | Model assumptions, variable definitions, dimensional consistency, sensitivity analysis, result interpretation |
| Data mining / ML | KDD Cup, DataFountain, Kaggle-style competitions, 数据挖掘竞赛 | Data leakage, metric alignment, reproducibility, validation split, feature engineering transparency |
| Management / business | Business analytics cases, management decision competitions | Practical feasibility, stakeholder logic, recommendation clarity, cost-benefit reasoning |
| General STEM innovation | 挑战杯, 互联网+, research innovation contests | Research framing, novelty, evidence quality, implementation credibility, presentation clarity |

## Competition-Specific Priorities

1. Answer the problem statement exactly.
2. Make the scoring objective or judging rubric explicit.
3. Connect every method choice to the competition goal.
4. Show reproducible data processing and model construction.
5. Present results in judge-friendly tables and figures.
6. Explain why the solution is reliable under realistic constraints.
7. Avoid overclaiming beyond the competition data.

## Audit Dimensions

| Dimension | Questions |
|---|---|
| Problem fit | Does the paper answer every required task? |
| Model validity | Are assumptions, variables, and constraints justified? |
| Data handling | Are sources, cleaning, feature engineering, and leakage risks clear? |
| Evaluation | Are metrics aligned with the competition objective? |
| Comparison | Are baselines or alternatives included? |
| Robustness | Are sensitivity, ablation, or scenario tests present? |
| Communication | Can judges understand the contribution quickly? |
| Reproducibility | Could another team reproduce the result? |

## Common High-Risk Issues

- The paper optimizes a proxy that does not match the scoring rule.
- The method is complex but not justified.
- Data cleaning changes the task population without disclosure.
- Charts look impressive but do not answer the judging question.
- Sensitivity analysis is missing for arbitrary weights or parameters.
- Abstract and conclusion claim general impact unsupported by the competition setting.

## Time-Pressure Handling

Competition manuscripts are often produced under 72-96 hour constraints. Do not lower academic standards, but distinguish:

- **Must fix before submission**: wrong task answer, data leakage, inconsistent results, broken formulas, missing required section, unreadable figures.
- **Known risk if time-limited**: limited ablation, shallow related work, incomplete sensitivity analysis, weaker formatting polish.
- **Post-submission learning item**: improvements that would require new data, major reimplementation, or a redesigned study.

When time is limited, rank fixes by expected score impact.

## Code and Appendix Checks

For competitions that require code, supplement, or appendix:

- Code or pseudocode must reproduce the reported pipeline at a high level.
- Data preprocessing steps must match the manuscript.
- Random seeds, split strategy, and metric calculation must be documented when relevant.
- Appendix should support, not replace, the main argument.
- Required files named in the competition instructions must be present.

## Recommended Verdict Labels

- `Score-ready`: likely clear and complete for judging.
- `Competitive but risky`: good core idea with fixable weaknesses.
- `Methodologically fragile`: result may not survive scrutiny.
- `Not judge-ready`: does not clearly answer the task or lacks evidence.
