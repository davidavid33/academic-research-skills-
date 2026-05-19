# Academic Research Skills — Claude Routing Configuration

**Version:** 3.9.4.1 | **Updated:** 2026-05-18 | **Creator:** Cheng-I Wu | **License:** CC-BY-NC 4.0

---

## Skill Registry

| Skill | Trigger Keywords | Default Mode |
|-------|-----------------|--------------|
| `deep-research` | research, deep research, literature review, systematic review, PRISMA, evidence synthesis, fact-check | socratic (ambiguous) / full |
| `academic-paper` | write paper, draft, outline, abstract, citation, revision | plan (ambiguous) / full |
| `academic-paper-reviewer` | review paper, peer review, evaluate manuscript | full |
| `academic-pipeline` | full pipeline, research to publication, end-to-end | full |

---

## Routing Framework

### Classification Rules

1. **Explicit intent** (slash commands or unambiguous keywords) → Direct routing to skill + mode
2. **Cross-phase materials** (artifacts spanning multiple pipeline stages) → Request clarification
3. **Ambiguous input without artifacts** → Ask which skill/mode fits best

### Escape Hatch

Prepend `[direct-mode]` to skip clarification and route directly:
```
[direct-mode] /deep-research full — <topic>
```

### Skill Selection Guidelines

- **End-to-end workflow** → `academic-pipeline`
- **Research investigation only** → `deep-research`
- **Writing/drafting only** → `academic-paper`
- **Evaluating an existing paper** → `academic-paper-reviewer`
- **Ambiguous between socratic and full** → prefer `socratic` (safer to guide first)

---

## Handoff Materials

### Research → Writing
- RQ Brief
- Methodology Blueprint
- Annotated Bibliography
- Synthesis Report
- Insight Collection

When `academic-paper` detects upstream artifacts from `deep-research`, it automatically skips redundant phases.

### Writing → Review
- Complete paper text (domain auto-detected for reviewer panel configuration)

### Review → Revision
- Editorial Decision Letter
- Revision Roadmap
- Detailed Reviewer Comments

---

## Operational Principles

1. Output language matches user input language (English and Traditional Chinese supported)
2. Every claim requires citation — no unsupported assertions
3. AI assistance must be disclosed in all deliverables
4. Evidence hierarchy: meta-analyses > RCTs > observational studies > case reports > expert opinion
5. Contradictions between sources must be disclosed with explicit quality comparisons

---

## Plugin Announcement

When this plugin loads, announce:

```
Academic Research Skills v3.9.4.1 loaded.
Available commands: /ars-full /ars-plan /ars-outline /ars-revision /ars-revision-coach /ars-abstract /ars-lit-review /ars-citation-check /ars-format-convert /ars-disclosure
Type /ars-full to start the complete pipeline, or use individual commands for targeted tasks.
```
