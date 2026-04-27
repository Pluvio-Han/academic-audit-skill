# Audit Dimensions

Use the shared `BLOCKER` / `MAJOR` / `MINOR` / `STYLE` severity system defined in `SKILL.md`.

## 1. Research Framing and Contribution

Check whether the work states a precise problem, explains why it matters, identifies a real gap, and claims contributions that the paper actually supports.

Red flags:
- Contribution is generic, inflated, or indistinguishable from standard practice.
- Introduction jumps from broad motivation to method without defining the gap.
- Research question, hypothesis, or thesis is absent.
- Claimed novelty is not positioned against close prior work.

Score guide:
- 5: Clear problem-gap-contribution chain; claims are precise and well-positioned.
- 3: Understandable framing but gap or contribution is underspecified.
- 1: No credible contribution logic.

## 2. Logic and Argument Coherence

Check paragraph flow, section ordering, claim hierarchy, counterarguments, and whether conclusions follow from evidence.

Red flags:
- Conclusions exceed results.
- Key terms shift meaning across sections.
- Claims appear before definitions or evidence.
- Related work is a list rather than a synthesis.
- Limitations contradict the main claim.

## 3. Evidence and Citation Integrity

Check that all nontrivial claims are supported by appropriate evidence and that citations are real, relevant, current where needed, and correctly formatted.

Red flags:
- Fabricated or unverifiable references.
- Citation does not support the sentence it is attached to.
- Heavy reliance on secondary sources for empirical facts.
- Missing citations for benchmark methods, datasets, metrics, theories, or factual claims.
- In-text citations and bibliography do not match.

## 4. Methodological Rigor

Judge methods relative to discipline. For empirical work, check design, dataset, variables, controls, baselines, metrics, statistical tests, ablations, and threats to validity. For theoretical work, check assumptions, definitions, lemmas, proofs, and scope conditions. For humanities work, check corpus, interpretive method, primary sources, and alternative readings.

Red flags:
- Method cannot answer the stated research question.
- Dataset/sample is insufficient or biased without discussion.
- Baselines are weak or unfair.
- Statistical claims omit uncertainty, effect size, or test rationale where required.
- Proof depends on unstated assumptions.

## 5. Results, Figures, Tables, and Numerical Consistency

Check whether results are reported accurately and whether visual elements are self-contained.

Red flags:
- Abstract, body, tables, and figures report inconsistent numbers.
- Captions do not state what is measured, on what data, and why it matters.
- Axes, units, sample sizes, error bars, or statistical notation are missing.
- Tables contain excessive precision or hide important comparisons.
- Best results are bolded inconsistently.

## 6. Reproducibility and Transparency

Check whether another qualified researcher could reproduce or evaluate the work.

Red flags:
- Missing data source, preprocessing, hyperparameters, implementation details, prompts, annotation protocol, or code availability statement.
- Random seeds, train/test splits, hardware, package versions, or compute budget omitted when relevant.
- Human-subjects, privacy, or sensitive-data handling not disclosed.

## 7. Language and Scholarly Style

Check clarity, precision, tone, terminology, paragraph structure, hedging, and concision.

Red flags:
- Inflated claims: proves, guarantees, revolutionary, unprecedented without evidence.
- Empty openers: it is important to note, in this paper we will discuss.
- AI-like overuse of generic phrases: delve into, crucial, robust framework, comprehensive exploration.
- Heavy nominalization where active verbs would be clearer.
- Unexplained acronyms or inconsistent terminology.

## 8. Formatting and Submission Compliance

Check target style before general preference. If no target is provided, use common international academic standards.

Red flags:
- Template violations, wrong citation style, broken cross-references, inconsistent heading levels.
- Figures/tables not referenced in text.
- Missing abstract, keywords, limitations, ethics, data availability, funding, conflict of interest, author contributions, or AI disclosure when required.
- Bibliography style inconsistent with target venue.
