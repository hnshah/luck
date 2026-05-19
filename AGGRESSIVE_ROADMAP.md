# Aggressive Roadmap: Our Luck

## North Star

Luck becomes the diagnostic layer we use before and after serious work.

It should answer four questions better than a smart general-purpose model:

1. What is the binding constraint?
2. What failure mode are we drifting toward?
3. What should we do now, next, and defer?
4. Did the intervention increase viable next steps?

The product is not a philosophy file. The product is a repeatable loop:

Context -> Luck diagnosis -> Work plan -> Intervention -> Recheck -> Learning captured

## Opinionated Product Shape

Our Luck should become five things:

1. Runtime skill: short, sharp instructions agents can use without taxonomy dumping.
2. CLI: one-command checks, JSON scorecards, selftests.
3. Pattern library: real examples that teach the framework by use case.
4. Eval harness: proves the runtime beats baseline and catches regressions.
5. Dogfood ledger: tracks real decisions, constraints, interventions, and whether they changed.

## What It Should Do

### Diagnose

Given a repo, workflow, product idea, strategy choice, or personal decision, Luck should produce:

- verdict
- binding constraint
- failure mode
- next test
- do now / do next / defer
- optional seven-check scorecard
- confidence and missing evidence

### Track

Luck should store assessments so we can compare over time:

- initial constraint
- intervention
- recheck constraint
- whether the system became more solvent, adoptable, compounding, circulating, or integrated

### Teach

Luck should improve users as they use it:

- explain why the constraint is the constraint
- show weak-answer contrast
- link to closest examples
- ask for missing context when input is thin

### Integrate

Luck should live inside actual workflows:

- repo reviews
- CRO audit system improvements
- OpenClaw skill design
- Verdict eval/product work
- strategy choices
- workflow rescue/refactor decisions

### Evaluate

Luck should be continuously tested:

- does it avoid reciting all seven checks?
- does it identify the correct binding constraint?
- does it sequence actions correctly?
- does it define a concrete next test?
- does it name what to defer?
- does it outperform baseline prompts?

## Roadmap

### Phase 0 - Baseline Already Shipped

Status: done.

Built:

- luck.runtime.md
- bin/luck-check
- bin/luck-selftest
- QUICKSTART.md
- USAGE.md
- TESTING.md
- templates/
- examples/
- evals/luck-runtime-effectiveness.yaml

Validated:

- help path
- fast mode
- JSON scorecard mode
- templates present
- Verdict eval dry-run
- local qwen runs

### Phase 1 - Make It Useful On Real Work

Goal: dogfood on real work immediately.

Build:

- dogfood/ledger.jsonl
- dogfood/README.md
- bin/luck-log: append a Luck assessment to the ledger
- bin/luck-recheck: compare a new assessment to an earlier one
- dogfood templates for "before intervention" and "after intervention"

Dogfood targets:

1. Verdict adoption path
2. Crazy Egg CRO audit system
3. OpenClaw skills quality
4. Luck itself
5. Local model stack

Success criteria:

- 5 real assessments logged
- 2 rechecks after interventions
- at least 1 decision changes because of Luck
- at least 1 workflow improvement is made from a Luck diagnosis

### Phase 2 - Pattern Library That Teaches

Goal: examples become the primary onboarding path.

Add 12 examples:

1. repo adoption
2. workflow heroic treadmill
3. AI marketplace timing
4. community knowledge circulation
5. SaaS onboarding adoption friction
6. founder fundraising timing
7. product feature prioritization
8. local model stack solvency
9. agency/reporting workflow circulation
10. open-source maintainer burnout
11. personal career optionality
12. content/distribution compounding loop

Each example includes:

- context
- strong Luck answer
- weak generic answer
- why the binding constraint is correct
- intervention
- recheck criteria

Success criteria:

- examples cover every failure mode
- examples cover every one of the seven checks as a binding constraint
- qwen2.5:7b improves when examples are included in prompt context

### Phase 3 - Eval Harness With Teeth

Goal: make quality measurable.

Build:

- 20-case Verdict pack
- paired baseline vs luck.runtime pack
- scorer/lint script for deterministic failures
- evals/results/ with latest run summaries
- regression command: bin/luck-eval

Deterministic lint checks:

- missing binding constraint
- missing next test
- missing defer/stop
- lists all seven checks in fast mode
- too many abstract terms
- no domain-language translation
- no concrete action verb
- JSON schema failure

