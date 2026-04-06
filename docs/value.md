# Value

## Definition

**Value** asks:

**Did this work create meaningful user or business benefit?**

In VISTA, value is not measured by code written, pull requests merged, tickets closed, or features released. Those are outputs. Value is about whether the work made a meaningful difference for customers, the business, or both.

## Why it matters

As AI makes software output cheaper and faster to produce, the risk is not that teams build too little. The risk is that they build more of the wrong things, or that they mistake shipped work for realized benefit.

Without an explicit value lens, organizations drift toward:
- delivery theater — celebrating releases instead of results
- feature accumulation — building more without evidence of benefit
- local optimization — improving parts that don't move the whole
- AI-generated slop — plausible-looking output that nobody asked for and nobody uses (see [glossary](#glossary) below)
- weak product focus — losing sight of who benefits and why

## What Value is not

Value is **not**:
- output volume
- engineering busyness
- implementation elegance alone
- how much code AI generated
- how quickly something shipped
- how loudly a stakeholder wanted it

## What Value includes

Value often includes:
- adoption by intended users
- repeat usage over time
- measurable movement in a target KPI
- customer trust or satisfaction improvement
- reduction in customer pain or friction
- revenue contribution or enablement
- retention, expansion, or churn reduction
- progress against a strategic objective

**Value is realized benefit, not delivered output.**

## Typical signals of strong Value

- intended users actually adopt it
- those users continue to use it over time
- the change improves an important user or business metric
- the feature becomes part of normal behavior
- the benefit is large enough to matter relative to alternatives

## Typical signals of weak Value

- a feature ships but usage remains low
- adoption exists, but repeat usage does not
- work is technically complete but creates little real-world traction
- users are confused about what it is for
- teams celebrate release activity without evidence of customer benefit

## Value and AI engineering

AI lowers the cost of producing outputs:
- more code
- more pull requests
- more experiments
- more backlog clearing

That can be helpful. But it also means organizations can create more low-value work faster than ever before.

## Questions Value should force

Before work starts:
- What user or business benefit should this create?
- For whom?
- How will we know if it worked?
- What would meaningful adoption look like?

After work ships:
- Did the intended users adopt it?
- Did they keep using it?
- Did it improve the metric or outcome we expected?
- Was the value large enough to matter?

## ODIM example for Value

- **Outcome:** Increase customer retention
- **Decision:** Which workflows or features should we improve first?
- **Insight:** Which behaviors or capabilities are associated with stronger retention?
- **Measure:** Adoption and repeat usage of those workflows by retained vs churned customers

## Concrete example

A team ships a workspace invite reminders feature. AI generated the code in hours. The PR merged cleanly. In a throughput-focused system, this looks like a win.

Three weeks later, the data shows: 14% of invited users clicked the reminder, but only 2% completed onboarding. Repeat usage is zero — the reminder fires once and is forgotten. Meanwhile, an onboarding flow improvement sat in the backlog that had strong evidence of reducing churn for users who *already* accepted invites.

The invite reminder scored well on speed and output. It scored poorly on Value because it didn't produce meaningful adoption or retention movement. A VISTA-informed system would have surfaced that gap before coding started by asking: *What does meaningful adoption look like for this feature?*

## Glossary

**AI-generated slop:** Code, features, or pull requests that are syntactically correct and superficially plausible but lack clear user benefit, strategic rationale, or evidence of demand. Slop is the predictable byproduct of optimizing for output volume without filtering for value. It consumes review capacity, clutters the product, and trains the organization to celebrate activity over outcomes.

---

Value asks whether the work actually mattered — not whether it shipped.
