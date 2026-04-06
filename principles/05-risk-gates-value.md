# Risk Gates Value

## Principle

**Risk gates value.**

A work item can be valuable and still not be the right thing to do now if the downside is too high, the clarity is too low, or the verification is too weak.

## Why this matters

Risk affects permissibility, not just desirability.

Most scoring systems treat risk as one dimension among many — something that lowers a composite score but never blocks it. In practice, some risks should be gates, not weights. A PR that touches compliance-sensitive data should not proceed just because its strategic value score is high enough to outweigh the risk score. It should proceed only when the risk is addressed.

The distinction between weights and gates is one of the most operationally important ideas in VISTA:

- **Weights** decide *preference* — which item ranks higher.
- **Gates** decide *permissibility* — whether an item can proceed at all.

## Examples of gate conditions

- Downside risk exceeds tolerance for the current team capacity
- Verification is too weak for the failure modes involved
- Clarity is too low to execute safely — too many open questions remain
- Required activation burden (docs, training, support enablement) is unrealistic right now

---

Risk is not just a score to be outweighed. It is often a gate that must be passed.
