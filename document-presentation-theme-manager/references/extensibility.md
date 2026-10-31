# Extending the package

Add a theme only when requested. Give it a unique stable ID and version and a standalone file under `themes/`. Define its purpose/audience, full semantic color palette and allowed foreground/background pairs, font chains, document and/or slide sizes, spacing and minimum readable sizes, chart/table treatment, print adaptation, and format limitations. Do not use inheritance between themes.

Add its routing row to SKILL.md with a discriminating trigger. Keep existing theme IDs, numbers and behavior stable unless a revision is explicitly requested. An override for one artifact is not a new global default. Shared accessibility and preservation rules remain applicable; move a rule into the shared layer only when it genuinely applies to every theme.

Before accepting a revision, check overlapping routes, explicit override precedence, source preservation, font fallback, contrast pairs, a representative render and applicable grayscale proof. Record theme versions in artifact handoff notes when reproducibility matters. Do not automatically install or publish the updated package.
