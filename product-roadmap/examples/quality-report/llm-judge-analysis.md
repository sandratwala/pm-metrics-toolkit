# LLM-as-Judge Analysis: product-roadmap

Evaluated against the good-example and bad-example runs in `../examples/`.

## Scoring

| Criterion | Score (/5) | Notes |
|---|---|---|
| Trigger clarity | 5 | Description names concrete trigger phrases (roadmap, prioritization, sequencing, Now/Next/Later, "what should we build first") without requiring exact framework names. |
| Groundedness | 5 | Every Reach/Impact/Confidence/Effort score in the good-example cites the specific JTBD or epic line it's drawn from; Epic 3 is correctly flagged as ungrounded rather than assigned a confident score. |
| Prerequisite enforcement | 5 | Bad-example correctly stops on a missing PRD and clarifies the research report is optional, not required. |
| Numeric-invention guardrail | 5 | Skill explicitly forbids invented percentages/dates/revenue and enforces qualitative High/Medium/Low scoring instead — the good-example output has zero invented numbers. |
| Horizon-assignment judgment | 4 | Correctly separated "blocked on confidence" (Epic 3 → Later) from "blocked on effort/dependency" (would be → Next) per Step 3. Docked one point: with only 3 epics the Next bucket ended up empty, so this test case doesn't fully exercise the Now/Next distinction — worth a second test with more epics before final submission. |
| Output format compliance | 5 | Matches required section order (Now → Next → Later → Dependencies) with no intro/conclusion. |

**Overall: 29/30**

## Strengths
- The refusal to assign numeric scores without source grounding is the strongest safeguard here — it's the same failure mode (confident invention) the metrics skill guards against, applied to a different output shape.
- Flagging an epic as "ungrounded" (Epic 3) rather than silently scoring it like the others is a meaningful quality signal a plain prioritization prompt wouldn't produce.

## Suggested improvement before submission
- Test against a PRD with 5+ epics and at least one genuine effort/dependency block, to confirm the Next horizon populates correctly and isn't just an artifact of a small example.
