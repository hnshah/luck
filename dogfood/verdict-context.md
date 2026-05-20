# Verdict Context

## Goal

Make Verdict the default local model evaluation and routing tool for real work.

## Current State

Verdict has a strong technical surface: model benchmarking, local/cloud providers, eval packs, regression detection, routing, OpenAI-compatible proxy, daemon, watch mode, and history.

## Active Demand

We need model selection for OpenClaw, Crazy Egg audits, local model routing, prompt regression checks, and deciding when local models beat paid frontier models.

## First-Run Path

The README points users to npm install or npx verdict init, then verdict run. The repo also has eval-pack docs, quick-start workflow docs, examples, model discovery, dry runs, and tests.

## Adoption Friction

The product surface is broad. A new user may not know which path to choose first: benchmark, write an eval pack, discover models, route prompts, run a daemon, or use the proxy. The first success path may be buried under advanced power.

## Maintenance Burden

Verdict depends on better-sqlite3 native bindings, provider configuration, eval pack quality, model availability, and local service state. Setup failures can look like product failures.

## Compounding Loop

Every eval run can create model history, routing data, regression knowledge, and better task-specific packs.

## Circulation

Results need to flow back into routing defaults, README examples, local model stack decisions, and OpenClaw workflows.

## Integration

Verdict can integrate through CLI, YAML packs, local history, daemon, proxy, and model discovery. The main risk is that these integrations are too many before the first win is obvious.

## Known Failure

Verdict could become a powerful evaluator that only expert operators use, instead of a default tool people reach for before choosing a model.
