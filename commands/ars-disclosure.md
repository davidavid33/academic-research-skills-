# /ars-disclosure

Triggers the `academic-paper` skill in `disclosure` mode.

**What it does:** Generates a venue-specific AI-usage disclosure statement.

**Model:** Sonnet

**Fidelity spectrum:** Low oversight

## Usage

```
/ars-disclosure <venue name>
```

## Example

```
/ars-disclosure NeurIPS
```

## Supported Venues

| Venue | Policy Type |
|-------|------------|
| ICLR | Conference (ML) |
| NeurIPS | Conference (ML) |
| Nature | Journal (multidisciplinary) |
| Science | Journal (multidisciplinary) |
| ACL | Conference (NLP) |
| EMNLP | Conference (NLP) |

For venues not listed, provide the venue's AI disclosure policy and the statement will be generated to match.

## Input required

- Target venue
- Description of how AI was used (research assistance, drafting, citation verification, etc.)
- Author names (for attribution statement)

## Output

- Formatted disclosure statement matching venue requirements
- Placement recommendation (acknowledgements, methods, or footnote)

## Notes

- Disclosure is mandatory for all ARS pipeline outputs
- See: `MODE_REGISTRY.md` § academic-paper | `academic-paper/SKILL.md`
