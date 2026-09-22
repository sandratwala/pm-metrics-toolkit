# product-roadmap

A Claude skill that turns a PRD's epics and Jobs To Be Done into a prioritized, outcome-based roadmap (Now/Next/Later), the way a Senior PM would.

## What it does

Given a PRD (with Epics and JTBD), and optionally a research report:

1. Extracts every epic and the JTBD it serves — flags any epic with no grounding.
2. Scores each epic qualitatively on Reach, Impact, Confidence, and Effort — each score justified by a specific line in the source documents, never invented.
3. Assigns each epic to **Now**, **Next**, or **Later** based on those scores.
4. Notes dependencies between epics where the PRD states or clearly implies them.

It requires a PRD and will stop and ask if it's missing. A research report is optional and only sharpens the Impact score when present.

## When it triggers

Any time a PRD is provided and the user asks for a roadmap, prioritization, sequencing, a Now/Next/Later plan, or "what should we build first" — even without naming the framework.

## Usage

Attach a PRD (and optionally a research report) to a Claude conversation with this skill installed, and ask for a roadmap or prioritization.

## Credit / similar skills

The Now/Next/Later structure and impact/effort-based prioritization is a well-established PM pattern also used by:

- [`roadmap-planning`](https://claudeskills.info/ja/skills/deanpeters/Product-Manager-Skills/roadmap-planning/) (deanpeters/Product-Manager-Skills) — a multi-phase workflow covering OKR gathering, epic hypotheses, impact/effort/strategic-fit prioritization, and Now/Next/Later or quarterly sequencing.
- [`roadmap-management`](https://claudemarketplaces.com/skills/anthropics/knowledge-work-plugins/roadmap-management) (Anthropic, knowledge-work-plugins) — handles roadmap planning via Now/Next/Later and Quarterly Themes frameworks.
- `roadmap-planning` (assimovt/productskills) — outcome-based roadmaps using Now/Next/Later horizons organized by problems to solve rather than feature lists.

This skill differs in scope and grounding: it works from a single PRD's epics/JTBD (rather than orchestrating a multi-week, multi-phase stakeholder process), uses strictly qualitative High/Medium/Low scoring instead of numeric RICE-style estimates, and explicitly refuses to invent reach/impact numbers not stated in the source documents — every score line must cite the PRD/JTBD/Impact line it's drawn from.

## Files in this folder

- `SKILL.md` — the skill definition.
- `examples/good-example/` — a sample run against a PRD with clear epics/JTBD.
- `examples/bad-example/` — a sample run with no PRD provided, showing the correct refusal.
- `quality-report/llm-judge-analysis.md` — LLM-as-judge evaluation of this skill.

