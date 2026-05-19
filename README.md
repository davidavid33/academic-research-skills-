# Academic Research Skills for Claude Code

A comprehensive suite of Claude Code skills for academic research, covering the full pipeline from research to publication.

## Core Skills

| Skill | Version | Description |
|-------|---------|-------------|
| **deep-research** | v2.9.4 | 13-agent research team, 7 modes (full, quick, lit-review, systematic-review, fact-check, socratic, paper-review) |
| **academic-paper** | v3.1.2 | 12-agent writing pipeline, 10 modes (full, plan, outline, revision, abstract-only, lit-review, citation-check, revision-coach, format-convert, disclosure) |
| **academic-paper-reviewer** | v1.9.1 | 5-reviewer peer review panel, 6 modes (full, re-review, quick, methodology-focus, guided, calibration) |
| **academic-pipeline** | v3.9.4.1 | 10-stage orchestrator with mandatory integrity gates |

## Installation

```
/plugin marketplace add Imbad0202/academic-research-skills
/plugin install academic-research-skills
```

## Slash Commands

| Command | Description |
|---------|-------------|
| `/ars-full` | Run complete research → write → review → revise → finalize pipeline |
| `/ars-plan` | Socratic chapter planning with high originality |
| `/ars-outline` | Detailed outline + evidence map, no full draft |
| `/ars-revision` | Revise draft based on reviewer feedback |
| `/ars-revision-coach` | Parse reviewer comments → Revision Roadmap + Response Letter |
| `/ars-abstract` | Bilingual abstract (EN + zh-TW) with keywords |
| `/ars-lit-review` | Annotated bibliography rendered as literature review section |
| `/ars-citation-check` | Citation error report (missing refs, mismatches, format errors) |
| `/ars-format-convert` | Convert between LaTeX, DOCX, PDF, Markdown |
| `/ars-disclosure` | Venue-specific AI-usage disclosure statement |

## Design Philosophy

**AI is your copilot, not the pilot.** The toolkit handles reference hunting, citation formatting, and data verification — leaving human researchers to define research questions, choose methods, and interpret findings.

Key safeguards:
- Mandatory Devil's Advocate checkpoints (cannot be skipped)
- Two integrity gates (Stages 2.5 & 4.5) checking for hallucinated citations and fabricated methodology
- Citation verification via Semantic Scholar, OpenAlex, and Crossref triangulation
- Anti-sycophancy protocols with concession thresholds

## Performance & Cost

Full 15,000-word paper pipeline: estimated **$4–6 USD** in token costs.

## License

[CC BY-NC 4.0](LICENSE) — Attribution required; non-commercial use only.

## Credits

Created by Cheng-I Wu. Contributors: aspi6246, mchesbro1, cloudenochcsis.
