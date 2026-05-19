# academic-paper — Skill Definition

**Version:** 3.1.2 | **Status:** Active | **Updated:** 2026-05-18

---

## Overview

A 12-agent paper writing pipeline for generating publishable academic papers across disciplines. Supports 10 operational modes from full-paper generation to targeted single-phase tasks.

---

## Agent Roster

| # | Agent | Responsibility |
|---|-------|---------------|
| 1 | `config_interview_agent` | Gathers paper specs (discipline, journal, style, word count) |
| 2 | `lit_search_strategy_agent` | Designs literature search strategy |
| 3 | `paper_architect_agent` | Designs paper structure and outline |
| 4 | `argument_construction_agent` | Builds argumentative structure |
| 5 | `draft_agent` | Full-text drafting with register and discipline adjustment |
| 6 | `citation_compliance_agent` | Citation verification via DOI/WebSearch |
| 7 | `abstract_agent` | Bilingual abstract generation (EN + zh-TW) |
| 8 | `simulated_reviewer_agent` | 5-dimensional pre-submission quality scoring |
| 9 | `format_conversion_agent` | LaTeX, DOCX, PDF, Markdown conversion |
| 10 | `plan_mentor_agent` | Socratic chapter-by-chapter planning |
| 11 | `figure_agent` | Publication-ready figure generation |
| 12 | `revision_coach_agent` | Parses reviewer comments into Revision Roadmap |

---

## Operational Modes

| Mode | Output | Model |
|------|--------|-------|
| `full` | Complete paper draft | Opus |
| `plan` | Chapter Plan + INSIGHT collection via Socratic dialogue | Sonnet |
| `outline` | Detailed outline + evidence map, no full draft | Sonnet |
| `revision` | Revised draft + point-by-point reviewer responses | Sonnet |
| `abstract-only` | Bilingual abstract (EN + zh-TW) + keywords | Sonnet |
| `lit-review` | Annotated bibliography as literature review section | Sonnet |
| `citation-check` | Citation error report | Sonnet |
| `revision-coach` | Revision Roadmap + Response Letter skeleton | Opus |
| `format-convert` | Cross-format document conversion | Sonnet |
| `disclosure` | Venue-specific AI-usage disclosure statement | Sonnet |

---

## Eight-Phase Workflow (full mode)

**Phase 0 — Configuration**
- Interview agent collects: discipline, target journal, citation style, word count, output format, language preference
- IRON RULE: explicit user confirmation of configuration record required before Phase 1

**Phase 1 — Literature Foundation**
- Search strategy design
- Upstream artifact detection (skips if deep-research materials present)

**Phase 2 — Architecture**
- Paper structure design
- Outline with evidence map

**Phase 3 — Argument Construction**
- Core claims identified
- Evidence mapped to claims

**Phase 4 — Drafting**
- Full-text generation with register calibration
- PATTERN PROTECTION: flags em-dash overuse, uniform paragraph lengths, AI throat-clearing openers

**Phase 5 — Citation Compliance**
- Every citation verified via DOI or WebSearch
- Fabricated references trigger immediate rejection

**Phase 6 — Abstract & Keywords**
- Independent bilingual composition (EN + zh-TW, not translation)

**Phase 7 — Pre-submission Review**
- 5-dimensional simulated peer review
- Quality score trajectory tracking

**Phase 8 — Format & Disclosure**
- Output format conversion
- AI disclosure statement generation

---

## Quality Safeguards

### Citation Integrity
- Every citation must be verified via DOI or WebSearch
- Three-layer citation anchoring: quotation → page → section
- Semantic Scholar + OpenAlex + Crossref triangulation
- Fabricated references → immediate rejection and restart

### Anti-Pattern Protection (PATTERN PROTECTION layer)
- Flags em-dash (—) overuse
- Flags uniform paragraph lengths (AI signal)
- Flags throat-clearing openers ("In today's world...", "It is important to note...")
- Enforces discipline-specific vocabulary

### Style Calibration
- Learns from user's past work when samples provided
- Adjusts register, sentence complexity, hedging language
- Never impersonates — calibrates to discipline norms

---

## Supported Citation Styles

APA 7.0 | Chicago | MLA | IEEE | Vancouver

## Supported Output Formats

Markdown | DOCX (via Pandoc) | LaTeX (APA7 class) | PDF (via tectonic)

## Supported Paper Structures

IMRaD | Thematic review | Case study | Policy brief | Conference paper

---

## Handoff Integration

**Incoming (from deep-research):**
- RQ Brief → skips Phase 1 literature strategy
- Annotated Bibliography → imported directly
- Synthesis Report → informs Phase 3 argument construction

**Outgoing (to academic-paper-reviewer):**
- Complete paper text with auto-detected discipline for reviewer panel configuration
