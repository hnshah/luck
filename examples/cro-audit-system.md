# Example: CRO Audit System

## Context

The Crazy Egg audit workflow produces screenshots, local-model CRO analysis, JSON reports, redesigned pages, QA, and deployment. The system has strong production value, but parts can still depend on operator memory and manual rescue.

## Luck Assessment: Crazy Egg CRO Audit System

### Verdict
- Durable if the workflow keeps becoming more self-checking

### Binding Constraint
- Circulation: audit learnings must flow back into templates, prompts, QA gates, and reusable components instead of staying trapped in one-off runs.

### Why
- Solvency is mixed: local models reduce cost, but manual rescue can still consume operator attention.
- Demand coupling is strong: companies have active conversion pain and want concrete fixes.
- Adoption friction is mixed: the workflow is powerful but still requires knowing which scripts, files, and quality gates matter.
- Compounding loop is the main opportunity: every audit should improve the next audit's prompts, examples, QA checks, and redesign patterns.

### Failure Mode To Avoid
- Fragmented ecology - screenshots, analysis, JSON, redesign, and deployment all work individually but do not feed a stronger whole.

### Next Test
- After each audit, require one reusable improvement to be captured in a prompt, template, script, QA rule, or example library.

### What To Do Now
1. Add a per-audit "system learning" field to run reports.
2. Promote repeated fixes into QA checks or templates.
3. Defer cosmetic workflow polish until the learning loop is reliable.

