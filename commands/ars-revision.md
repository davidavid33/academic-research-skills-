# /ars-revision

Triggers the `academic-paper` skill in `revision` mode.

**What it does:** Generates a revised manuscript draft and point-by-point responses to reviewer feedback.

**Model:** Sonnet

**Fidelity spectrum:** High fidelity

## Usage

```
/ars-revision
```

Paste your draft and reviewer comments when prompted.

## Input required

1. Original manuscript (Markdown, plain text, or DOCX content)
2. Reviewer comments (structured or unstructured)
3. Editorial decision letter (optional but recommended)

## Output

- Revised manuscript draft with tracked changes (Markdown diff format)
- Point-by-point Response Letter addressing each reviewer concern
- R&R Traceability Matrix (links each revision to the reviewer comment it addresses)

## Notes

- For unstructured reviewer comments, use `/ars-revision-coach` first to generate a Revision Roadmap
- Maximum one RE-REVISE round after Major Revision decision
- See: `MODE_REGISTRY.md` § academic-paper | `academic-paper/SKILL.md`
