# Dogfood Ledger

This directory records real Luck assessments.

The point is not to collect pretty outputs. The point is to see whether Luck changes decisions and whether interventions change binding constraints.

## Log An Assessment

    bin/luck-log --project luck --name "Luck itself" --file dogfood/luck-context.md

## Recheck A Project

After an intervention, log another assessment:

    bin/luck-log --project luck --name "Luck itself after quickstart" --file dogfood/luck-context.md --phase recheck --intervention "Added CLI and selftest"

Then compare:

    bin/luck-recheck --project luck

## What Matters

- Did the binding constraint change?
- Did the failure mode become less likely?
- Did the next test get sharper?
- Did the work create more viable next steps?

