# Safety

## Definition

**Safety** asks:

**Did this work avoid hidden downside, including security failures, and hold up in reality?**

In VISTA, Safety is broader than defect prevention alone. It explicitly includes security alongside quality, privacy, resilience, and trust. It includes:
- regressions
- escaped defects
- security vulnerabilities and control failures
- rollback burden
- review and verification effectiveness
- privacy and security implications
- trust-sensitive failures
- hidden post-merge cost

## Why it matters

As AI makes implementation faster, one of the biggest risks is that teams optimize coding speed while underestimating:
- review burden
- verification complexity
- hidden edge cases
- rollout effort
- security exposure
- privacy implications
- security and trust concerns
- post-merge cleanup

**Safety is the ability to move without creating disproportionate downside, including security downside.**

Two related concepts from delivery engineering:

- **Blast radius** — how many files, modules, services, or users a change touches. Wide blast radius demands more scrutiny.
- **Change surface** — the scope of code and system boundaries affected. A one-file UI tweak and a cross-service data migration have very different change surfaces even if both are "medium" PRs by line count.

## Safety, security, and privacy

Security and privacy deserve explicit attention inside Safety.

AI may generate plausible code quickly. That does not mean it has fully reasoned through:
- authentication and authorization gaps
- data exposure paths
- privacy implications
- trust boundaries
- product confusion
- operational load
- rollout risk
- subtle business rules

## Typical signals of strong Safety

- similar risky changes cause fewer post-merge problems over time
- regressions stay low relative to throughput
- review depth is proportionate to risk and impact
- verification strength matches downside severity
- privacy and security concerns are identified early and validated before release

## Typical signals of weak Safety

- throughput rises while regressions rise
- throughput rises while security findings or incident escapes rise
- review speed is optimized without regard to review quality
- hidden cleanup grows after merge
- verification is thin relative to downside risk
- privacy and security concerns are discovered late

## Questions Safety should force

Before coding:
- What is the downside if this goes wrong?
- How reversible is it?
- What evidence would make this safe enough?
- What security, privacy, or trust concerns could arise?

During review:
- Is review depth matched to the true risk?
- Is verification strong enough for the likely failure modes?
- Are the relevant security controls and trust boundaries actually enforced?
- Have we seen this pattern fail before?

After release:
- Did it work without regressions?
- What hidden cleanup did it create?
- Were security, privacy, or trust issues missed?

## ODIM example for Safety

- **Outcome:** Fewer customer-impacting regressions, security incidents, and trust failures
- **Decision:** Which changes require deeper review and stronger verification?
- **Insight:** Which kinds of changes, PR patterns, or data-handling scenarios create the most downstream security and reliability problems?
- **Measure:** Regression rate, security issue rate, trust-sensitive issue rate, and post-merge cleanup burden by change type

## Concrete example

An AI agent generates a PR for audit export retention (API-092). The diff is 180 lines — "medium" by size. But the change crosses data policy boundaries, touches compliance-sensitive retention rules, weakens an access-control assumption, and affects an API used by external integrations.

A throughput-focused system treats this as a medium PR and routes it through standard review. A VISTA-informed system flags the high blast radius, the compliance sensitivity, the security sensitivity, and the weak verification path — and routes it to human review first, with explicit acceptance criteria for the retention policy and access controls.

The cost of catching this *during* review is one hour. The cost of catching it in production — after a customer's audit data is silently dropped — is weeks of incident response and a trust discussion with legal.

---

Safety asks whether the work was delivered without creating disproportionate hidden downside, including hidden security downside.
