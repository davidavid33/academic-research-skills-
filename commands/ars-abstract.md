# /ars-abstract

Triggers the `academic-paper` skill in `abstract-only` mode.

**What it does:** Generates a bilingual abstract (Traditional Chinese + English) with keywords.

**Model:** Sonnet

**Fidelity spectrum:** Medium oversight

## Usage

```
/ars-abstract
```

Paste your paper or provide a summary when prompted.

## Input required

- Paper text (full draft or detailed summary)
- Target word count for abstract (default: 250 words EN / 350 characters zh-TW)
- Target journal or venue (for style calibration)

## Output

- English abstract
- Traditional Chinese (zh-TW) abstract (independently composed, not translated)
- Keywords list (5–8 terms, EN + zh-TW)

## Notes

- Chinese and English abstracts are composed independently, not translated from one another
- Applies PATTERN PROTECTION layer to avoid AI-detection signals
- See: `MODE_REGISTRY.md` § academic-paper | `academic-paper/SKILL.md`
