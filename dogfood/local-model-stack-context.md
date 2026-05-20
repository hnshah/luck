# Local Model Stack Context

## Goal

Use local models for most reasoning, analysis, HTML generation, and evaluation while reserving frontier/tool agents for orchestration and file operations.

## Current State

The workspace has validated local model roles: qwen3:235b for CRO strategic analysis, qwen3-coder:30b for structured and HTML generation, qwen2.5:7b for fast orchestration-style calls, qwen2.5:32b for Luck and Verdict checks, and llama3.3:70b for judging.

## Active Demand

Local models reduce cost and improve throughput for Crazy Egg audits, Verdict evals, strategy checks, prompt experiments, and repeatable content generation.

## Adoption Path

Scripts call Ollama or MLX models for specific tasks. Human/agent operators choose a model based on documented task-model mappings.

## Adoption Friction

The stack depends on service state, correct endpoints, prompt shape, model availability, timeouts, and remembering which models have been validated for which tasks.

## Maintenance Burden

Model behavior changes, servers need to be running, failures can be silent, and validation results need to stay current as workflows evolve.

## Compounding Loop

Every successful or failed run should update model routing, eval packs, prompt templates, timeout defaults, and fallback rules.

## Circulation

Model learnings live in MEMORY.md and scattered reports. They become durable when they flow into scripts, Verdict packs, model-selection docs, and automated checks.

## Integration

The stack integrates with Ollama, MLX, OpenClaw, Verdict, CRO scripts, and local automation.

## Known Failure

Institutional zombie: the documented stack survives, but parts become stale unless evals and real workflow outcomes keep it alive.
