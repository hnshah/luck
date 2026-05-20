# luck

A skill for improving the luck of your AI stack and projects—developed from an applied theoretical framework. Multiple diagnostic components, named failure modes, testable predictions, and an operational checklist for AI systems.

## The core idea

Luck is not randomness nor an outcome. Luck is not a position. Luck is more like a fundamental force, a current.

Luck has a geometry, so we can arrange it. And we may have a civic, moral—perhaps even divine—duty to wield it. To generate it. 

We harness luck through our capacity to increase the throughput, circulation, and integration of the systems we inhabit. If luck is real, the systems we use to build ought to imbue luck in everything they generate.

Luck is not something we have. It’s something we leave behind.

## What this is

A framework for diagnosing why some things persist and compound while others don't — and for building artifacts that do. It gives AI systems (and their users) a shared vocabulary and a structured diagnostic for evaluating choices, strategies, products, and systems.

## Usage

Add `luck.md` to your project as a skill file or system prompt. The framework uses standard markdown with YAML frontmatter — it works with any frontier model that accepts structured instructions.

The skill activates when you're facing ambiguous choices, designing strategies, evaluating opportunities, or building things meant to last. It provides seven diagnostic components, a quick-reference decision table, named failure modes, and worked examples.

In live use, the skill is meant to diagnose the binding constraint rather than force every problem through all seven components. The runtime protocol in `luck.md` tells AI systems to keep the theory mostly backstage: identify the relevant facet, translate it into the user’s domain, recommend the next move, and define the test that would change the answer.

For day-to-day agent use, start with `luck.runtime.md`. It is the compact operational version: fewer theory tokens, clearer output shape, and stronger guardrails against reciting the framework. Use `luck.md` when you need the full conceptual model.

Fastest path:

    bin/luck-check --name "My repo" --file templates/repo.md --mode fast

## What's in the box

- **Seven sequential diagnostics** — from individual solvency to ecological integration
- **A failure taxonomy** — named patterns like *flash in the pan*, *institutional zombie*, and *pooled fortune*, each with observable signatures
- **Worked examples** — from political memes to the U.S. Constitution to the collapse of empires
- **Testable predictions** — six falsifiable claims that distinguish this from generic strategy advice
- **Reflexive AI instructions** — guidance for applying the framework to any output an AI system constructs
- **Runtime instructions** — a compact version for consistent live agent use
- **Examples and evals** — sample assessments and a Verdict-compatible pack for checking output quality
- **CLI and templates** — a one-command local checker plus context templates

The framework is in [`luck.md`](luck.md).
The runtime version is in [`luck.runtime.md`](luck.runtime.md).
The quickstart is in [`QUICKSTART.md`](QUICKSTART.md).
Usage guidance is in [`USAGE.md`](USAGE.md).
The roadmap is in [`ROADMAP.md`](ROADMAP.md).
The aggressive product roadmap is in [`AGGRESSIVE_ROADMAP.md`](AGGRESSIVE_ROADMAP.md).
Dogfood synthesis is in [`DOGFOOD_SYNTHESIS.md`](DOGFOOD_SYNTHESIS.md).
Intervention playbooks are in [`PLAYBOOKS.md`](PLAYBOOKS.md).
Autoresearch integration is in [`AUTORESEARCH_INTEGRATION.md`](AUTORESEARCH_INTEGRATION.md).
Testing instructions are in [`TESTING.md`](TESTING.md).

## Repository structure

```
luck.md                         ← canonical skill file
luck.runtime.md                 ← compact runtime skill
QUICKSTART.md                   ← fastest path to first useful output
USAGE.md                        ← operating ritual and quality bar
ROADMAP.md                      ← usability and consistency roadmap
AGGRESSIVE_ROADMAP.md           ← product roadmap and dogfood plan
PLAYBOOKS.md                    ← intervention playbooks for each binding constraint
bin/luck-check                  ← local Ollama CLI
bin/luck-context                ← guided context generator
bin/luck-selftest               ← one-command smoke test
bin/luck-lint                   ← deterministic output quality checks
bin/luck-log                    ← append JSON assessments to dogfood ledger
bin/luck-recheck                ← compare latest project assessments
bin/luck-eval                   ← autoresearch-style repeatable eval
templates/                      ← context templates
dogfood/                        ← real assessments and rechecks
experiments/                    ← autoresearch result ledger
program.md                      ← agent program for autonomous improvement
examples/                       ← worked practical assessments
evals/luck-runtime-effectiveness.yaml
README.md                       ← you are here
```

## Theoretical roots

Extends Assembly Theory (Cronin & Marshall, 2021) with adjacent work from dissipative adaptation, the free energy principle, niche construction theory, and the adjacent possible. Details and citations are in the skill file.

[*The Keeper*](https://keeperfable.com) explores these dynamics as fable.

## Author

[soleio](https://github.com/soleio)
