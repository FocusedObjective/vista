# Team Profiles

VISTA profiles are diagnostic patterns. They help teams recognize where they are and identify what to work on next.

These are not personality types. A team may shift between profiles as conditions change.

---

## Profile A: Fast but weak

**Signals:**

- High throughput — lots of PRs merged, features shipped
- Low review depth relative to risk
- Rising regressions and post-merge cleanup
- Weak adoption — features ship but users don't stick
- Poor strategic alignment — work doesn't map to goals

**What's happening:**

The team is optimizing for speed and volume. AI tools may be amplifying output without anyone checking whether that output connects to customer value. Review is treated as a gate to clear, not a judgment to make.

**What to do:**

- Introduce post-release value checks: is anyone using it? are they coming back?
- Require a one-sentence strategic rationale before work starts
- Match review depth to downside risk — stop rubber-stamping high-risk PRs
- Track regressions per shipped item, not just total regressions

---

## Profile B: Safe but stagnant

**Signals:**

- Low regressions — nothing breaks
- Strong review rigor on everything
- Low capacity on high-cost-of-delay work
- Weak strategic movement — important things aren't advancing
- Excessive caution on routine items

**What's happening:**

The team has learned to avoid failure, often from past incidents. But the same review intensity is applied to every change regardless of risk, which slows high-value work. Cost of delay is not factored into prioritization.

**What to do:**

- Classify changes by risk tier and match review depth accordingly
- Track capacity allocation: what percentage goes to high-cost-of-delay items?
- Run hindsight reviews on sequencing decisions quarterly
- Give routine changes a lighter review path so high-risk work gets the attention it needs

---

## Profile C: Busy but unfocused

**Signals:**

- Lots of work in motion simultaneously
- Many items labeled "urgent" or "high priority"
- Low prioritization clarity — teams can't explain why one item is above another
- Weak hindsight choice quality — decisions often look wrong in retrospect
- Stakeholder pressure dominates sequencing

**What's happening:**

The organization doesn't have a concrete enough strategy to drive tradeoffs. Everything sounds important, so everything gets started. Work-in-progress balloons, finish rates drop, and the loudest voice wins.

**What to do:**

- Force comparative choice: before starting any item, name what it displaces
- Limit concurrent priorities to a number the team can actually finish
- Apply cost-of-delay thinking: what happens if this waits two weeks?
- Require that strategy be specific enough to explain ordering, not just direction

---

## Profile D: Healthy system

**Signals:**

- High-priority work finishes at a strong rate
- No rise in hidden post-merge cost
- Review depth proportional to risk
- Repeated issue types cause fewer regressions over time
- Priority decisions hold up better in hindsight

**What's happening:**

The team is advancing strategy while managing risk well. They're learning from past patterns, routing review effort where it matters, and connecting work to real outcomes. AI tools increase throughput without increasing hidden cost.

**What to sustain:**

- Continue tracking hindsight quality — don't assume good results will persist
- Look for emerging blind spots: new kinds of risk that the current system doesn't catch
- Share learning mechanisms across teams
- Watch for signs of backsliding as pressure increases
