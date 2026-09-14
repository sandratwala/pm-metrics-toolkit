# Product Metrics Frameworks

A skill that identifies product metrics from a PRD the way a Senior PM would — using the North Star Metric framework, plus either Pirate Metrics (AARRR) or HEART depending on whether the product is new or already existing.

## What it does

1. Reads a PRD's Epics and Jobs To Be Done to find the main feature.
2. Derives a North Star Metric (with driver metrics and rationale) for that feature — always included.
3. Infers from the PRD's own language whether the product is new or existing (no need to tell it which).
4. Adds exactly one second framework based on that inference:
   - **New product → Pirate Metrics (AARRR)**: Acquisition, Activation, Retention, Referral, Revenue
   - **Existing product → HEART**: Happiness, Engagement, Adoption, Retention, Task Success
5. Outputs just the two framework sections — no intro, no summary, no filler.

## Requirements

- A PRD document (containing Epics and Jobs To Be Done) is **mandatory**. If none is attached, the skill stops and asks for it rather than guessing.
- The skill relies only on the content of the provided document(s) — it never uses web search to fill in metrics.
- Every metric it produces should trace back to something explicitly in the PRD (an epic, a JTBD, or a stated goal), not generic PM boilerplate.

## How product status is decided

The skill looks for signals in the PRD text itself:

| Signal type | Example language |
|---|---|
| New product | "launch," "MVP," "greenfield," "0 to 1," no existing user base mentioned |
| Existing product | "current users," "redesign," "migrate," references to existing metrics/dashboards/versions |

If the PRD is ambiguous, it defaults to "existing" (the safer assumption) and notes the inference in the section header rather than as separate commentary.

## Output shape

Always exactly two sections:

1. **North Star Metric Framework**
2. **Pirate Metrics Framework (AARRR)** *or* **HEART Framework** (never both)

No introduction or conclusion text — just the two sections with concise, PRD-grounded bullet points.

## Usage

Attach a PRD and ask something like:
- "Identify the product metrics for this PRD as a Senior PM would."
- "What's the North Star metric and the right growth framework for this?"
- "Run a HEART/AARRR analysis on this PRD."

## Status

Drafted and not yet run against a real PRD — validate against an actual document before relying on it for coursework or client work.