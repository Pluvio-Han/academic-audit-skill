# Academic Audit Skill

`academic-audit` is a Codex skill for auditing the academic rigor of manuscripts, with a strong focus on competition papers, statistical modeling reports, data mining papers, research reports, theses, and ordinary academic drafts.

It is designed as an audit tool, not a ghostwriting tool. It helps an agent find high-impact issues in logic, methods, evidence, citations, reproducibility, language, formatting, and final submission readiness.

## What It Does

- Audits competition papers with judge-facing score impact in mind.
- Checks claim-evidence alignment and highlights unsupported conclusions.
- Reviews methodology, variables, models, statistics, experiments, and reproducibility.
- Flags citation and reference integrity risks.
- Reviews Chinese, English, and mixed-language academic style.
- Checks LaTeX/DOCX/PDF formatting and submission-readiness risks.
- Supports revision audits with fixed/partial/unresolved/regressed/new issue tracking.

## Best Use Cases

- Statistical modeling competition papers
- Mathematical modeling papers such as MCM/ICM-style reports
- Data mining or ML competition papers
- Course research reports
- Empirical economics, management, policy, or social science papers
- Thesis or dissertation drafts
- Literature reviews and ordinary academic manuscripts

## Installation

Copy the skill folder into your Codex skills directory:

```bash
mkdir -p ~/.codex/skills
cp -R academic-audit ~/.codex/skills/academic-audit
```

Then start a new Codex session or reload skills if your client supports it.

## Basic Usage

For a complete competition paper:

```text
Use $academic-audit to audit this complete competition paper in competition-audit mode.
Focus on task fit, model credibility, data processing, result interpretation, reproducibility, academic style, formatting, and final submission risk.
If the competition type is unclear, infer it and state your assumption.
```

For a Chinese statistical modeling paper:

```text
使用 $academic-audit 对这篇统计建模比赛论文做 competition-audit。
重点检查模型设定、变量定义、数据处理、稳健性、图表公式、中文学术表达、排版规范和最终提交风险。
如果材料不足，请做 scoped audit，并在 Verification Limits 中说明无法验证的部分。
```

For a revised manuscript:

```text
Use $academic-audit in revision-audit mode.
Here is the previous audit report: [paste report]
Here is the revised manuscript: [paste or provide file path]
Classify each prior issue as Fixed, Partially fixed, Unresolved, Regressed, or New issue.
```

## Audit Modes

- `triage`: quick review for outlines or short drafts
- `full-audit`: complete academic audit
- `competition-audit`: contest-paper audit mapped to scoring risk
- `citation-audit`: reference and citation integrity
- `logic-audit`: claim-evidence and argument coherence
- `method-audit`: method, model, experiment, statistics, and reproducibility
- `language-audit`: scholarly style, clarity, Chinese/English consistency
- `format-audit`: LaTeX/DOCX/PDF/template/submission compliance
- `revision-audit`: regression check after manuscript revisions

## Repository Structure

```text
academic-audit/
├── SKILL.md
├── agents/
│   └── openai.yaml
├── references/
│   ├── audit_dimensions.md
│   ├── citation_integrity.md
│   ├── competition_papers.md
│   ├── discipline_overrides.md
│   ├── format_submission.md
│   ├── language_style.md
│   ├── method_rigor.md
│   └── revision_protocol.md
└── templates/
    ├── audit_report.md
    └── claim_evidence_matrix.md
```

## Example Output Sections

The skill asks the agent to produce an `Academic Audit Report` with:

- Overall Verdict
- Highest-Risk Findings
- Dimension Scorecard
- Claim-Evidence Matrix
- Detailed Findings
- Revision Roadmap
- Verification Limits
- Submission Readiness Checklist

## Design Principles

- Findings should be evidence-bound: major findings need file/page/section location and a concrete rationale.
- Competition audits should prioritize score impact, not only journal-style standards.
- Missing information should be reported as a verification limit, not guessed.
- The skill should preserve disciplinary conventions instead of forcing all fields into one rubric.

## License

MIT License. See [LICENSE](LICENSE).
