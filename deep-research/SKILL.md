# deep-research — Skill Definition

**Version:** 2.9.4 | **Status:** Active | **Updated:** 2026-05-18

---

## Overview

A 13-agent universal academic research system supporting seven operational modes. Covers the full investigation cycle from research question formulation through synthesis, peer evaluation, and post-publication monitoring.

---

## Agent Roster

| Agent | Role |
|-------|------|
| `research_question_agent` | Transforms vague topics into FINER-scored research questions |
| `research_architect_agent` | Designs methodology blueprints |
| `bibliography_agent` | Conducts systematic literature searches across databases |
| `source_verification_agent` | Grades sources, detects predatory journals |
| `synthesis_agent` | Integrates findings across sources with contradiction disclosure |
| `report_compiler_agent` | Drafts APA 7.0 complete reports |
| `editor_in_chief_agent` | Provides journal-style editorial review |
| `devils_advocate_agent` | Challenges assumptions at three mandatory checkpoints |
| `ethics_review_agent` | Screens for disclosure requirements and dual-use concerns |
| `socratic_mentor_agent` | Guides exploratory research through five-layer dialogue |
| `risk_of_bias_agent` | Applies RoB 2 and ROBINS-I standards |
| `meta_analysis_agent` | Executes effect-size synthesis and forest plot generation |
| `monitoring_agent` | Tracks post-publication developments |

---

## Operational Modes

| Mode | Output | Word Count |
|------|--------|-----------|
| `full` | Complete APA 7.0 research report | 3,000–8,000 |
| `quick` | Research brief | 500–1,500 |
| `lit-review` | Annotated bibliography + synthesis | 1,500–4,000 |
| `systematic-review` | PRISMA 2020 report + forest plots | 5,000–15,000 |
| `fact-check` | Claim verification report | 300–800 |
| `socratic` | Research plan summary (iterative) | Iterative |
| `paper-review` | Structured paper critique | 800–2,000 |

---

## Six-Phase Workflow

**Phase 1 — Scoping**
- Research question formulation (FINER criteria)
- Methodology blueprint design
- Devil's Advocate Checkpoint #1

**Phase 2 — Investigation**
- Systematic literature search
- Source verification and grading
- Predatory journal detection

**Phase 3 — Analysis**
- Cross-source synthesis
- Risk-of-bias assessment (RoB 2, ROBINS-I)
- Contradiction identification and disclosure
- Devil's Advocate Checkpoint #2

**Phase 4 — Composition**
- Full APA 7.0 draft generation
- Evidence hierarchy enforcement
- Citation chain tracking

**Phase 5 — Review**
- Parallel: editorial review + ethics screening + vulnerability assessment
- Devil's Advocate Checkpoint #3

**Phase 6 — Revision**
- Feedback integration (max 2 iteration rounds)
- Final AI disclosure statement

---

## Trigger System

**English activation:** research, deep research, literature review, systematic review, PRISMA, evidence synthesis, fact-check, investigate, survey the literature

**Chinese activation:** 研究, 文獻回顧, 系統性回顧, 事實查核, 文獻綜述

**Socratic activation:** activates when user signals uncertainty about research direction, requests guided thinking, or asks exploratory questions regardless of exact wording.

**Default rule:** When intent is ambiguous between `socratic` and `full`, prefer `socratic` — safer to guide first than produce misaligned output.

---

## Iron Rules

1. **Devil's Advocate checkpoints are mandatory.** Critical-severity issues block phase progression.
2. **Ethics Review can halt delivery** for serious concerns (dual-use, undisclosed conflicts of interest).
3. **Every claim requires citation.** No unsupported assertions.

---

## Anti-Patterns (Prohibited)

- Confirmation bias in source selection
- Evidence cherry-picking
- Fabricated references
- Source-tier inflation (citing opinion as RCT-level evidence)
- Shallow Socratic dialogue that provides answers instead of guiding discovery

---

## Socratic Mode Protocol

Five-layer dialogue progression:
1. **Clarification** — what exactly do you want to understand?
2. **Assumption Probing** — what do you assume to be true?
3. **Evidence & Reasoning** — what supports this?
4. **Viewpoint Exploration** — what would a critic say?
5. **Implication Analysis** — what follows if this is true?

The mentor never gives direct answers. Users are guided to discover their own research direction.

---

## Handoff to academic-paper

Completed materials transferred downstream:
- Research Question Brief
- Methodology Blueprint
- Annotated Bibliography
- Synthesis Report
- Insight Collection

`academic-paper` automatically detects these artifacts and skips redundant steps.
