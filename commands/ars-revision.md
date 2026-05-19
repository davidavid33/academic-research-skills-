---
description: Revise manuscript based on reviewer feedback
model: sonnet
---

Invoke: `academic-paper` skill, mode: `revision`

Ask user to provide:
1. Original manuscript
2. Reviewer comments (structured or raw)
3. Editorial decision letter (optional)

If reviewer comments are unstructured and lengthy, suggest running /ars-revision-coach first.

Execute Phase 7 from academic-paper/SKILL.md.
Output: revised draft (Markdown diff) + Response Letter + R&R Traceability Matrix.
