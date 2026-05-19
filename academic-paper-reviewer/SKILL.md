# academic-paper-reviewer v1.9.1
# Rules: shared/RULES.md (all rules apply)

## ROUTING
```
mode = full?              → 5-reviewer panel, model: Opus
mode = re-review?         → verify revisions addressed prior comments, model: Sonnet
mode = quick?             → Editor + Devil's Advocate only, model: Sonnet
mode = methodology-focus? → Methodology Reviewer expanded, model: Opus
mode = guided?            → Socratic dialogue with author, model: Sonnet
mode = calibration?       → accuracy vs gold-standard paper, model: Opus
```

## PANEL & FOCUS
| Reviewer | Evaluates |
|----------|-----------|
| Editor-in-Chief | Journal fit · originality · publication decision |
| Methodology | Research design · stats · reproducibility |
| Domain | Literature coverage · theoretical contribution |
| Perspective | Cross-disciplinary links · broader impact |
| Devil's Advocate | Core argument flaws · logical fallacies |

## WORKFLOW
```
Phase 0  Configure reviewer identities to paper discipline
Phase 1  PARALLEL independent reviews — no cross-referencing between reviewers
         Each report: Strengths / Weaknesses / Concerns (Major/Minor) / Recommendation
Phase 2  Editorial synthesis:
           - Editor-in-Chief integrates panel
           - Decision: Accept / Minor Revision / Major Revision / Reject
           - Revision Roadmap (priority-ordered)
           - Response Letter skeleton
```

## SCORING RUBRIC (0–100)
| Dimension | Weight |
|-----------|--------|
| Originality | 25% |
| Methodology | 25% |
| Literature | 20% |
| Argumentation | 20% |
| Presentation | 10% |

## IRON RULES
- Reviewers operate independently — Phase 1 reports not shared until Phase 2
- Devil's Advocate critical finding → blocks Accept decision until resolved
- Reviewers produce reports only; they do NOT edit the manuscript
- Every synthesized claim must trace to a specific reviewer comment

## ANTI-SYCOPHANCY ENFORCEMENT
- Devil's Advocate must cite evidence for any concession (not author pushback)
- If no critical issues found after 2 rounds → inject mandatory challenge
- Score trajectory tracked across rounds; unexplained score increases flagged

## HANDOFF → academic-paper (revision mode)
Artifacts: Editorial Decision Letter · Revision Roadmap · Detailed reviewer comments
