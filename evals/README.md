# Luck Runtime Evals

Use this pack to check whether Luck Runtime produces useful operational advice instead of framework performance.

With Verdict installed locally:

    verdict run -c verdict.yaml -p evals/luck-runtime-effectiveness.yaml

What to inspect:

- Does the answer name one binding constraint?
- Does it avoid walking through all seven checks?
- Does it define a concrete next test?
- Does it say what to defer or stop?

The pack is intentionally small. Its job is to catch the common regression: models displaying the Luck vocabulary without changing the next move.

