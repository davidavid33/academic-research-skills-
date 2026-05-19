# /ars-plan

Triggers the `academic-paper` skill in `plan` mode.

**What it does:** Produces a Chapter Plan + INSIGHT collection through Socratic dialogue with the user.

**Model:** Sonnet

**Fidelity spectrum:** Very high oversight

## Usage

```
/ars-plan <paper topic or working title>
```

## Example

```
/ars-plan Examining the role of microbiome diversity in treatment-resistant depression
```

## Output

- Chapter Plan (section-by-section structure with purpose statements)
- INSIGHT Collection (key claims and evidence gaps identified during dialogue)
- Recommended next step (proceed to `/ars-outline` or `/ars-full`)

## Notes

- Uses Socratic dialogue — expect questions before output
- High originality standards enforced throughout
- Ideal starting point when research direction is not fully defined
- See: `MODE_REGISTRY.md` § academic-paper | `academic-paper/SKILL.md`