Success criteria:

- runtime beats baseline on qwen2.5:7b, qwen2.5:32b, and one frontier model
- fast mode stays under 180 output tokens median
- JSON mode schema pass rate >= 95%
- no-framework-performance rate >= 90%

### Phase 4 - Better Context Capture

Goal: improve assessments by improving inputs.

Build:

- bin/luck-context: guided context generator
- template-specific prompts
- missing-evidence detection
- confidence scoring
- "ask these 3 questions first" output when context is too thin

Modes:

- repo
- workflow
- product
- strategy
- personal
- skill
- audit-system

Success criteria:

- thin-context assessments identify missing evidence instead of hallucinating certainty
- users can generate usable context in under 5 minutes
- dogfood assessments get more specific over time

### Phase 5 - Skill Packaging

Goal: installable and portable.

Build:

- OpenClaw/Codex skill package
- Claude/ChatGPT copy-paste runtime
- README install paths
- versioned runtime files
- changelog

Success criteria:

- can install as a local skill
- can run CLI without remembering repo paths
- runtime version is visible in every assessment
- selftest verifies install

### Phase 6 - Intervention Playbooks

Goal: Luck does not stop at diagnosis.

For each binding constraint, create intervention playbooks:

- Solvency: reduce maintenance, increase margin, remove rescue points
- Demand coupling: find sharper pull, test urgency, narrow audience
- Adoption friction: first-run path, templates, defaults, integration
- Compounding loop: make every use create reusable assets
- Circulation: move knowledge/value back into the system
- Integration: connect to standards/workflows/ecosystems
- Timing: sequence prerequisites, wait/build/partner

Each playbook includes:

- symptoms
- first fix
- anti-patterns
- next test
- examples
- metrics

Success criteria:

- every assessment can point to a playbook
- playbooks reduce generic recommendations
- interventions become reusable across projects

### Phase 7 - Luck Memory And Dashboard

Goal: see compounding over time.

Build:

- assessment ledger browser
- constraint trend summaries
- repeated failure mode alerts
- project-level history
- "what did Luck improve?" report

Success criteria:

- we can see our most common constraint across projects
- we can see whether interventions changed constraints
- we can identify repeated heroic treadmill patterns before they burn us

## Dogfood Plan

### Dogfood 1: Luck Itself

Question: Is Luck becoming a usable operating system or just a better doc set?

Run:

- bin/luck-check on the Luck repo in full mode
- log result
- implement one intervention
- recheck

Expected current constraint: adoption friction or compounding loop.

### Dogfood 2: Verdict

Question: What is the next move to make Verdict adoptable?

Run:

- feed README, first-run path, our prior fixes, and eval results
- produce scorecard
- convert next test into a concrete change

Expected current constraint: adoption friction.

### Dogfood 3: Crazy Egg CRO Audit System

Question: Are audit learnings circulating back into the system?

Run:

- feed workflow docs, run reports, QA gates
- assess whether one-off work compounds
- add one system-learning capture point

Expected current constraint: circulation.

### Dogfood 4: OpenClaw Skills

Question: Which skills are living tools vs static prompt documents?

Run:

- sample 5 skills
- assess each in JSON mode
- identify common failure mode

Expected current constraint: integration or circulation.

### Dogfood 5: Local Model Stack

Question: Is model usage solvent and repeatable, or dependent on memory?

Run:

- feed MEMORY model stack and scripts
- assess repeatability
- create one routing/default improvement

Expected current constraint: integration.

## Next 48 Hours

1. Build dogfood ledger.
2. Add bin/luck-log.
3. Add bin/luck-recheck.
4. Run Dogfood 1 on Luck itself.
5. Implement the first intervention from Dogfood 1.
6. Recheck Luck.
7. Run Dogfood 2 on Verdict.
8. Add two examples from the dogfood runs.
9. Expand eval pack to 10 cases.
10. Commit results.

## Non-Negotiables

- Default output must be short.
- Every output must name what to defer or stop.
- Every output must define a next test.
- Full seven-check scans are opt-in.
- JSON mode must stay schema-valid.
- Dogfood results must be recorded.
- If Luck does not change the next action, it failed.

## The Bet

The aggressive version of Luck is not "a framework for thinking."

It is a system for increasing the rate at which our work becomes more durable, adoptable, compounding, circulating, and integrated.

