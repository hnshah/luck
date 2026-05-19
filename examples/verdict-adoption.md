# Example: Verdict Repo Adoption

## Context

Verdict is an LLM eval framework with strong architecture: multiple providers, result storage, leaderboard publishing, routing, eval packs, and local Ollama support.

Local inspection found it can pass doctor, typecheck, tests, build, and JSON smoke runs. But first-run adoption remains fragile: model setup, config, judge constraints, noisy CLI behavior, and generic examples can block new users before they reach the payoff.

## Luck Assessment: Verdict Repo Adoption

### Verdict
- Promising but fragile

### Binding Constraint
- Adoption friction is higher than the immediate payoff for a new evaluator.

### Why
- Solvency is strong: the repo can run and has a real test/build path.
- Demand coupling is real: LLM teams need repeatable evals and routing evidence.
- Adoption friction is weak: users must understand config, local models, judges, packs, and storage before they see value.
- Circulation is promising: results, leaderboards, and routing can turn eval runs into reusable intelligence once the first run works.

### Failure Mode To Avoid
- Heroic treadmill - maintainers have to personally help users over setup friction instead of the repo teaching the path.

### Next Test
- Give a new user a single command and a known-good local config; measure whether they can produce a clean JSON result in under 10 minutes without maintainer help.

### What To Do Now
1. Ship a first-run path with one local model, one judge, one tiny eval pack, and expected output.
2. Replace generic examples with task-specific starter packs.
3. Defer advanced routing/leaderboards until the first successful eval is boring.

