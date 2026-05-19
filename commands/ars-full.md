# /ars-full

Triggers the `academic-pipeline` orchestrator in `full` mode.

**What it does:** Runs the complete research → write → review → revise → finalize pipeline (10 stages).

**Model:** Opus (project policy)

**Fidelity spectrum:** Maximum oversight

**Estimated cost:** $4–6 USD for a 15,000-word paper

## Usage

```
/ars-full <topic or research question>
```

## Example

```
/ars-full The effect of sleep deprivation on working memory consolidation in adults
```

## Pipeline stages executed

1. RESEARCH (deep-research full mode)
2. WRITE (academic-paper full mode)
2.5 INTEGRITY CHECK (mandatory gate)
3. REVIEW (academic-paper-reviewer full mode)
3' RE-REVIEW (if revisions requested)
4. REVISE (academic-paper revision mode)
4' RE-REVISE (if needed, max 1 round)
4.5 FINAL INTEGRITY CHECK (mandatory gate)
5. FINALIZE (format conversion)
6. PROCESS SUMMARY

## Notes

- Each stage requires explicit user confirmation before advancing
- Integrity gates at 2.5 and 4.5 cannot be skipped
- See: `MODE_REGISTRY.md` § academic-pipeline | `academic-pipeline/SKILL.md`
