# /ars-revision-coach

Triggers the `academic-paper` skill in `revision-coach` mode.

**What it does:** Parses reviewer comments and produces a Revision Roadmap plus a Response Letter skeleton — without writing the revision itself.

**Model:** Opus (per project policy)

**Fidelity spectrum:** Balanced, medium oversight

## Usage

```
/ars-revision-coach
```

Paste reviewer comments when prompted.

## Input required

- Reviewer comments (any format: structured review, inline comments, email feedback)
- Editorial decision letter (optional)

## Output

1. **Revision Roadmap** — feedback organized by:
   - Priority (Critical / Major / Minor)
   - Theme (Methodology / Literature / Clarity / Structure / Other)
   - Action required for each concern

2. **Response Letter Skeleton** — pre-structured template with:
   - Placeholder for each reviewer concern
   - Suggested response framing
   - Cross-reference markers for manuscript changes

## Notes

- Does NOT write the revision — use `/ars-revision` for that
- Ideal when reviewer comments are long, overlapping, or contradictory
- See: `MODE_REGISTRY.md` § academic-paper | `academic-paper/SKILL.md`
