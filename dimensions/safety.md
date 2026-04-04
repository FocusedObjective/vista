# Safety

## Definition

**Safety** asks:

**Did this work avoid hidden downside and hold up in reality?**

In VISTA, Safety is broader than defect prevention alone. It includes:

- regressions
- escaped defects
- rollback burden
- review and verification effectiveness
- privacy and security implications
- trust-sensitive failures
- hidden post-merge cost
- operational fragility
- follow-on cleanup and stabilization work

Safety exists because software success is not just about getting work shipped. It is about getting the right work shipped **without creating disproportionate harm, fragility, or cleanup cost**.

---

## Why it matters

As AI makes implementation faster, one of the biggest risks is that teams optimize coding speed while underestimating:

- review burden
- verification complexity
- hidden edge cases
- rollout effort
- privacy implications
- security and trust concerns
- post-merge cleanup

A change that ships quickly but creates instability is not a clear win.
A feature that lands but requires disproportionate follow-on work is not obviously cheap.
A code change that passes basic tests but harms privacy, trust, or maintainability is not “safe enough.”

Safety is what helps teams see the real delivery cost, not just the visible engineering motion.

---

## The core idea

A useful shorthand is:

**Safety is the ability to move without creating disproportionate downside.**

That downside can be technical, operational, business, customer-facing, legal, privacy-related, or reputational.

---

## Why Safety must include more than bugs

Traditional engineering thinking often reduces safety to defect rates and uptime. Those still matter, but they are not enough.

In AI-assisted engineering, Safety also includes whether the organization has responsibly managed:

- verification strength
- review depth
- blast radius
- reversibility
- privacy and data handling
- security consequences
- customer trust implications
- hidden operational costs

AI may generate plausible code quickly. That does not mean it has fully reasoned through:
- privacy implications
- trust boundaries
- product confusion
- operational load
- rollout risk
- subtle business rules

That is why Safety must stay broad.

---

## Safety and privacy

Security and privacy deserve explicit attention inside Safety.

A team can produce code that is technically functional and even relatively secure in obvious ways, while still missing:
- over-collection of customer data
- weak privacy boundaries
- poor retention logic
- accidental exposure risk
- inappropriate logging
- misuse of sensitive information
- product behavior that undermines user trust

In other words:

**AI can help generate secure-looking systems while still missing privacy, trust, and governance implications.**

Safety should make those visible.

---

## Typical signals of strong Safety

Indicators of strong Safety include:

- similar risky changes cause fewer post-merge problems over time
- regressions stay low relative to throughput
- review depth is proportionate to risk and impact
- verification strength matches downside severity
- rollback and recovery burden are manageable
- privacy and security concerns are identified early
- hidden post-merge cleanup stays controlled
- teams know which patterns need deeper scrutiny

Strong Safety does not mean the organization becomes slow and fearful.
It means the organization moves with proportional caution and proportional confidence.

---

## Typical signals of weak Safety

Indicators of weak Safety include:

- throughput rises while regressions rise
- review speed is optimized without regard to review quality
- hidden cleanup grows after merge
- the same classes of issue recur
- verification is thin relative to downside risk
- privacy and security concerns are discovered late
- activation and support burdens are underestimated
- teams treat “it passed tests” as sufficient evidence

One of the most revealing weak-safety patterns is:
**more visible delivery gains paired with growing hidden post-merge cost.**

---

## Common anti-patterns

### 1. Fast review vanity
Review speed is celebrated even when risky PRs still produce preventable post-merge failures.

### 2. Test-passing complacency
Passing tests is treated as proof that the work is ready, even when broader risk remains.

### 3. Hidden cleanup blindness
Follow-on work, support load, and stabilization effort are ignored in delivery assessment.

### 4. Security-only safety
Security concerns are considered, but privacy, trust, and product harm are not.

### 5. Uniform review treatment
Low-risk and high-risk changes get similar review patterns, wasting effort in one place and under-investing in another.

---

## Questions Safety should force

Before coding:
- What is the downside if this goes wrong?
- How reversible is it?
- What evidence would make this safe enough?
- What privacy or trust concerns could arise?
- Is this AI-suitable given the risk?

During review:
- Is review depth matched to the true risk?
- Is verification strong enough for the likely failure modes?
- Have we seen this pattern fail before?
- What failure would hurt most here?

After release:
- Did it work without regressions?
- What hidden cleanup did it create?
- Did review and verification match the actual risk?
- Were privacy, trust, or security issues missed?
- What should future similar items do differently?

---

## Suggested measures

Examples include:

- regression rate by change type
- escaped defect severity
- rollback frequency and rollback cost
- hidden post-merge cleanup effort
- support burden created per shipped item
- review depth vs risk classification
- verification effectiveness by work type
- privacy/security issues discovered before vs after release
- recurrence rate of known risky issue patterns
- customer trust incident rate

The strongest safety measures often connect to patterns over time, not just individual incidents.

---

## ODIM example for Safety

- **Outcome:** Fewer customer-impacting regressions and trust incidents
- **Decision:** Which changes require deeper review and stronger verification?
- **Insight:** Which kinds of changes, PR patterns, or data-handling scenarios create the most downstream problems?
- **Measure:** Regression rate, trust-sensitive issue rate, and post-merge cleanup burden by change type

This is powerful because it ties safety measures directly to review and verification decisions.

---

## What good looks like

A team with a strong Safety discipline:

- adjusts review depth to risk
- treats privacy and security as part of safe delivery
- recognizes hidden post-merge cost as a real delivery cost
- reduces repeated failure patterns over time
- uses evidence to choose appropriate caution
- does not confuse speed with readiness

A good Safety discipline does not try to eliminate all risk.
It tries to make risk visible, proportional, and responsibly managed.

---

## Summary

Safety is the dimension that asks whether the work was delivered without creating disproportionate hidden downside.

It protects teams from confusing movement with readiness, and helps organizations account for the full delivery cost: not just coding, but review, verification, privacy, trust, cleanup, and stability.

**VISTA uses Safety to measure whether engineering is moving responsibly, not just moving quickly.**
