# Decision Model

## Why VISTA needs a decision model

VISTA is not just a reporting framework. It is a framework for making better choices about engineering work when AI makes output abundant and judgment becomes the constraint.

## The central problem

The central problem is not simply:

**Is this work item good?**

The harder question is:

**Is this the right work to do now, compared with the alternatives, given the value, strategy, risk, timing, and activation realities we face?**

## The VISTA decision rule

**The right next item is the one with the best timing-adjusted strategic upside, subject to acceptable downside risk, sufficient clarity, and realistic verification and activation readiness.**

### What "timing-adjusted" means in practice

Two items may both score high on strategic value. The adjustment for timing asks: *what happens if each one waits?*

Consider a team choosing between:

| | Enterprise SSO (AUTH-184) | Pricing page experiment (WEB-216) |
|---|---|---|
| **Strategic value** | High - required for enterprise segment | Moderate - expected 3% conversion lift |
| **Cost of delay** | High - three deals waiting, one at risk of slipping to next quarter | Low - no deadline, conversion rate is stable |
| **Downside risk** | High - security-sensitive, compliance implications | Low - shallow blast radius, easily reversible |
| **Clarity** | Medium - some discovery gaps remain | High - well-scoped A/B test |
| **Verification readiness** | Low - needs security review protocol | High - automated test coverage exists |

Raw value scores might put these items close together. The timing adjustment separates them: SSO's delay carries measurable strategic harm (lost deals), while the pricing experiment's delay costs almost nothing.

But SSO also hits two gates: downside risk is high and verification readiness is low. The decision rule doesn't say "do SSO immediately." It says "SSO has the highest timing-adjusted upside *subject to* acceptable risk and verification." The right action might be: start discovery and security review planning for SSO now, while the pricing experiment executes in parallel on an AI-first path.

This is the decision rule at work - not a formula that produces a single number, but a structured way to think about comparative choice under constraint.

## The three layers of the model

### Layer 1: Should we do this?
Pre-start decision making - assess and route.

### Layer 2: How should we do this?
Execution, review, and verification shaping - match the approach to the work.

### Layer 3: Was it worth it?
Post-merge and post-release evaluation - close the feedback loop.

## Layer 1: Should we do this?

Score the work across these dimensions before coding starts:

