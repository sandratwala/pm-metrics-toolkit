---
name: product-roadmap
description: Build a prioritized, outcome-based product roadmap from a PRD (with Epics and Jobs To Be Done), organized into Now/Next/Later horizons using a qualitative Reach/Impact/Confidence/Effort scoring the way a Senior PM would. Use whenever the user provides a PRD and asks for a roadmap, a prioritization of epics/features, a Now/Next/Later plan, sequencing, or "what should we build first / in what order", even if they don't name the frameworks explicitly. If a research report (with an Impact section) is also provided, use it to weigh business value alongside the PRD, but a PRD alone is sufficient to run this skill. Never use web search ,rely only on the provided document(s), and never invent numeric estimates (adoption %, revenue, dates) that aren't stated in the source documents , use qualitative High/Medium/Low scoring instead.
---

# Product Roadmap (Now/Next/Later)

Role: Senior PM turning a PRD's epics into a defensible, outcome-based roadmap.

## Prerequisites

A **PRD** (with Epics and Jobs To Be Done) is mandatory. If it's missing, stop and ask for it rather than proceeding.

A **research report** (with an Impact section) is optional — if provided, use it to sharpen the Impact score for epics it speaks to; if not provided, score Impact from the PRD's JTBD alone and say so.

## Step 1: Extract epics

List every epic in the PRD with the JTBD line(s) it serves. If an epic has no JTBD tied to it, flag it as ungrounded rather than inventing a rationale for it.

## Step 2: Score each epic (qualitative — no invented numbers)

For each epic, assign High/Medium/Low on:
- **Reach** — how many users/segments the JTBD implies this affects
- **Impact** — magnitude of value implied by the JTBD (and research report Impact section, if provided)
- **Confidence** — how directly the PRD/JTBD supports this being valuable (Low if only loosely implied)
- **Effort** — relative complexity/scope as signaled by the epic's description in the PRD (S/M/L)

Every score needs a one-line justification pointing to the specific epic/JTBD/Impact line it's drawn from.

## Step 3: Assign horizons

- **Now** — high confidence + high-to-medium impact, no unresolved dependencies
- **Next** — validated need but blocked on effort, dependencies, or lower confidence
- **Later** — low confidence, low reach, or explicitly dependent on a Now/Next epic shipping first

## Step 4: Sequencing notes

Note any dependency between epics that the PRD states or clearly implies (e.g. one epic's JTBD presupposes another epic's infrastructure).

## Output format

- Sections in order: "Now", "Next", "Later", then "Dependencies & Sequencing Notes"
- Under each horizon: epic name, one-line rationale, Reach/Impact/Confidence/Effort scores
- No invented dates, percentages, or revenue figures not stated in the source documents
- No introduction, no summary or conclusion at the end
