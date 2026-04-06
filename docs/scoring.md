# Scoring Template

This template structures thinking at three points: before coding, during review, and after release. It is not a bureaucratic checklist — it's a discipline for better decisions.

---

## Before coding

Rate each factor 1–5. Gates override scores.

| Factor | 1 (Low) | 3 (Moderate) | 5 (High) |
|--------|---------|--------------|----------|
| **Strategic relevance** | No clear link to any strategic initiative | Supports a strategic goal indirectly | Directly advances a top-3 priority |
| **Expected user/business value** | Speculative benefit, no evidence | Reasonable hypothesis with some signal | Strong evidence of demand or validated problem |
| **Cost of delay** | Can wait months with no consequence | Moderate competitive or learning cost from delay | Market window, dependency, or strategic harm from waiting |
| **Downside risk** | Easily reversible, low blast radius | Moderate scope, some users affected if wrong | Trust-sensitive, hard to reverse, broad user exposure |
| **Clarity/readiness** | Requirements unclear, many open questions | Mostly defined, a few unknowns remain | Well-scoped, acceptance criteria clear |
| **Verification readiness** | No test strategy, unclear how to validate | Partial coverage plan, some gaps | Clear verification plan, automated where appropriate |
| **Activation burden** | Ship it and done — no cross-functional work | Some docs, training, or rollout coordination needed | Requires sales enablement, support training, migration, or marketing |
| **AI suitability** | Requires deep domain judgment, high ambiguity | Parts can be AI-assisted with oversight | Well-defined, pattern-based, strong AI fit |

### Gates

Any item should be paused or rerouted if:

- Downside risk exceeds tolerance for the current team capacity
- Verification is too weak for the failure modes involved
- Clarity is too low to execute safely
- Required activation burden is unrealistic right now

**Weights decide preference. Gates decide permissibility.** A high-scoring item that fails a gate should not proceed until the gate condition is resolved.

### Forcing questions

1. What better competing option exists right now?
2. Why is this above that option?
3. What would make this safer or clearer first?
4. What non-dev work is required to realize value?
5. If this slips two weeks, what strategic harm occurs?

---

## During review

| Factor | What to assess |
|--------|----------------|
| **Review depth needed** | Does this PR warrant a quick scan, a careful read, or a deep walkthrough? |
| **Evidence strength** | Are there tests, screenshots, or data that demonstrate correctness? |
| **Rollback sensitivity** | If this breaks, how hard is it to undo? |
| **Trust/compliance sensitivity** | Does this touch user data, payments, security, or regulated areas? |
| **Hidden complexity** | Is the diff size misleading? Are there non-obvious side effects? |
| **Pattern similarity** | Have we seen this type of change cause problems before? |

### Forcing questions

1. What type of failure is most likely here?
2. What evidence would catch it?
3. Have we seen this pattern fail before?
4. What reusable guidance should come from this review?

---

## After release

| Factor | What to assess |
|--------|----------------|
| **Regressions** | Did anything break? What was the blast radius? |
| **Adoption** | Did intended users find and use it? |
| **Repeat usage** | Did they come back, or was it a one-time interaction? |
| **Strategic movement** | Did it advance the initiative it was meant to advance? |
| **Follow-on cleanup** | How much hidden work did it create post-merge? |
| **Trust/satisfaction** | Did it build confidence or erode it? |

### Forcing questions

1. Was a better option available that we didn't choose?
2. What did we underestimate?
3. Did value actually materialize, or did we just ship?
4. Did the review level match the true risk?
5. What should change for future similar items?

---

## Measure timing categories

Different measures serve different moments. Mix them or you'll only see the past.

| Category | When used | Examples |
|----------|-----------|---------|
| **Leading** | Before work starts | Cost of delay, strategic alignment, risk profile, verification readiness |
| **In-flight** | During coding and review | Churn, review depth vs risk, emerging complexity, rollout burden changes |
| **Lagging** | After release | Adoption, repeat usage, regressions, strategic progress |
| **Learning** | Across patterns over time | Repeated issue classes getting safer, review guidance reuse, better AI routing |
