# Claim-Evidence Matrix

| ID | Claim | Location | Evidence Type | Evidence Provided | Adequacy | Risk | Required Fix |
|---|---|---|---|---|---|---|---|
| C1 |  |  | Data / Citation / Proof / Experiment / Theory |  | Strong / Partial / Weak / Missing |  |  |

## Claim Identification Guide

Audit these statement types as claims requiring evidence:

- **Contribution claims**: "This paper proposes", "introduces", "is the first to", "improves".
- **Performance claims**: "Our model achieves X", "outperforms baseline by Y", "reduces error".
- **Causal claims**: "X causes", "leads to", "results in", "improves because".
- **Generalization claims**: "works for all", "is robust across", "can be widely applied".
- **Factual background claims**: statistics, prevalence figures, market facts, policy facts, dataset facts.
- **Method validity claims**: "the model is reliable", "the assumptions are reasonable", "the metric is appropriate".

Do not over-audit explicitly scoped observations, acknowledged limitations, or clearly marked hypotheses as if they were proven conclusions. If a claim is too vague to evaluate, mark it as `Weak` and require clarification.

## Evidence Type Guide

- Data: manuscript's own dataset, table, figure, or measurement.
- Citation: external scholarly source.
- Proof: formal derivation, theorem, or logical demonstration.
- Experiment: controlled test, ablation, benchmark, simulation.
- Theory: accepted conceptual framework or model.
