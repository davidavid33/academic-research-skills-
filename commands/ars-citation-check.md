# /ars-citation-check

Triggers the `academic-paper` skill in `citation-check` mode.

**What it does:** Produces a citation error report identifying missing references, mismatched in-text citations, and format errors.

**Model:** Sonnet

**Fidelity spectrum:** Low oversight (audit only, no edits)

## Usage

```
/ars-citation-check
```

Paste your paper text when prompted.

## Input required

- Paper text with in-text citations
- Reference list / bibliography
- Citation style (APA 7.0, Chicago, MLA, IEEE, or Vancouver)

## Output

Citation error report covering:

| Error Type | Description |
|-----------|-------------|
| Missing reference | In-text citation has no matching bibliography entry |
| Orphaned reference | Bibliography entry has no in-text citation |
| Format errors | Citations not conforming to specified style |
| Suspected fabrication | Citations that cannot be verified via DOI/WebSearch |
| Metadata mismatches | Author names, years, titles inconsistent between in-text and bibliography |

## Notes

- Fabricated references flagged separately with verification attempt log
- Does not auto-correct — produces report only
- See: `MODE_REGISTRY.md` § academic-paper | `academic-paper/SKILL.md`
