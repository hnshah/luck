# Crazy Egg CRO Workflow Context

## Goal

Make CRO audits reliably produce useful V3 reports, redesigned pages, and deployable outputs with minimal expert rescue.

## Trigger

Hiten sends a site URL for a CRO audit or five-second test.

## Inputs

Original URL, screenshots, extracted page text, brand system, qwen analysis, audit JSON, redesign HTML, QA checks, and deployment.

## Output

A deployed audit with a 7-fix V3 report, a branded redesigned homepage, quality gates passed, and a run report documenting what happened.

## Current Steps

The workflow captures screenshots, verifies the real business through fetched text, runs qwen3:235b text-only analysis, converts the analysis into JSON, generates the report, builds a branded redesign, runs QA, and deploys to Cloudflare Pages.

## Manual Rescue Points

The weak points are JSON creation from analysis, applying all fixes in redesigns, validating visual polish across mobile and desktop, fallback handling when local models fail, and making sure lessons from each audit become reusable checks instead of chat memory.

## Active Demand

There is repeated demand for Crazy Egg audits. The system already has validated model choices, screenshot playbooks, QA scripts, and deployed examples.

## Maintenance Burden

Quality still depends on an expert operator remembering the current workflow, reading the right examples, checking validation, and updating memory after failures.

## Compounding Loop

Each audit should create reusable QA rules, better templates, stronger redesign patterns, citation improvements, and documented failure prevention.

## Circulation

Run learnings are scattered across MEMORY.md, daily logs, scripts, and audit folders. The system improves when those learnings flow into scripts, validators, templates, and pre-flight checks.

## Integration

The workflow connects OpenClaw, local Ollama models, browser automation, Playwright-style capture, templates, Cloudflare Pages, and long-term memory.

## Known Failure

Heroic treadmill: high-quality audits keep shipping, but only because a senior operator remembers hidden steps and catches silent failures.
