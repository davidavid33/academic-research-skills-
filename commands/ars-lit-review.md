# /ars-lit-review

Triggers the `academic-paper` skill in `lit-review` mode.

**What it does:** Produces an annotated bibliography rendered as a literature review section.

**Model:** Sonnet

**Fidelity spectrum:** Medium oversight

## Usage

```
/ars-lit-review <topic or list of sources>
```

## Example

```
/ars-lit-review Cognitive load theory in multimedia learning environments
```

## Output

- Prose literature review section (not just a list)
- Annotated bibliography with source grading
- Thematic organization with synthesis across sources
- Identified research gaps

## Notes

- For upstream research-phase literature reviews requiring annotated bibliography + synthesis analysis, prefer `deep-research` skill in `lit-review` mode instead
- This mode targets writing-phase integration of literature, not investigation
- All citations verified via DOI/WebSearch
- See: `MODE_REGISTRY.md` § academic-paper | `academic-paper/SKILL.md`
