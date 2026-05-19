# Mode Registry

Central reference for all operational modes across the Academic Research Skills suite.

---

## deep-research

| Mode | Trigger | Output | Word Count | Model |
|------|---------|--------|-----------|-------|
| `full` | "research", "deep research" | Complete APA 7.0 report | 3,000–8,000 | Opus |
| `quick` | "quick brief", "brief summary" | Research brief | 500–1,500 | Sonnet |
| `lit-review` | "literature review", "annotated bibliography" | Annotated bibliography + synthesis | 1,500–4,000 | Sonnet |
| `systematic-review` | "systematic review", "PRISMA", "meta-analysis" | PRISMA 2020 report + forest plots | 5,000–15,000 | Opus |
| `fact-check` | "fact check", "verify claim" | Claim verification report | 300–800 | Sonnet |
| `socratic` | uncertainty signals, exploratory questions | Research plan summary (iterative) | Iterative | Sonnet |
| `paper-review` | "review this paper", "critique" | Structured paper critique | 800–2,000 | Sonnet |

---

## academic-paper

| Mode | Trigger / Command | Output | Model |
|------|-------------------|--------|-------|
| `full` | `/ars-full` (writing phase) | Complete paper draft | Opus |
| `plan` | `/ars-plan` | Chapter Plan + INSIGHT collection | Sonnet |
| `outline` | `/ars-outline` | Detailed outline + evidence map | Sonnet |
| `revision` | `/ars-revision` | Revised draft + Response Letter | Sonnet |
| `abstract-only` | `/ars-abstract` | Bilingual abstract (EN + zh-TW) | Sonnet |
| `lit-review` | `/ars-lit-review` | Literature review section | Sonnet |
| `citation-check` | `/ars-citation-check` | Citation error report | Sonnet |
| `revision-coach` | `/ars-revision-coach` | Revision Roadmap + Response skeleton | Opus |
| `format-convert` | `/ars-format-convert` | Converted document | Sonnet |
| `disclosure` | `/ars-disclosure` | AI-usage disclosure statement | Sonnet |

---

## academic-paper-reviewer

| Mode | Description | Model |
|------|-------------|-------|
| `full` | 5-reviewer assessment + editorial decision | Opus |
| `re-review` | Verify revisions addressed initial comments | Sonnet |
| `quick` | 15-minute rapid assessment | Sonnet |
| `methodology-focus` | In-depth methods evaluation | Opus |
| `guided` | Socratic dialogue for authors | Sonnet |
| `calibration` | Accuracy measurement against gold standard | Opus |

---

## academic-pipeline

| Mode | Description | Model |
|------|-------------|-------|
| `full` | Complete 10-stage pipeline | Opus |
| `mid-entry` | Resume from specified stage | Inherits from invoked skill |

---

## Model Assignment Rationale

- **Opus** — full drafting, revision coaching, complete pipeline (maximum capability required)
- **Sonnet** — targeted tasks, analysis, structured outputs (speed + cost efficiency)
