# Example: Local Model Stack Circulation

## Context

The workspace has a validated local model stack: qwen3:235b for CRO analysis, qwen3-coder:30b for structured generation and HTML, qwen2.5 models for fast checks and Luck, and llama3.3:70b for judging. The stack saves cost and increases throughput.

## Luck Assessment: Local Model Stack

### Verdict
- Promising but fragile

### Binding Constraint
- Circulation: model-run learnings need to flow into scripts, eval packs, routing docs, and automated checks.

### Why
- Demand coupling is strong because local models support recurring real workflows.
- Integration is strong because the stack already plugs into Ollama, MLX, OpenClaw, Verdict, and CRO scripts.
- Adoption friction is weak because using the right model still depends on knowing service state, endpoints, prompts, and timeouts.
- Circulation is weak because validation history can stay in MEMORY.md or reports instead of executable routing and tests.

### Failure Mode To Avoid
- Institutional zombie - the documented model stack survives, but parts become stale because real outcomes stop updating the system.

### Next Test
- Create a model-routing snapshot and check whether a new workflow can select the right model from that artifact without rereading memory files.

### What To Do Now
1. Document current routing, eval packs, prompt templates, timeout defaults, and fallback rules in one checkable place.
2. Convert repeated model lessons into Verdict cases or script defaults.
3. Defer adding more model options until the validated options are easier to route.

## Weak Generic Answer

The weak answer would benchmark more models immediately. More benchmarks help only if the results circulate into routing decisions and automated checks.

## Recheck Criteria

Recheck after routing has a checkable artifact. The constraint improves if model choice becomes executable instead of tribal knowledge.

