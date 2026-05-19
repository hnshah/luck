---
name: luck-runtime
description: "A compact runtime version of Luck for AI agents. Use for strategy, repo feedback, workflow design, opportunity evaluation, and diagnosing whether something will persist, compound, or fade."
metadata:
  author: hnshah
  source: soleio/luck
  version: "0.1"
---

# Luck Runtime

Luck means increasing the number and quality of viable next steps for a person, project, or system.

Use this file when the user is facing an ambiguous choice, evaluating a product or workflow, designing a system, or asking why something will persist, compound, or fade.

Do not recite the theory. Use the framework backstage to identify the binding constraint and next test.

## The Seven Checks

Assess in this order. Earlier failures dominate later strengths.

1. Solvency - can it survive without constant rescue?
2. Demand coupling - does it connect to a real, active need?
3. Adoption friction - can people actually adopt and use it?
4. Compounding loop - does success make future success easier?
5. Circulation - does value move through the system and return, or get stuck?
6. Integration - does it connect into a broader ecosystem?
7. Timing - is this the right sequence and moment?

## Plain-Language Translation

Use the user's domain language instead of abstract terms when possible:

| Luck term | Plain-language examples |
|---|---|
| Solvency | runway, maintainer capacity, operational slack, upkeep cost |
| Demand coupling | active pain, budget, urgency, repeated pull |
| Adoption friction | setup friction, behavior change, integration cost, learning curve |
| Compounding loop | usage creates data, trust, distribution, templates, infrastructure |
| Circulation | knowledge reuse, money reinvestment, feedback loops, contributor flow |
| Integration | ecosystem fit, standards, APIs, workflows, handoffs |
| Timing | prerequisites, sequencing, market readiness, window state |

## Failure Modes

Use one when it clarifies the risk:

- Flash in the pan - excitement without retention or compounding.
- Heroic treadmill - works only through unsustainable manual effort.
- Extractive mirage - local metrics improve while the system decays.
- Institutional zombie - maintained by inertia, not live demand.
- Fragmented ecology - strong parts, weak handoffs and weak whole.
- Timing trap - right idea, wrong sequence or missing prerequisites.

## Runtime Protocol

Default behavior:

1. Inspect concrete context first.
2. Identify the one binding constraint.
3. Mention only the checks that change the decision.
4. Translate concepts into the user's domain language.
5. Recommend what to do now, what to defer, and what evidence would change the answer.
6. End with the next test.

Avoid:

- Walking through all seven checks when a shorter diagnosis is enough.
- Using Luck vocabulary to sound profound while leaving the next move unclear.
- Giving timing advice when the real problem is solvency.
- Talking about moats before adoption works.

## Standard Output

Use this shape for full assessments:

## Luck Assessment: [thing]

### Verdict
- [Durable / Promising but fragile / Likely temporary / Do not pursue]

### Binding Constraint
- [One sentence]

### Why
- [2-4 bullets using only the relevant checks]

### Failure Mode To Avoid
- [Named failure mode] - [plain-language reason]

### Next Test
- [Concrete experiment, artifact, metric, or decision checkpoint]

### What To Do Now
1. Do now: [Highest-leverage move]
2. Do next: [Second move]
3. Defer/stop: [What to defer or stop]

## Fast Output

Use this shape when the user needs speed:

- Luck constraint: [one line]
- Failure mode: [one line]
- Next test: [one line]
- Do now / do next / defer: [one line]
