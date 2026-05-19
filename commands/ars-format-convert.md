# /ars-format-convert

Triggers the `academic-paper` skill in `format-convert` mode.

**What it does:** Converts academic papers between formats and citation styles.

**Model:** Sonnet

**Fidelity spectrum:** Low oversight

## Usage

```
/ars-format-convert
```

Specify source format, target format, and citation style when prompted.

## Supported Conversions

### Document Formats
| From | To | Tool |
|------|----|----|
| Markdown | DOCX | Pandoc |
| Markdown | LaTeX | Direct |
| Markdown | PDF | tectonic |
| LaTeX | DOCX | Pandoc |
| LaTeX | PDF | tectonic |
| DOCX | Markdown | Pandoc |

### Citation Styles
APA 7.0 ↔ Chicago ↔ MLA ↔ IEEE ↔ Vancouver

## Notes

- Requires Pandoc for DOCX output
- Requires tectonic for PDF output
- LaTeX output uses APA7 document class by default
- Citation style conversion preserves all metadata; formatting only changes
- See: `MODE_REGISTRY.md` § academic-paper | `academic-paper/SKILL.md`
