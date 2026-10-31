# Global Skills Registry

This repository maintains a directory of reusable
ChatGPT skills.

## Skill Activation

When a user explicitly requests a registered skill:

1. Identify the requested skill in this registry.
2. Retrieve its SKILL.md file from the specified GitHub URL.
3. Read any supporting files required by the skill.
4. Follow the skill instructions when performing the task.
5. If retrieval fails, inform the user rather than
   claiming the skill was executed.

Do not activate skills for unrelated requests.

---

## Registered Skills

### Humanizer

Description:
Rewrites text to sound natural, authentic, and human
while preserving its original meaning.

Activation phrases:
- Humanize this text
- Run Humanizer
- Use my Humanizer skill
- Make this sound more human

Repository:
https://github.com/LUISDA182/humanizer

Skill Instructions:
https://github.com/LUISDA182/humanizer/blob/main/SKILL.md

Activation:
Explicit request only.

Status:
Active

### Brand Designer

Description:
Develops distinct business and product brand identities, complete branding kits, and reusable guidelines. Supports brand strategy, naming, logo systems, typography, color palettes, brand voice, illustrated brand manuals, identity audits, and approved revisions.

Activation phrases:
- Run Brand Designer
- Use my Brand Designer skill
- Create a brand identity
- Design a branding kit
- Create a brand manual
- Audit this brand identity

Repository:
https://github.com/LUISDA182/global-skills/tree/main/brand-designer

Skill Instructions:
https://github.com/LUISDA182/global-skills/blob/main/brand-designer/SKILL.md

Activation:
Explicit request only.

Status:
Active

### Document & Presentation Theme Manager

Skill name:
`document-presentation-theme-manager`

Description:
Applies three independent themes to documents and presentations: Academic Clarity for student assessments and study guides (digital and grayscale print), Institutional Professional for formal Science Department reports, and Scientific Discovery for engaging classroom presentations. Preserves school letterhead and content; includes theme routing, overrides, accessibility checks, font fallbacks, validation, and optional template guidance.

Activation phrases:
- Run Document & Presentation Theme Manager
- Use my Theme Manager skill
- Apply Academic Clarity
- Apply Institutional Professional
- Apply Scientific Discovery
- Format this using my document and presentation themes

Repository:
https://github.com/LUISDA182/global-skills/tree/main/document-presentation-theme-manager

Skill Instructions:
https://github.com/LUISDA182/global-skills/blob/main/document-presentation-theme-manager/SKILL.md

Supporting directories:
- `document-presentation-theme-manager/themes/`
- `document-presentation-theme-manager/references/`

Activation:
Explicit request only. After activation, automatically route each deliverable to the appropriate theme unless the user overrides the choice. Read required supporting files before applying the theme.

Status:
Active
