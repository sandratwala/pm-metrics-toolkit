# LLM-as-Judge Analysis: product-metrics-frameworks

Evaluated against the good-example and bad-example runs in `../examples/`.

## Scoring

| Criterion | Score (/5) | Notes |
|---|---|---|
| Trigger clarity | 5 | Frontmatter description names exact trigger conditions (PRD + research report present, PM-metric request) without requiring the user to name frameworks explicitly. |
| Groundedness | 5 | Every metric in the good-example output traces to a specific epic, JTBD line, or Solution/Impact sentence — no generic PM boilerplate metrics were introduced. |
| Prerequisite enforcement | 5 | Bad-example run correctly stops and names the *specific* missing document instead of guessing or falling back to general knowledge. |
| Framework-selection judgment | 4 | Correctly identified AARRR-only fit from growth/funnel signals and explained why HEART was skipped, per Step 3's instruction to skip ungrounded categories. Docked one point: the skill doesn't give the model an explicit tie-breaker for genuinely 50/50 mixed signals beyond "apply both." |
| Output format compliance | 5 | Matched the required section order (North Star → selected framework(s) → Business Metrics) with no added intro/conclusion, per Step 6. |
| Robustness to ambiguity | 4 | Handles a clearly single-feature PRD well; less tested is a PRD with multiple competing "main feature" candidates — worth a second test case before final submission. |

**Overall: 28/30**

## Strengths
- Hard requirement to stop on missing input prevents hallucinated business metrics — the single biggest risk for this skill type.
- Framework selection is evidence-based (Step 3) rather than a fixed template, so it adapts to what the PRD actually emphasizes.

## Suggested improvement before submission
- Add one more test case: a PRD where epics split evenly between growth and usability signals, to confirm the "apply both frameworks" branch degrades gracefully (each category present only where grounded, per Step 3's last bullet).
