# academic-paper v3.1.2
# Rules: shared/RULES.md (all rules apply)

## ROUTING
```
input has upstream deep-research artifacts? → skip Phase 1 (lit strategy)
mode = full?        → 8-phase pipeline, model: Opus
mode = plan?        → Phase 0 + Socratic planning only, model: Sonnet
mode = outline?     → Phase 0–2 only, model: Sonnet
mode = revision?    → Phase 7 only (needs draft + reviewer comments), model: Sonnet
mode = revision-coach? → parse comments → Roadmap + skeleton (no draft), model: Opus
mode = abstract-only?  → Phase 6 only, model: Sonnet
mode = lit-review?     → Phase 1 output only, model: Sonnet
mode = citation-check? → audit only, no edits, model: Sonnet
mode = format-convert? → Phase 8 only, model: Sonnet
mode = disclosure?     → disclosure statement only, model: Sonnet
```

## AGENTS & PHASES
```
Phase 0  config_interview   → collect: discipline, journal, style, word count, format, language
                              IRON RULE: explicit user confirmation required before Phase 1
Phase 1  lit_search         → (skip if deep-research artifacts present)
Phase 2  paper_architect    → structure + outline + evidence map
Phase 3  argument_builder   → claim-evidence mapping; identify gaps
Phase 4  draft_agent        → full-text; register calibration; PATTERN PROTECTION active
Phase 5  citation_verifier  → DOI/WebSearch check per shared/RULES.md; BLOCKS on fabrication
Phase 6  abstract_agent     → EN + zh-TW (independent composition, not translation) + keywords
Phase 7  revision_agent     → revised draft + point-by-point Response Letter + traceability matrix
Phase 8  format_converter   → LaTeX / DOCX / PDF / Markdown; citation style conversion
         disclosure_agent   → venue-specific AI-usage statement (mandatory in all modes)
```

## PATTERN PROTECTION (Phase 4 enforcement)
Flag and rewrite if found:
- Em-dash overuse (—) as sentence connectors
- Uniform paragraph length (±10% variance signals AI)
- Throat-clearing openers: "In today's world", "It is important to note", "In conclusion"
- Generic hedges not standard in target discipline

## CITATION STYLES
APA 7.0 · Chicago · MLA · IEEE · Vancouver

## OUTPUT FORMATS
Markdown · DOCX (Pandoc) · LaTeX (APA7 class) · PDF (tectonic)

## REVISION-COACH OUTPUT
1. Revision Roadmap: feedback sorted by Priority (Critical/Major/Minor) × Theme
2. Response Letter Skeleton: one entry per concern, framing suggestion, change cross-ref marker
Note: does NOT write the revision — use `revision` mode for that.

## DISCLOSURE VENUES
ICLR · NeurIPS · Nature · Science · ACL · EMNLP · (custom: provide venue policy)

## FORBIDDEN
- Advancing past Phase 0 without user config confirmation
- Fabricated citations (see shared/RULES.md — hard stop)
- Translating abstracts instead of independent composition
- Accepting reviewer criticism as revision guidance without user review
