---
name: product-metrics-frameworks
description: Identify product metrics from a PRD document (Epics, Jobs To Be Done) the way a Senior PM would — derive the North Star Metric for the main feature, then infer from the PRD whether the product is new or already existing and apply the matching second framework: Pirate Metrics (AARRR) for new products, or HEART for existing products. Use this whenever the user provides a PRD and asks to identify product metrics, a North Star metric, Pirate/AARRR metrics, or HEART metrics, or asks for PM-style metric analysis of a document — even if they don't name the frameworks explicitly. Requires a PRD document as mandatory input; if none is attached, stop and ask for it rather than proceeding. Never use web search — rely only on the provided document(s).
---

# Product Metrics Frameworks (North Star + Pirate/HEART)

Role: Senior PM analyzing a PRD to identify the right product metrics.

## Prerequisite

A PRD document (with Epics and Jobs To Be Done) is mandatory. If none has been provided or uploaded, stop and ask the user to attach it before doing anything else. Do not substitute general knowledge or web search for the PRD's content — every metric produced must trace back to something stated in the document (an epic, a JTBD, a stated goal).

## Step 1: Read the PRD

Extract the Epics and Jobs To Be Done. Identify the **main feature** — the feature that best represents the primary user/business value, usually the headline epic or the one the most JTBD tie back to.

## Step 2: North Star Metric framework (always included)

For the main feature, define:
- **North Star Metric** — the single metric that best captures the core value the main feature delivers to users, tied to long-term business value.
- **Input/driver metrics** — 3–5 metrics that feed into the North Star Metric.
- **Rationale** — one or two sentences, grounded in the PRD's stated epics/JTBD, on why this metric was chosen.

## Step 3: Infer product status (new vs. existing)

Decide automatically from the PRD content — do not ask the user.

- **New product signals**: language like "launch," "MVP," "greenfield," "new product," "0 to 1"; no mention of an existing user base, current metrics, or a legacy system.
- **Existing product signals**: language like "current users," "existing product," "redesign," "migrate," "improve retention/engagement of current...," references to existing metrics, dashboards, or version numbers.

If the signal is genuinely ambiguous, default to treating it as an existing product (the safer assumption), and note the inference briefly in the section header rather than as separate filler text — e.g. "HEART Framework (inferred as an existing product based on references to a redesign)".

## Step 4: Apply the matching second framework

Only one of these two runs per analysis — never both.

**If new → Pirate Metrics (AARRR).** Give specific metrics for the main feature under each stage:
- Acquisition
- Activation
- Retention
- Referral
- Revenue

**If existing → HEART.** Give specific metrics for the main feature under each category:
- Happiness
- Engagement
- Adoption
- Retention
- Task Success

## Output format

- Exactly two sections: "North Star Metric Framework" and either "Pirate Metrics Framework (AARRR)" or "HEART Framework" — whichever applies.
- No introduction, no "Here's the analysis...," no summary or conclusion at the end.
- Concise bullet points under each metric/stage. Don't pad with generic PM boilerplate that isn't grounded in the PRD.