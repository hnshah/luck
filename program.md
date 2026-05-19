# Luck Autoresearch Program

This is an autonomous improvement loop for our Luck fork.

Your goal: make Luck more usable, consistent, measurable, and useful on real work.

## Setup

Before experimenting:

1. Confirm you are on a working branch.
2. Read:
   - README.md
   - luck.runtime.md
   - QUICKSTART.md
   - USAGE.md
   - AGGRESSIVE_ROADMAP.md
   - AUTORESEARCH_INTEGRATION.md
   - evals/luck-runtime-effectiveness.yaml
3. Run:
   - bin/luck-selftest
   - bin/luck-eval --quick
4. Confirm experiments/results.tsv exists.

## Editable Scope

You may edit:

- luck.runtime.md
- bin/luck-check
- bin/luck-selftest
- bin/luck-eval
- evals/luck-runtime-effectiveness.yaml
- examples/
- templates/
- QUICKSTART.md
- USAGE.md
- TESTING.md

Do not edit unless explicitly requested:

- luck.md
- dogfood/ledger.jsonl
- LICENSE

## Experiment Loop

Each experiment should be small and reviewable.

Loop:

1. Inspect current results.
2. Choose one improvement idea.
3. Edit files.
4. Run bin/luck-eval --quick.
5. If it passes, commit.
6. Run a fuller eval when the change touches runtime prompts or evaluator behavior.
7. Record result in experiments/results.tsv.
8. Keep improvements that pass.
9. Revert or discard regressions.

## Metrics

Track:

- selftest_pass
- json_schema_pass
- fast_mode_has_constraint
- fast_mode_has_failure_mode
- fast_mode_has_next_test
- fast_mode_has_defer
- eval_avg_score
- median_fast_tokens
- framework_performance_failures

## Keep Rules

Keep a change if:

- selftest passes
- JSON mode stays valid
- fast mode has constraint, failure mode, next test, and defer/stop
- output is more concrete or shorter
- eval score is stable or better
- the next action is clearer

## Discard Rules

Discard a change if:

- JSON mode breaks
- fast mode lists all seven checks
- output loses defer/stop
- next test becomes vague
- recommendations become generic
- CLI gets harder to use

## First Experiments

1. Add more eval cases for community circulation and marketplace timing.
2. Add deterministic lint for fast mode.
3. Improve JSON enum compliance.
4. Add examples for every failure mode.
5. Add dogfood recheck summaries.

