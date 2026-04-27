# Academic Audit Skill

`academic-audit` 是一个用于 Codex 的学术审计 skill，目标是让 agent 像审稿人、竞赛评委和方法学审计员一样检查论文，而不是直接代写论文。

它特别适合审计比赛论文、统计建模论文、数学建模论文、数据挖掘/机器学习竞赛论文、课程研究报告、学位论文草稿和普通学术论文。审计重点包括：问题匹配度、逻辑链、方法严谨性、变量与数据可复现性、引用真实性、语言风格、排版规范和最终提交风险。

## 核心定位

这个 skill 不是论文写作工具，而是论文质量审计工具。

它会帮助 agent：

- 找出会影响比赛得分或投稿质量的高风险问题。
- 检查论文主张是否有足够证据支撑。
- 审计模型、变量、统计方法、实验设计和复现性。
- 检查引用、参考文献和文献支撑是否可靠。
- 审查中文、英文和中英混合学术表达。
- 检查 LaTeX、DOCX、PDF 的格式和提交风险。
- 支持修改后的回归审计，追踪问题是否真正修复。

## 适用场景

- 统计建模比赛论文
- 数学建模论文，例如 MCM/ICM 或全国大学生数学建模竞赛
- 数据挖掘、机器学习、Kaggle/DataFountain 类竞赛论文
- 课程论文和研究报告
- 经济、管理、政策、社会科学等实证论文
- 学位论文或毕业论文草稿
- 文献综述和普通学术论文

## 安装方法

把 `academic-audit/` 文件夹复制到 Codex 的 skills 目录：

```bash
mkdir -p ~/.codex/skills
cp -R academic-audit ~/.codex/skills/academic-audit
```

然后重启 Codex 会话，或在客户端中重新加载 skills。

## 基础用法

审计一篇完整比赛论文：

```text
使用 $academic-audit 对这篇完整比赛论文做 competition-audit。
重点检查：问题匹配度、模型可信度、数据处理、结果解释、复现性、学术表达、排版规范和最终提交风险。
如果无法确认比赛类型，请说明你的假设。
```

审计一篇中文统计建模论文：

```text
使用 $academic-audit 对这篇统计建模比赛论文做 competition-audit。
重点检查模型设定、变量定义、数据处理、稳健性、图表公式、中文学术表达、排版规范和最终提交风险。
如果材料不足，请做 scoped audit，并在 Verification Limits 中说明无法验证的部分。
```

审计修改后的论文：

```text
使用 $academic-audit 做 revision-audit。
这是上一轮审计报告：[粘贴报告]
这是修改后的论文：[粘贴内容或提供文件路径]
请逐条判断 Fixed / Partially fixed / Unresolved / Regressed / New issue。
```

## 审计模式

- `triage`：快速审计，适合 outline、半成稿或短材料。
- `full-audit`：完整学术审计。
- `competition-audit`：比赛论文审计，重点映射到评委打分风险。
- `citation-audit`：引用真实性、参考文献和文献支撑审计。
- `logic-audit`：论证结构和 claim-evidence 审计。
- `method-audit`：模型、方法、实验、统计和复现性审计。
- `language-audit`：学术表达、中文/英文/中英混合语言审计。
- `format-audit`：LaTeX、DOCX、PDF、模板和提交规范审计。
- `revision-audit`：修改后回归审计，追踪问题是否修复。

## 推荐工作流

完整比赛论文可以按这个顺序使用：

1. 初稿完成后：`competition-audit`
2. 根据报告修改论文。
3. 修改后：`revision-audit`
4. 提交前：`format-audit`
5. 如果需要核查参考文献：单独做 `citation-audit`

## 仓库结构

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

## 文件说明

- `academic-audit/SKILL.md`：核心触发说明、工作流、审计模式、严重性分级和输出规范。
- `academic-audit/references/audit_dimensions.md`：通用八维审计标准。
- `academic-audit/references/discipline_overrides.md`：不同学科的审计重点和常见阻断问题。
- `academic-audit/references/competition_papers.md`：比赛论文评分逻辑、竞赛类型、时间压力和附录/代码检查。
- `academic-audit/references/citation_integrity.md`：引用、来源质量、参考文献和文献支撑审计。
- `academic-audit/references/method_rigor.md`：方法、统计、机器学习、质性研究、理论研究和复现性检查。
- `academic-audit/references/language_style.md`：英文、中文和中英混合学术表达审计。
- `academic-audit/references/format_submission.md`：LaTeX/DOCX/PDF 格式、必要声明和中文比赛排版检查。
- `academic-audit/references/revision_protocol.md`：修改后回归审计流程和状态定义。
- `academic-audit/templates/audit_report.md`：完整审计报告模板。
- `academic-audit/templates/claim_evidence_matrix.md`：主张-证据矩阵模板和主张识别规则。
- `academic-audit/agents/openai.yaml`：UI 元数据和默认调用提示。

## 输出结构

默认完整审计报告包含：

- Overall Verdict
- Highest-Risk Findings
- Dimension Scorecard
- Claim-Evidence Matrix
- Detailed Findings
- Revision Roadmap
- Verification Limits
- Submission Readiness Checklist

## 设计原则

- 高风险问题必须有证据定位，例如文件、页码、章节、原文摘录或转述。
- 比赛论文优先关注评委打分影响，而不是机械套用期刊论文标准。
- 缺失材料要写入 Verification Limits，不要臆测。
- 不同学科有不同规范，不能用同一套方法强行审计所有论文。
- 只在用户明确要求时进行修改或重写；默认行为是审计和给出修改路线图。

## License

MIT License. See [LICENSE](LICENSE).
