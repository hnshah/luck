# Luck Roadmap

Goal: make Luck consistently useful as an operating framework for agents and humans, without turning it into ceremony or vague strategy language.

The binding constraint is adoption friction. The framework is compelling, but users need a shorter path from "interesting theory" to "better next move."

## Current State

Already in the fork:
- luck.md - canonical theory and full conceptual model.
- luck.runtime.md - compact runtime instructions for agents.
- USAGE.md - operating ritual and quality bar.
- QUICKSTART.md - first-run guide.
- bin/luck-check - local Ollama CLI.
- templates/ - context templates for common use cases.
- examples/ - first practical assessments.
- evals/luck-runtime-effectiveness.yaml - small Verdict eval pack.

Validated so far:
- The compact runtime avoids most framework-performance behavior.
- Local Verdict eval runs with qwen2.5:7b and qwen2.5:32b.
- Outputs now include binding constraint, failure mode, next test, and do-now/do-next/defer.

## Phase 1 - Make Runtime Use Boring

Purpose: anyone should be able to use Luck in under two minutes.

Build:
- A one-page quickstart.
- A small bin/luck-check CLI wrapper.
- Install instructions for using luck.runtime.md as a Codex/OpenClaw/Claude skill.
- Three output modes: fast, standard, full.
- A copy-paste prompt for non-tool environments.

Done when:
- A user can assess a repo, workflow, or strategy choice with one command.
- The output is short enough to paste into an issue, PR comment, or planning doc.
- The default mode does not list all seven checks.

## Phase 2 - Expand Examples Into a Pattern Library

Purpose: make the framework concrete across domains.

Add examples for open-source adoption, AI workflow heroics, marketplace timing, SaaS onboarding, community knowledge circulation, fundraising, career decisions, product prioritization, content strategy, and internal ops.

Each example should include context, Luck assessment, what a weak answer would have said, why the binding constraint is the binding constraint, and the next test.

Done when users can find an example close to their situation and agents have enough demonstrations to stop being abstract.

## Phase 3 - Strengthen Evals

Purpose: prevent regressions and measure whether Luck is helping.

Add eval dimensions:
- Binding constraint accuracy.
- No framework performance.
- Concrete next test.
- Correct sequencing.
- Explicit defer/stop.
- Domain-language translation.
- Failure mode fit.

Build:
- More Verdict cases, at least 20.
- Paired baseline vs runtime eval.
- A deterministic lint for obvious failures: all seven checks in fast mode, missing next test, no defer/stop, too much abstract vocabulary.
- Score reports checked into evals/results/.

Done when runtime beats full luck.md on small and mid-sized local models and catches taxonomy-display regressions.

## Phase 4 - Add Context Templates

Purpose: improve input quality so Luck checks are not starved of evidence.

Create templates for repos, workflows, products, strategy choices, and personal decisions.

Each template should ask for current goal, current constraint, active demand, adoption path, maintenance burden, what repeats, what success makes easier next, and known friction.

Done when a shallow input can be turned into a useful assessment quickly and the template itself teaches the user what matters.

## Phase 5 - Integrate With Real Workflows

Purpose: Luck should change work, not live as a side document.

Integrations:
- OpenClaw/Codex skill install path.
- Local scripts/luck-check.py or repo-native CLI.
- Verdict eval command.
- CRO audit run reports: add Luck constraint / failure mode / next test.
- Repo review workflow: run after first inspection, before feedback.
- Workflow design docs: run when manual rescue repeats.

Done when the next three substantial projects use Luck once, each final note says whether the constraint changed, and at least one workflow improves because of the diagnosis.

## Phase 6 - Improve the Theory/Runtime Boundary

Purpose: preserve the original depth while keeping runtime use sharp.

Work:
- Keep luck.md as canonical theory.
- Keep luck.runtime.md as the operational layer.
- Add a concepts/ directory for solvency, circulation, integration, compounding loops, and timing.
- Add cross-links from runtime terms to theory sections.
- Add when-not-to-use guidance.

Done when runtime users are not overloaded and theory users can go deeper without polluting default agent behavior.

## Phase 7 - Build a Lightweight Scorecard

Purpose: make repeated assessments comparable.

Build a structured output option with verdict, binding_constraint, failure_mode, next_test, and seven Strong/Mixed/Weak scores.

Done when assessments can be tracked over time and we can compare whether an intervention changed the binding constraint.

## Near-Term Backlog

1. Expand eval pack from 3 to 20 cases.
2. Add example for community knowledge circulation.
3. Add example for AI marketplace timing.
4. Add result snapshots from Verdict evals.
5. Package as an installable OpenClaw/Codex skill.
6. Run Luck on the next three real projects and document outcomes.
7. Add deterministic lint for mode compliance.
8. Add concepts pages and cross-links back to luck.md.

## Quality Bar

Luck is working when it makes the next move clearer, identifies what to stop or defer, reduces manual rescue, turns isolated wins into reusable loops, and improves downstream artifacts.

Luck is failing when it adds jargon, lists all seven checks by default, produces strategy theater, does not change the next action, or requires a dedicated expert to interpret it.
