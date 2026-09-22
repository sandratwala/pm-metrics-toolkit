# product-metrics-frameworks

A Claude skill that identifies **product metrics** (North Star + Pirate/AARRR and/or HEART) and **business metrics** from a PRD and a research report, the way a Senior PM would.

## What it does

Given a PRD (with Epics and Jobs To Be Done) and a research report (with Solution and Impact sections), the skill:

1. Identifies the main feature from the PRD's epics/JTBD.
2. Derives a **North Star Metric** with 3–5 input/driver metrics, grounded in the PRD.
3. Reads the feature's stated goals to decide whether **Pirate Metrics (AARRR)**, **HEART**, or both apply — rather than defaulting by product age.
4. Applies the selected framework(s) with specific, PRD-grounded metrics per category.
5. Derives 3–5 **business metrics** from the research report's Solution and Impact sections.

It requires both documents and will stop and ask if either is missing, rather than filling gaps from general PM knowledge.

## When it triggers

Any time both a PRD and a research report are provided and the user asks for product metrics, business metrics, a North Star metric, Pirate/AARRR or HEART metrics, or general PM-style metric analysis,even without naming the frameworks explicitly.

## Usage

Attach a PRD and a research report to a Claude conversation with this skill installed, and ask for a metrics breakdown (e.g. "What metrics should we track for this feature?").

## Credit / similar skills

This skill's core structure — a single North Star Metric feeding into framework-based sub-metrics — is a common pattern also used by:

- [`product-analytics`](https://agentskillsfinder.com/skills/product-analytics) (alirezarezvani) — defines KPIs and selects AARRR/North Star/HEART frameworks for dashboards, retention, and adoption analysis.
- [`metrics-framework`](https://vibeindex.ai/skills/assimovt/productskills/metrics-framework) (assimovt/productskills) — North Star metric + input/output metric tree + counter-metrics.
- [`north-star-metric`](https://claudemarketplaces.com/skills/phuryn/pm-skills/north-star-metric) (phuryn/pm-skills)
- [`metric-architecture`](https://skills.rest/skill/metric-architecture) (danielpradilla) — connects a North Star metric to actionable indicators with a business-stage-based framework recommendation.
- [`metrics-review`](https://skillselion.com/skills/anthropics/knowledge-work-plugins/metrics-review) (Anthropic, knowledge-work-plugins) — trend analysis and review cadence for existing metrics.

This skill differs from the above in two ways: (1) it selects AARRR vs. HEART based on **signals in the PRD's stated epics/JTBD** rather than product maturity or business stage, and (2) it derives business metrics strictly from a paired **research report's Solution/Impact sections**, rather than general business-stage heuristics — so every metric traces back to something explicitly stated in the input documents.

## Files in this folder

- `SKILL.md` — the skill definition.
- `examples/good-example/` — a sample run with both documents present.
- `examples/bad-example/` — a sample run with a required document missing, showing the correct refusal behavior.
- `quality-report/llm-judge-analysis.md` — LLM-as-judge evaluation of this skill per the assignment's skills-quality-scorer process.

