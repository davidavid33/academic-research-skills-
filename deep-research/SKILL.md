# deep-research v2.9.4
# Rules: shared/RULES.md (all rules apply)

## ROUTING
```
input has uncertainty/exploratory intent?  → mode: socratic
input has "systematic review" / "PRISMA"?  → mode: systematic-review
input has "fact-check" / "verify"?         → mode: fact-check
input has "literature review"?             → mode: lit-review
input has "quick" / "brief"?              → mode: quick
default                                    → mode: full
```
Override with: `[direct-mode] deep-research <mode> — <topic>`

## AGENTS & ORDER
```
Phase 1  research_question  → FINER-score RQ; clarify scope; DA checkpoint #1
Phase 2  bibliography       → search 3+ databases; log query strings
         source_verifier    → grade sources; flag predatory journals
Phase 3  synthesis          → cross-source integration; disclose contradictions
         risk_of_bias       → RoB 2 / ROBINS-I (systematic-review only)
         meta_analysis      → effect-size synthesis (systematic-review only)
         devils_advocate     → DA checkpoint #2 — BLOCKS on critical findings
Phase 4  report_compiler    → draft per mode spec below
Phase 5  editor_in_chief    → journal-style review
         ethics_review      → dual-use / disclosure scan — BLOCKS on serious concerns
         devils_advocate     → DA checkpoint #3
Phase 6  revisions          → max 2 rounds
         monitoring         → post-publication tracking (full mode only)
```

## MODE SPECS
| Mode | Output | Words |
|------|--------|-------|
| full | APA 7.0 report | 3 000–8 000 |
| quick | Research brief | 500–1 500 |
| lit-review | Annotated bibliography + synthesis | 1 500–4 000 |
| systematic-review | PRISMA 2020 + forest plots | 5 000–15 000 |
| fact-check | Claim verification report | 300–800 |
| socratic | Iterative dialogue → research plan | Iterative |
| paper-review | Structured critique | 800–2 000 |

## SOCRATIC PROTOCOL
Layers (in order, never skip): Clarification → Assumption Probing → Evidence/Reasoning → Viewpoint Exploration → Implication Analysis
Rule: guide discovery through questions; never give direct answers.

## HANDOFF → academic-paper
Artifacts: RQ Brief · Methodology Blueprint · Annotated Bibliography · Synthesis Report · Insight Collection
academic-paper auto-detects these and skips redundant phases.

## FORBIDDEN
- Confirmation bias in source selection
- Citing opinion-level sources at RCT tier
- Fabricated references (see shared/RULES.md)
- Shallow Socratic (answering instead of questioning)
