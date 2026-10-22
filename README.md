# Friction Finder
### A Lumora Strategy experiment in making work easier

**[Try the live prototype](https://levitatingsnake.github.io/Lumora-friction-finder/)**

Most teams know when a process is frustrating. Explaining *why* it is frustrating, and what to try instead, is harder.

Friction Finder turns a plain-English description of a workflow into a first-pass process map, possible sources of friction, simpler alternatives and small tests a team could run. It is designed for people who know their work but don't speak consultancy jargon.

## What the prototype does

1. **Describe the work.** Enter a workflow or try one of 53 example scenarios across five industry collections.
2. **See the current process.** The tool extracts a rough sequence of actions and labels possible waits and handoffs.
3. **Explore potential friction.** Transparent text-matching rules suggest issues worth investigating, prioritised by predefined impact categories.
4. **Consider alternatives.** Each suggestion explains a practical change, likely business implications and a caution.
5. **Run a small test.** The output proposes a starting action, an owner, a measure and a decision criterion. Findings can be copied.

## Why it exists

The design question was: **Could someone explain a messy process in everyday language and leave with one sensible experiment, without needing a consultant or a complicated dashboard?**

The prototype tests a human-centred approach to improvement:

**Possibility → Opportunity → Efficiency → Productivity**

Its underlying principle is to make the next useful decision clearer, not to automate human judgement.

## Technical approach

- Single-page website built with HTML, CSS and vanilla JavaScript.
- Hosted on GitHub Pages; no account or server required.
- Analysis runs in the browser using explicit keyword and regular-expression rules.
- No model API, external data retrieval or machine learning.
- The app does not send entered process descriptions to an application server. The page loads a Google Fonts stylesheet.
- Outputs are **hypotheses**, not a measured diagnosis, and savings are not fabricated.

The project deliberately uses an inspectable rules engine. It is an exercise in interaction design, workflow reasoning, practical recommendations and honest communication about uncertainty, **not** a claim to have built an autonomous AI system.

## Design choices

**Keep it approachable.** Use normal language, industry examples and a small set of result views rather than a technical cockpit.

**Start with the people doing the work.** When an owner cannot be inferred, the process map says so. Recommendations ask users to check assumptions with the team.

**Make advice testable.** A suggestion is more useful when it includes an owner, a first step, a measure and a reason to continue or stop.

**Protect important controls.** Advice involving safety, privacy, professional decisions or required approvals includes cautions.

## Current status and known limits

**Prototype, under quality review.**

- All 53 built-in scenarios have at least one specific advice-rule match. This is coverage, **not** evidence that every recommendation is relevant.
- Syntax checks and targeted rule checks have been performed. Comprehensive real-browser and accessibility testing is not yet complete.
- Process mapping uses simple sentence splitting, not language understanding. It can misidentify actors, omit steps or mistake a mention for a problem.
- Rule matching can produce false positives, miss important problems and favour familiar patterns.
- Priority is a heuristic, not a calculation of actual financial impact.
- No sensitive organisational or customer information should be entered into a public demonstration without appropriate authorisation.

See [the release review and manual test checklist](RELEASE_REVIEW.md) for the latest QA evidence.

## Next validation steps

- Walk through every result tab and control on mobile Safari and desktop browsers.
- Review representative scenarios with actual people who work in those processes.
- Measure whether users understand the output and can identify a useful first experiment.
- Record misleading recommendations and improve the engine based on evidence.

## Portfolio perspective

This project demonstrates product framing, human-centred interface design, a transparent decision-support prototype, and iterative quality improvement. The most important work is not the number of rules. It is turning an unclear business complaint into a question that can be investigated and tested.

Built under **Lumora Strategy**.

[Live prototype](https://levitatingsnake.github.io/Lumora-friction-finder/) · [Source repository](https://github.com/levitatingsnake/Lumora-friction-finder)
