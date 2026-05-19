# academic-paper-reviewer — Skill Definition

**Version:** 1.9.1 | **Status:** Active | **Updated:** 2026-05-18

---

## Overview

A comprehensive academic peer review simulation system deploying five independent reviewers across three phases: field analysis, parallel multi-perspective review, and editorial synthesis.

---

## Review Panel

| Reviewer | Focus Area |
|----------|-----------|
| Editor-in-Chief | Journal fit, originality assessment, publication decision |
| Methodology Reviewer | Research design, statistical validity, reproducibility |
| Domain Reviewer | Literature coverage, theoretical contribution, field positioning |
| Perspective Reviewer | Cross-disciplinary connections, broader impact |
| Devil's Advocate | Core argument challenges, logical fallacy detection |

---

## Operational Modes

| Mode | Description | Model |
|------|-------------|-------|
| `full` | Comprehensive 5-reviewer assessment + editorial decision | Opus |
| `re-review` | Verify revisions addressed initial comments | Sonnet |
| `quick` | Rapid 15-minute assessment (Editor-in-Chief + Devil's Advocate only) | Sonnet |
| `methodology-focus` | In-depth methods evaluation (Methodology Reviewer expanded) | Opus |
| `guided` | Socratic dialogue helping authors understand issues | Sonnet |
| `calibration` | Measures reviewer accuracy against gold-standard papers | Opus |

---

## Three-Phase Workflow

**Phase 0 — Field Configuration**
- Reviewer identities calibrated to paper's discipline
- Domain Reviewer background matched to paper's subject area
- Journal tier and scope expectations set

**Phase 1 — Parallel Independent Review**
- All five reviewers operate independently without cross-referencing
- Each generates structured report with:
  - Strengths
  - Weaknesses
  - Specific concerns (major / minor)
  - Recommendation (Accept / Minor Revision / Major Revision / Reject)

**Phase 2 — Editorial Synthesis**
- Editor-in-Chief synthesizes panel findings
- Final decision issued (Accept / Minor / Major / Reject)
- Revision Roadmap generated
- Response Letter skeleton provided

---

## Iron Rules

1. **Reviewers operate independently.** No cross-referencing between Phase 1 reports.
2. **Devil's Advocate critical issues prevent acceptance decisions.** Must be resolved before Accept is possible.
3. **Reviewers produce reports only.** They never modify the manuscript.
4. **All synthesis must trace to specific reviewer comments.** No synthesized claims without source attribution.

---

## Quality Rubric (0–100 scoring)

| Dimension | Weight | Criteria |
|-----------|--------|----------|
| Originality | 25% | Novel contribution beyond existing literature |
| Methodology | 25% | Rigor, validity, reproducibility |
| Literature Coverage | 20% | Breadth and depth of engagement |
| Argumentation | 20% | Logical coherence, evidence quality |
| Presentation | 10% | Clarity, structure, citation accuracy |

---

## Anti-Sycophancy Protocol

- Devil's Advocate must justify any concessions with evidence
- Concession threshold: requires explicit counter-evidence, not author pushback
- Editor-in-Chief tracks Devil's Advocate challenge resolution across rounds
- Dialogue health monitoring: automatic challenge injection if no critical issues found after 2 rounds

---

## Integration

**Incoming:** Complete paper from `academic-paper` (discipline auto-detected)

**Outgoing (to academic-paper revision mode):**
- Editorial Decision Letter
- Revision Roadmap (prioritized by severity)
- Detailed reviewer comments with line references
