---
name: product-metrics-frameworks
description: Identify both product and business metrics from a PRD and a research report the way a Senior PM would. For product metrics — derive the North Star Metric for the main feature, then select whichever framework(s) (Pirate Metrics/AARRR, HEART, or both) best fit that feature's stated goals and JTBD, rather than defaulting by product age. For business metrics — derive them from the research report's Solution and Impact sections. Use this whenever the user provides a PRD and/or research report and asks to identify product metrics, business metrics, a North Star metric, Pirate/AARRR metrics, HEART metrics, or asks for PM-style metric analysis of a document — even if they don't name the frameworks explicitly. Requires BOTH a PRD (with Epics and Jobs To Be Done) and a research report (with Solution and Impact sections) as mandatory input; if either is missing, stop and ask for the missing one(s) rather than proceeding. Never use web search — rely only on the provided document(s).
---

# Product Metrics Frameworks (North Star + Pirate/HEART + Business Metrics)

Role: Senior PM analyzing a PRD and a research report to identify product and business metrics.

## Prerequisites

Two documents are mandatory:
- A **PRD** (with Epics and Jobs To Be Done) — needed for the product metrics (North Star + framework).
- A **research report** (with Solution and Impact sections) — needed for business metrics.

If either is missing, stop and ask the user to attach it — name specifically which one(s) are missing. Do not substitute general knowledge or web search for either document's content — every metric produced must trace back to something stated in the documents (an epic, a JTBD, a line in the Solution/Impact sections).

## Step 1: Read the PRD

Extract the Epics and Jobs To Be Done. Identify the **main feature** — the feature that best represents the primary user/business value, usually the headline epic or the one the most JTBD tie back to.

## Step 2: North Star Metric framework (always included)

For the main feature, define:
- **North Star Metric** — the single metric that best captures the core value the main feature delivers to users, tied to long-term business value.
- **Input/driver metrics** — 3–5 metrics that feed into the North Star Metric.
- **Rationale** — one or two sentences, grounded in the PRD's stated epics/JTBD, on why this metric was chosen.

## Step 3: Select the right product framework(s) from feature signals

Do not infer "new vs. existing product." Instead, read what the main feature's epics/JTBD are actually optimizing for, and select based on fit:

- **Growth/funnel signals** — acquiring users, converting signups, first-time activation, referral loops, monetization — point to **Pirate Metrics (AARRR)**.
- **Experience/quality signals** — usability, satisfaction, task completion, engagement depth, retention of usage — point to **HEART**.
- If the PRD's stated goals for the feature mix both concerns, apply **both frameworks** — but only include categories directly supported by something stated in the PRD. Skip a category rather than padding it with generic metrics it isn't grounded in.
- If signals are genuinely unclear, default to **HEART** (broadest fit for most features) and note the inference briefly in the section header — e.g. "HEART Framework (inferred — PRD emphasizes usability over growth)".

## Step 4: Apply the selected framework(s)

For each framework selected in Step 3, give specific metrics for the main feature under each of its categories:

- **Pirate Metrics (AARRR)**: Acquisition, Activation, Retention, Referral, Revenue
- **HEART**: Happiness, Engagement, Adoption, Retention, Task Success

If both are selected, present them as two separate sections rather than merging categories.

## Step 5: Business metrics (from the research report)

Read the **Solution** and **Impact** sections of the research report. Derive business metrics that connect the feature to business outcomes (revenue, cost, efficiency, market share, etc.), grounded in what's stated there.

- Give 3–5 business metrics.
- **Rationale** for each — one line, grounded in the Solution/Impact content.

## Output format

- Sections, in order: "North Star Metric Framework", then the selected product framework section(s) ("Pirate Metrics Framework (AARRR)" and/or "HEART Framework"), then "Business Metrics".
- No introduction, no "Here's the analysis...," no summary or conclusion at the end.
- Concise bullet points under each metric/stage/category. Don't pad with generic PM boilerplate that isn't grounded in the documents.