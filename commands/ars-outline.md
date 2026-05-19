# /ars-outline

Triggers the `academic-paper` skill in `outline` mode.

**What it does:** Produces a detailed paper outline with evidence map. Does not generate the full draft.

**Model:** Sonnet

**Fidelity spectrum:** Balanced, high oversight

## Usage

```
/ars-outline <topic or existing Chapter Plan>
```

## Example

```
/ars-outline Longitudinal study of urban heat island effects on respiratory health outcomes
```

## Output

- Section-by-section outline with subsection headings
- Evidence map: key citations mapped to each section
- Argument flow diagram (text-based)
- Gap analysis: sections needing additional sources

## Notes

- Provide a Chapter Plan (from `/ars-plan`) for best results
- Evidence map sources are verified via DOI/WebSearch
- See: `MODE_REGISTRY.md` § academic-paper | `academic-paper/SKILL.md`
