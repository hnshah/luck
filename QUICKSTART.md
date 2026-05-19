# Luck Quickstart

Use Luck when the question is not "can this be done?" but "will this survive, spread, and compound?"

## 1. Prepare Context

Use a template from templates/ or paste rough notes with goal, current constraint, active demand, adoption path, maintenance burden, what repeats, what success makes easier next, and known friction.

## 2. Run A Check

Fast mode:

    bin/luck-check --name "My workflow" --file templates/workflow.md --mode fast

Standard mode:

    bin/luck-check --name "My repo" --file templates/repo.md

Full scan:

    bin/luck-check --name "Product idea" --file templates/product.md --mode full

JSON scorecard:

    bin/luck-check --name "Strategy choice" --file templates/strategy.md --mode json --output result.json

Default model: qwen2.5:32b through Ollama.

## 3. Carry Forward Three Lines

For actual work, carry forward only:

- Luck constraint
- Failure mode
- Next test

If those three lines do not change what you do next, the assessment is not useful enough.

## 4. Use The Result

- Repo feedback: turn the next test into an issue or PR.
- Workflow design: remove the manual rescue point first.
- Strategy: do the move that changes the binding constraint.
- Product: reduce adoption friction before adding more surface area.

## 5. Recheck After Intervention

After the next test, rerun Luck and ask:

- Did the binding constraint change?
- Did the failure mode become less likely?
- Did this create more viable next steps?

## Test The Install

    bin/luck-selftest

## Dogfood A Real Project

    bin/luck-log --project luck --name "Luck itself" --file dogfood/luck-context.md
    bin/luck-recheck --project luck
