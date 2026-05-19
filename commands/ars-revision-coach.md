---
description: Parse reviewer comments → Revision Roadmap + Response Letter skeleton
model: opus
---

Invoke: `academic-paper` skill, mode: `revision-coach`

Ask user to paste reviewer comments and editorial decision letter (optional).

Execute revision_coach_agent from academic-paper/SKILL.md.
Output:
  1. Revision Roadmap sorted by Priority (Critical/Major/Minor) × Theme
  2. Response Letter Skeleton with placeholder per concern

Do NOT write the revision. Direct user to /ars-revision for that.