- **Strategic relevance** - How directly does this advance a current roadmap theme?
- **Expected customer value** - What user benefit should this create, and what's the evidence?
- **Cost of delay** - What strategic harm occurs if this waits?
- **Downside risk** - What's the blast radius if this goes wrong?
- **Clarity and readiness** - Are requirements, acceptance criteria, and scope well-defined?
- **Verification readiness** - Do test paths, coverage plans, and rollback strategies exist?
- **Activation burden** - What non-dev work is required to realize value? (See [glossary](#glossary) below.)
- **AI suitability** - Is this bounded and pattern-based enough for AI-first execution, or does it require human judgment?

### Weights vs gates

**Weights** express preference - they determine which item ranks higher.
**Gates** express permissibility - they determine whether an item can proceed at all.

**Weights decide preference. Gates decide permissibility.**

An item may be paused or rerouted if:

- Downside risk exceeds tolerance for the team's current capacity
- Verification is too weak for the failure modes involved
- Clarity is too low to execute safely
- Activation burden is unrealistic right now

A high-scoring item that fails a gate should not proceed until the gate condition is resolved.

### Execution lanes

Assessment leads to routing. Based on the scores and gates, work moves into one of several execution lanes:

| Lane | When to use | Example |
|------|------------|---------|
| **AI-first** | Bounded scope, high historical similarity, strong verification, low blast radius | Workspace invite reminders (APP-331) |
| **AI with guardrails** | Clear scope but needs manual review checkpoints | Pricing page experiment (WEB-216) |
| **Human review first** | Cross-cutting concerns, compliance implications, trust-sensitive areas | Audit export retention (API-092) |
| **Needs discovery** | Security-sensitive, verification gaps remain, ambiguity is high | Enterprise SSO provisioning (AUTH-184) |

The lane is not a permanent label. Work can move between lanes as clarity improves or risk is resolved.

## Layer 2: How should we do this?

Once work is approved and routed, shape the execution approach:

- **Review depth** - Does this PR warrant a quick scan, a careful read, or a deep walkthrough?
- **Verification strength** - What test paths, coverage, and evidence are required?
- **Rollback sensitivity** - If this breaks, how hard is it to undo?
- **Privacy and trust sensitivity** - Does this touch user data, payments, or regulated areas?
- **Change surface and blast radius** - How many files, modules, and service boundaries are affected?
- **Known failure pattern similarity** - Have similar changes caused problems before?
- **Reversibility** - Can this be reverted in minutes, hours, or never?
- **AI involvement and oversight needs** - What level of human oversight does the AI-generated code require?

In practice, this means PR review should not be FIFO. PRs should be prioritized by delivery value and risk - high-value, high-risk PRs reviewed first, low-risk housekeeping batched or deferred.

## Layer 3: Was it worth it?

After release, close the feedback loop:

- **Regressions and hidden post-merge cost** - Did anything break? What follow-on cleanup did it create?
- **Adoption and repeat usage** - Did intended users find it and keep using it?
- **Strategic movement** - Did it advance the initiative it was meant to advance?
- **Trust and satisfaction impact** - Did it build confidence or erode it?
- **Activation success** - Did the non-dev dependencies (docs, training, support, marketing) actually happen?
- **Hindsight quality of the priority choice** - Knowing what we know now, was this the right thing to do next?
- **Reusable learning created** - What can future work learn from this delivery?

This layer feeds back into Layer 1. Delivery outcomes sharpen future assessments.

## How VISTA handles uncertainty

VISTA does not pretend to eliminate judgment. It exists because judgment is required.

That means:
- Thresholds vary by context - a startup and a healthcare company have different risk tolerances
- Gate conditions are team-specific - what counts as "sufficient verification" depends on the domain
- Weights shift with business context - when a customer escalation lands, customer value goes up; when a release is days away, verification readiness dominates

Interactive weighting - adjusting dimension emphasis in real time and watching rankings reorder - makes these tradeoffs visible instead of implicit.

## How VISTA relates to other frameworks

VISTA is not a replacement for DORA, SPACE, or DevEx. It is a complement.

| Framework | What it measures | VISTA's relationship |
|-----------|-----------------|---------------------|
| **DORA** | Deployment frequency, lead time, change failure rate, recovery time | DORA measures **flow** - how fast and reliably work moves through the pipeline. VISTA adds **direction** - whether that flow carried the right work. |
| **SPACE** | Satisfaction, Performance, Activity, Communication, Efficiency | SPACE measures **developer experience** across multiple dimensions. VISTA shares the multi-dimensional philosophy but focuses on **organizational outcomes** rather than individual developer experience. |
| **DevEx** | Developer friction, cognitive load, flow state | DevEx measures **how it feels to build**. VISTA measures **whether what was built mattered**. |

A team can score well on DORA (fast deploys, low failure rate) and poorly on VISTA (deploying the wrong things quickly). A team can have great DevEx scores (low friction, good flow) while building features nobody uses. VISTA adds the outcome layer that these frameworks intentionally leave out.

## VISTA anti-patterns

VISTA itself can be misused. Watch for these failure modes:

- **Analysis paralysis** - Spending more time scoring work than doing work. VISTA should make decisions faster, not slower. If scoring takes longer than a brief conversation, the process is too heavy.
- **Score gaming** - Teams inflating strategic relevance or cost-of-delay scores to get their preferred work approved. Counter this with hindsight reviews: do the predictions hold up after delivery?
- **Bureaucratic overhead** - Requiring full VISTA scoring for every small change. Routine, low-risk work should move through lightweight paths. Reserve deep assessment for work with real strategic stakes or downside risk.
- **Weaponizing metrics** - Using VISTA scores as individual performance measures. VISTA measures system outcomes, not individual productivity. Using it to rank engineers will destroy trust and produce gaming.
- **Premature precision** - Treating 1-5 scores as calibrated measurements. They are structured judgment aids, not exact quantities. A score of 4 vs 3 is a conversation prompt, not a verdict.

## Glossary

**Activation burden:** The non-development work required to realize value from a shipped change. This includes documentation, sales enablement, support team training, customer migration, marketing communication, and operational readiness. A feature that ships with zero activation burden (deploy and done) is rare. Most require cross-functional follow-through that is invisible to engineering metrics but essential to outcomes. When activation burden is high and unplanned, value never materializes - the code works, but nobody knows it exists or how to use it.

**Blast radius:** The scope of impact if a change fails - how many users, services, or systems are affected. A narrow blast radius (one UI component, one user segment) means failure is contained. A wide blast radius (cross-service data migration, public API change) means failure cascades.

**Change surface:** The files, modules, and service boundaries a change touches. Related to blast radius but focused on the code side: how widely does this change reach into the codebase? Wide change surfaces increase review burden and hidden interaction risk.

**Cost of delay:** The strategic harm caused by not doing this work now. Not all delay is equally costly - some work can wait months with no consequence, while other work loses market position, customer trust, or competitive advantage with every week of delay.

---

The goal is not perfect certainty. The goal is better judgment under constraint.
