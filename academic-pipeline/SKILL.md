# academic-pipeline — Skill Definition

**Version:** 3.9.4.1 | **Status:** Active | **Updated:** 2026-05-18

---

## Overview

The orchestration layer coordinating all three skills (deep-research, academic-paper, academic-paper-reviewer) through a 10-stage workflow with mandatory integrity gates. The pipeline does not perform substantive work itself — it coordinates specialized skills and enforces quality checkpoints.

---

## 10-Stage Architecture

| Stage | Name | Skill Invoked |
|-------|------|--------------|
| 1 | RESEARCH | deep-research |
| 2 | WRITE | academic-paper |
| 2.5 | INTEGRITY CHECK | — (mandatory gate) |
| 3 | REVIEW | academic-paper-reviewer |
| 3' | RE-REVIEW | academic-paper-reviewer (re-review mode) |
| 4 | REVISE | academic-paper (revision mode) |
| 4' | RE-REVISE | academic-paper (revision mode, optional) |
| 4.5 | FINAL INTEGRITY | — (mandatory gate) |
| 5 | FINALIZE | academic-paper (format-convert mode) |
| 6 | PROCESS SUMMARY | — (documentation) |

---

## Mandatory Integrity Gates

### Stage 2.5 — Pre-Review Integrity
Runs before paper enters peer review. Checks:
- Citation hallucination (fabricated references)
- Implementation bugs
- Hallucinated experimental results
- Shortcut reliance (LLM parametric memory instead of literature)
- Bug-as-insight (misinterpreting errors as findings)
- Methodology fabrication
- Pipeline-level issues (stage skipping, artifact contamination)

**Suspected failures block progression to Stage 3.**

### Stage 4.5 — Final Integrity
Runs after revision, before finalization. Same checklist as 2.5, plus:
- Revision claim verification (did revisions actually address reviewer concerns?)
- R&R Traceability Matrix validation

**Suspected failures block Stage 5.**

---

## Adaptive Checkpoint System

After each stage, explicit user confirmation required before advancing.

| Checkpoint Type | When Used |
|----------------|-----------|
| `FULL` | Standard stage completion — complete deliverables list + decision dashboard |
| `SLIM` | Routine transitions — one-line status + explicit continue/pause prompt |
| `MANDATORY` | Integrity failures, review decisions, finalization — cannot be skipped |

### Quality Self-Check (before each checkpoint)
1. Citation integrity: all references verifiable?
2. Quality maintained across stages (no degradation)?
3. Scope discipline: no unauthorized expansions?
4. Completeness: all stage deliverables present?

---

## Collaboration Depth Observer

Advisory-only mechanism (never blocking) evaluating user collaboration patterns.

Four dimensions:
- **Delegation Intensity** — how much substantive work was delegated to AI
- **Cognitive Vigilance** — how actively user monitored AI outputs
- **Cognitive Reallocation** — how user invested time freed by AI
- **Zone Classification** — overall collaboration pattern category

Invoked at full checkpoints and pipeline completion. Never appears on the `Flagged` line.

---

## Material Passport

Enables cross-session resumption. Tracks:
- Which stages completed
- Artifacts produced at each stage
- Integrity check results
- Reviewer decisions

Mid-entry is supported: users can enter at any stage by providing prior materials.
**Exception: mid-entry cannot skip Stage 2.5** unless a previous integrity report is provided AND content is unchanged.

---

## Anti-Patterns (Prohibited)

1. Skipping integrity checks (2.5 or 4.5)
2. Orchestrator overstepping into substantive work
3. Auto-advancing past mandatory checkpoints
4. Quality degradation across stages
5. Silently dropping reviewer concerns
6. Selective re-verification (only rechecking favorable citations)
7. Inflated quality scoring
8. Bypassing the AI Research Failure Mode Checklist

---

## Iron Rules

1. **Both Stage 2.5 and Stage 4.5 must run the full AI Research Failure Mode Checklist.**
2. **Suspected failures block progression.** No override without explicit user authorization.
3. **Maximum one RE-REVISE round** after receiving Major Revision decision.
4. **All mandatory checkpoints require user confirmation** before pipeline advances.
