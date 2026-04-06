# Software Development Performance Index (SDPI)

**Author:** Larry Maccherone
**Reference:** [Quantifying the Impact of Agile](https://www.infoq.com/articles/quantifying-impact-agile/) (InfoQ)

---

## What SDPI is

The Software Development Performance Index is a multi-dimensional framework for measuring software development performance. Rather than reducing performance to a single number or a narrow set of throughput metrics, SDPI defines several dimensions that together represent a more complete picture of how well a team or organization is performing.

Maccherone's core insight: **no single metric captures software development performance.** A team can score well on speed while accumulating hidden quality or predictability debt. Meaningful measurement requires looking at multiple dimensions simultaneously.

## Connection to VISTA

SDPI directly influenced VISTA in two ways.

**Multi-dimensional measurement.** VISTA's five-dimension structure — Value, Impact, Safety, Timing, Adaptation — follows the same principle that SDPI established: performance is not reducible to one axis. Different dimensions can move independently, and optimizing one at the expense of others produces misleading results.

**ODIM.** Larry Maccherone's **Outcome, Decision, Insight, Measure** framework is used directly in VISTA as the primary method for designing metrics that connect to business outcomes. ODIM ensures that every measure traces back through an insight and a decision to a real outcome — preventing the accumulation of orphan metrics that track activity without connecting to value.

## What VISTA changes

SDPI was designed for the pre-AI era of software development. VISTA extends the multi-dimensional approach into an environment where:

- AI-generated output is abundant and cheap
- The constraint has shifted from production to judgment
- Review, verification, and activation costs dominate delivery cost
- Security and safety risks scale with output volume
- Learning and adaptation matter more when change is faster
