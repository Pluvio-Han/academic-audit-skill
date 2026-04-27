# Citation Integrity

Use the shared `BLOCKER` / `MAJOR` / `MINOR` / `STYLE` severity system defined in `SKILL.md`.

## Source Quality Tiers

- Tier 1: Peer-reviewed journal articles, top conference proceedings, academic books, standards, official datasets, laws/regulations, authoritative technical reports.
- Tier 2: Preprints, working papers, dissertations, institutional reports, government reports.
- Tier 3: News, blogs, documentation, Wikipedia, personal sites. Use only when the claim concerns current events, software behavior, public communication, or nonacademic context.

## Checks

1. In-text citations match bibliography entries.
2. Bibliography entries match real works.
3. DOI, URL, title, author, venue, and year are plausible and verified when possible.
4. Citation placement supports the specific sentence, not just the paragraph topic.
5. Seminal works are included when necessary.
6. Recent literature is included when the field moves quickly.
7. Review articles are not used as primary evidence for precise empirical claims unless clearly stated.
8. Direct quotes include page numbers or exact source location.
9. Citation style follows target format.

## Severity

`BLOCKER`:
- Fabricated reference.
- Citation supports a different claim.
- Core empirical/theoretical claim has no source or evidence.

`MAJOR`:
- Missing key prior work.
- Overreliance on weak sources.
- Citation format is systematically wrong.

`MINOR`:
- Incomplete page range, inconsistent capitalization, missing access date when style requires it.

## Output Add-on

For citation audits, include:

```markdown
### Citation Integrity Table
| Citation | Status | Supports Claim? | Problem | Fix |
|---|---|---|---|---|

### Orphan References
[References listed but never cited.]

### Missing References
[Citations in text missing from bibliography.]
```
