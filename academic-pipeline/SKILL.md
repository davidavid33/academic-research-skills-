# academic-pipeline v3.9.4.1
# Rules: shared/RULES.md (all rules apply)
# This skill ORCHESTRATES — it does no substantive work itself.

## ENTRY POINTS
```
/ars-full <topic>   → start at Stage 1
mid-entry           → detect available artifacts, suggest entry stage
                      EXCEPTION: cannot skip Stage 2.5 without prior integrity report + unchanged content
```

## PIPELINE
```
Stage 1    RESEARCH   → deep-research (full)
Stage 2    WRITE      → academic-paper (full)
────────── GATE 2.5 ──────────────────────────────── MANDATORY, cannot skip
Stage 3    REVIEW     → academic-paper-reviewer (full)
Stage 3'   RE-REVIEW  → academic-paper-reviewer (re-review)  [if revisions requested]
Stage 4    REVISE     → academic-paper (revision)
Stage 4'   RE-REVISE  → academic-paper (revision)  [optional, max 1 round]
────────── GATE 4.5 ──────────────────────────────── MANDATORY, cannot skip
Stage 5    FINALIZE   → academic-paper (format-convert)
Stage 6    SUMMARY    → process documentation + Collaboration Quality Report
```

## INTEGRITY GATES (2.5 & 4.5)
Run full AI Research Failure Mode Checklist:
- [ ] Citation hallucination (fabricated references)
- [ ] Hallucinated experimental results
- [ ] Shortcut reliance (parametric memory instead of literature)
- [ ] Methodology fabrication
- [ ] Bug-as-insight (misread error as finding)
- [ ] Implementation bugs in any code/analysis
- [ ] Pipeline integrity (stage skipping, artifact contamination, scope creep)

**Any suspected failure → STOP. Report finding. Await user decision. Do not auto-proceed.**

## CHECKPOINTS (after every stage)
```
FULL      → complete deliverables list + decision dashboard   [standard]
SLIM      → one-line status + continue/pause prompt           [routine transitions]
MANDATORY → integrity failures, review decisions, finalization [cannot skip]
```
Self-check before presenting checkpoint:
1. All citations verifiable?
2. Quality maintained (no degradation from prior stage)?
3. Scope unchanged?
4. All stage deliverables present?

## COLLABORATION DEPTH OBSERVER (advisory only, never blocks)
Dimensions: Delegation Intensity · Cognitive Vigilance · Cognitive Reallocation · Zone Classification
Invoked at: full checkpoints + pipeline completion
Never appears on Flagged line.

## MATERIAL PASSPORT
Tracks: stages completed · artifacts produced · integrity results · reviewer decisions
Enables cross-session resume. Surfaced at every FULL checkpoint.

## IRON RULES
- Gates 2.5 and 4.5 run the full checklist — no partial checks
- Suspected failures block progression — no user override without explicit confirmation
- Max 1 RE-REVISE round after Major Revision
- Orchestrator never performs substantive work (writing, analysis, citations)
- Auto-advance past mandatory checkpoints is forbidden

## FORBIDDEN
- Skipping integrity gates
- Overstepping into substantive work
- Silent quality degradation across stages
- Dropping reviewer concerns without traceability
- Selective re-verification of citations
