# Testing Luck Runtime

Run the self-test:

    bin/luck-selftest

By default it uses qwen2.5:7b through Ollama for speed.

Use another model:

    LUCK_TEST_MODEL=qwen2.5:32b bin/luck-selftest

The self-test checks:

- bin/luck-check --help
- fast mode passes deterministic lint for constraint, failure mode, next test, defer/stop, brevity, and no taxonomy recitation
- JSON mode passes deterministic lint for required fields, enum compliance, scorecard shape, and concrete next test
- all context templates exist
- bin/luck-context lists modes and generates a workflow context

Lint a saved output directly:

    bin/luck-lint --mode fast --file /tmp/luck-fast.md
    bin/luck-lint --mode json --file /tmp/luck.json

Run the Verdict eval pack:

    verdict run -c verdict.yaml -p evals/luck-runtime-effectiveness.yaml

What to inspect:

- Does the answer name one binding constraint?
- Does it avoid walking through all seven checks by default?
- Does it define a concrete next test?
- Does it include what to defer or stop?

Run the autoresearch-style eval bundle:

    bin/luck-eval --quick

By default this uses qwen2.5:32b because JSON scorecard compliance is stricter than fast-mode smoke testing.

Run the fuller bundle:

    bin/luck-eval --full
