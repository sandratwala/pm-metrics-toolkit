# Reflection

**What's the next step with automation, from this exercise?**

The biggest gap this exercise exposed is verification: the skill can produce a well-structured, well-cited metrics breakdown, but nothing currently checks that breakdown against reality — e.g. whether the "North Star" it picked actually correlates with retention or revenue once real data comes in. The natural next step is closing that loop: wiring the skill's output into an MCP connection to an actual analytics source (Amplitude, Mixpanel, a warehouse) so the metrics it proposes can be back-tested against historical data automatically, rather than just judged for internal consistency by another LLM.

**What else did you learn doing this assignment?**

Grounding constraints (stop and ask if a required document is missing; trace every output line back to a stated input) do more for output quality than adding more instructions to the prompt. The failure mode for a PM-metrics skill isn't "not knowing enough PM theory" — it's confidently inventing plausible-sounding metrics that aren't actually supported by the documents in front of it. Writing the bad-example case (missing research report) surfaced that risk more clearly than writing the good-example case did.
