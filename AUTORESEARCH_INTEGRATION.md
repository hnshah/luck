# Autoresearch Integration

Source: karpathy/autoresearch.

## What Matters

Karpathy's autoresearch is not primarily "AI does ML research." The transferable pattern is:

1. One constrained experimental surface.
2. One fixed time budget per experiment.
3. One objective metric.
4. One agent instruction file that the human improves.
5. A keep/discard loop.
6. A results ledger.
7. Overnight throughput.

For Luck, this is directly relevant. We can use the same pattern to improve the runtime, examples, evals, and dogfood loop.

## Karpathy Pattern

Autoresearch structure:

- prepare.py: fixed setup and evaluation utilities. Do not modify.
- train.py: one editable file. The agent experiments here.
- program.md: human-authored research org code. The agent reads this and runs the loop.
- results.tsv: untracked experiment ledger.
- metric: val_bpb, lower is better.
- fixed time budget: 5 minutes per experiment.
- outcome: keep improving commits, discard regressions.

The important design choice is comparability. Every experiment gets the same budget and same metric.

## Luck Translation

Luck equivalent:

- luck.runtime.md: primary editable runtime surface.
- evals/luck-runtime-effectiveness.yaml: evaluation task set.
- bin/luck-check: execution harness.
- bin/luck-selftest: install smoke test.
- dogfood/ledger.jsonl: real-world assessment ledger.
- program.md: agent instructions for autonomous Luck improvement.
- experiments/results.tsv: experiment results ledger.

Primary metric should be a bundle, not one score:

- eval_avg_score: Verdict average score.
- json_pass_rate: schema-valid JSON outputs.
- defer_coverage: outputs that say what to defer/stop.
- fast_token_median: fast mode output length.
- framework_performance_failures: outputs that recite the framework instead of deciding.
- dogfood_change_rate: rechecks where the binding constraint changed or next test sharpened.

## What To Incorporate Now

### 1. Add program.md

This gives agents a bounded loop for improving Luck itself.

The editable scope should be narrow:

- luck.runtime.md
- evals/luck-runtime-effectiveness.yaml
- examples/
- templates/
- bin/luck-check
- bin/luck-selftest

Protected files:

- luck.md should not be modified during autoresearch unless explicitly requested.
- README.md should only be updated after a kept improvement.
- dogfood/ledger.jsonl should not be rewritten.

### 2. Add experiments/results.tsv

Track:

- commit
- metric
- status
- changed_files
- description

### 3. Add bin/luck-eval

Run the repeatable checks:

- bin/luck-selftest
- Verdict dry-run
- sample fast mode
- sample JSON mode
- optional full Verdict eval

Use qwen2.5:32b as the default eval model for now. qwen2.5:7b is useful for stress testing fast mode, but it can leave required JSON fields empty.

### 4. Define Keep/Discard Rules

Keep if:

- selftest passes
- JSON mode passes schema
- fast output includes constraint/failure/next-test/defer
- eval score does not regress
- output gets shorter or more decisive without losing next-test quality

Discard if:

- JSON breaks
- output recites all seven checks in fast mode
- next test missing
- defer/stop missing
- intervention advice becomes generic
- CLI gets harder to use

### 5. Dogfood The Loop

Start with short experiments:

- improve fast prompt
- improve JSON prompt
- add one eval case
- add one example
- improve one template

Do not start with broad theory edits.

## Why This Fits Luck

Luck's current binding constraint is adoption friction. Autoresearch directly attacks it by making improvement measurable and repetitive.

The compounding loop becomes:

1. Real work exposes a failure.
2. Failure becomes eval case or lint.
3. Runtime/template/example improves.
4. Selftest/eval verifies no regression.
5. Dogfood ledger records whether the intervention helped.

That is Luck applied to Luck.

## Initial Recommendation

Incorporate Karpathy autoresearch as Phase 8 of the aggressive roadmap, but start implementation now with:

1. program.md
2. experiments/results.tsv
3. bin/luck-eval
4. one logged baseline eval result

This gives us autonomous improvement infrastructure without overbuilding.
