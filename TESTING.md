# Testing Luck Runtime

Run the self-test:

    bin/luck-selftest

By default it uses qwen2.5:7b through Ollama for speed.

Use another model:

    LUCK_TEST_MODEL=qwen2.5:32b bin/luck-selftest

The self-test checks:

- bin/luck-check --help
- fast mode includes constraint, failure mode, and next test
- JSON mode returns the required scorecard shape
- all context templates exist

Run the Verdict eval pack:

    verdict run -c verdict.yaml -p evals/luck-runtime-effectiveness.yaml

What to inspect:

- Does the answer name one binding constraint?
- Does it avoid walking through all seven checks by default?
- Does it define a concrete next test?
- Does it include what to defer or stop?

