---
description: Citation audit — missing refs, mismatches, format errors, suspected fabrications
model: sonnet
---

Invoke: `academic-paper` skill, mode: `citation-check`

Ask for: paper text with in-text citations, reference list, citation style.

Execute citation_verifier from academic-paper/SKILL.md.
Verify each citation via Semantic Scholar → OpenAlex → Crossref.

Output report with columns: Citation | Status | Error Type | Action
Status values: VERIFIED · UNVERIFIED · SUSPECTED_FABRICATION · FORMAT_ERROR · ORPHANED

Do NOT auto-correct. Report only.
