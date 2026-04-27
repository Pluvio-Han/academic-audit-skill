# Language and Scholarly Style

## Audit Passes

Use the shared `BLOCKER` / `MAJOR` / `MINOR` / `STYLE` severity system from `SKILL.md`.

1. **Clarity**: Is the sentence easy to parse? Is the subject close to the verb?
2. **Precision**: Are terms defined and used consistently?
3. **Concision**: Can empty phrases be removed without loss?
4. **Hedging**: Are claims calibrated to evidence?
5. **Flow**: Does each paragraph have one main idea and a clear transition?
6. **Register**: Does tone match the discipline and venue?

## Common Fixes

Replace:
- "It is important to note that X" -> "X"
- "Due to the fact that" -> "Because"
- "In order to" -> "To"
- "A number of" -> "Several" or the exact number
- "Conduct an analysis of" -> "Analyze"
- "Provide an explanation of" -> "Explain"

Flag but do not automatically change:
- Passive voice in methods where field style expects it.
- Repeated technical terms; consistency is often better than synonym variation.
- Long sentences that are syntactically clear and necessary.

## AI-Like Style Signals

Flag patterns that reduce scholarly credibility:
- Generic intensifiers: crucial, significant, robust, comprehensive, transformative without evidence.
- Formulaic transitions repeated across paragraphs.
- Uniform paragraph length and sentence rhythm.
- Overbroad opening claims about modern society, rapid development, or increasing importance.
- Claims that sound polished but carry no measurable content.

For non-native English writers, distinguish AI-like generic prose from normal ESL patterns before flagging. Treat these issues as `STYLE` unless the pattern is pervasive enough to undermine scholarly credibility or obscure meaning.

## Chinese and Mixed-Language Style

For Chinese academic writing:

- Flag slogan-like claims, policy-style exaggeration, and unsupported grand narratives.
- Prefer precise subject-verb-object sentences over long chains of abstract nouns.
- Check that Chinese translations of technical terms remain consistent.
- Avoid unnecessary English terms when a standard Chinese academic term exists; retain English for proper nouns, model names, datasets, and field-standard abbreviations.
- In mixed manuscripts, verify that acronyms are defined at first use in both abstract and main text when required.

## Output Add-on

For language audits, include examples:

```markdown
| Location | Issue | Original | Suggested Revision | Rationale |
|---|---|---|---|---|
```
