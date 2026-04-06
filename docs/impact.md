# Impact

## Definition

**Impact** asks:

**Did this work materially advance strategic goals or competitive position?**

Value and Impact are related but distinct.

Value is measured at the **item level**: did this specific piece of work create benefit for users or the business?

Impact is measured at the **portfolio level**: did the set of choices the organization made — what to build, what to defer, what to kill — advance its strategic position?

A feature can score high on Value (users love it) and low on Impact (it doesn't strengthen the company's position in a target market). Conversely, a capability-building investment may show modest immediate Value but high Impact because it unlocks future competitive advantage.

## Why it matters

Strategy is not about whether an item sounds reasonable on its own.
Strategy is about comparative choice under constraint.

Impact helps answer:
- Does this strengthen a capability we need?
- Does this help us win where we are trying to win?
- Does this move us closer to a strategic objective?
- Is this more important than the alternatives?

## How to tell them apart

| | Value | Impact |
|---|---|---|
| **Level** | Individual work item | Portfolio of choices |
| **Question** | Did users benefit? | Did strategy advance? |
| **Timeframe** | Weeks after release | Quarter or longer |
| **Failure mode** | Shipped but unused | Useful but strategically irrelevant |
| **Example** | Invite reminders get 14% click rate | Enterprise SSO — table stakes for target segment — advances despite being less "exciting" |

**Impact is strategic consequence, not local usefulness.**

## What Impact includes

Impact often includes contributions to:
- strategic initiative progress
- capability-building for the future
- target market or segment traction
- competitive differentiation
- positioning strength
- company-level goal movement
- higher-quality choices about what gets done and when

## Typical signals of strong Impact

- work clearly maps to strategic goals
- completed work strengthens an important capability
- the change helps the company win in a target market
- the priority decision looks correct in hindsight
- engineering capacity is increasingly directed toward high-cost-of-delay work

## Typical signals of weak Impact

- many items can be justified as “important”
- teams cannot explain why one item should come before another
- work maps to vague goals but not to real tradeoffs
- completed work helps locally but does not strengthen position

## Questions Impact should force

Before work starts:
- What strategic objective does this help advance?
- What capability does this strengthen?
- How does this improve our position?
- What better competing option exists?
- Why is this above that option?

After release:
- Did this choice hold up in hindsight?
- Did it help move a strategic initiative?
- Did it strengthen a capability we needed?
- Was the cost-of-delay judgment correct?

## ODIM example for Impact

- **Outcome:** Improve win rate in a target market segment
- **Decision:** Which product capabilities should be prioritized first?
- **Insight:** Which capabilities most influence buying confidence and onboarding success in that segment?
- **Measure:** Adoption and strategic traction of segment-specific capabilities, plus hindsight quality of sequencing decisions

## Concrete example

Consider two items competing for the same sprint capacity:

1. **Pricing page experiment** — clear scope, strong customer signal, expected to improve conversion by ~3%.
2. **Enterprise SSO provisioning** — complex, security-sensitive, but required to close three enterprise deals in the pipeline.

The pricing page scores higher on immediate Value (fast win, measurable KPI lift). But SSO scores higher on Impact because the enterprise segment is a stated strategic priority and delays here have high cost of delay.

A system that only measures Value would always pick the pricing page. VISTA's Impact dimension surfaces the strategic cost of that choice.

---

Impact asks whether the work moved the company in the right direction — not just whether it helped locally.
