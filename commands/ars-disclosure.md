---
description: Venue-specific AI-usage disclosure statement
model: sonnet
---

Invoke: `academic-paper` skill, mode: `disclosure`

Argument `$ARGUMENTS` is the venue name (e.g. NeurIPS, Nature).
If no argument, ask for venue name.

Supported venues: ICLR · NeurIPS · Nature · Science · ACL · EMNLP
For unlisted venues: ask user to paste the venue's AI policy.

Ask: how was AI used? (research, drafting, citation verification, editing — select all that apply)

Output: formatted disclosure statement + placement recommendation (acknowledgements / methods / footnote).
