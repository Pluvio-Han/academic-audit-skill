# Revision Audit Protocol

Use for `revision-audit` when the user provides a revised manuscript, prior audit report, reviewer comments, or a list of intended fixes.

## Inputs

Prefer at least two of:

- Previous audit report or issue list.
- Revised manuscript.
- Original manuscript or diff.
- Author response explaining changes.
- Target venue or competition rubric.

If only the revised manuscript is available, run a scoped audit and state that regression against prior findings could not be verified.

## Procedure

1. Reconstruct the prior issue list and assign stable issue IDs if missing.
2. For each prior issue, inspect the revised manuscript and classify current status.
3. Check whether the fix created new problems, contradictions, formatting regressions, or unsupported claims.
4. Re-run only the relevant dimension checks unless the user asks for a full re-audit.
5. End with a short go/no-go recommendation.

## Status Values

| Status | Meaning |
|---|---|
| `Fixed` | The issue is resolved without creating a new problem |
| `Partially fixed` | Some improvement, but the original risk remains |
| `Unresolved` | No meaningful change found |
| `Regressed` | The revision made the issue worse or created inconsistency |
| `New issue` | A new problem introduced by revision |

## Output

```markdown
## Revision Audit

### Regression Table
| Issue ID | Previous Finding | Current Status | Evidence | Notes |
|---|---|---|---|---|

### New Issues
| Severity | Location | Finding | Required Fix |
|---|---|---|---|

### Go / No-Go Recommendation
[Ready / Needs targeted fixes / Needs another full audit]
```
