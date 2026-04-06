# Dashboards

A VISTA implementation should start lean. These three dashboard views give different audiences the signals they need.

---

## Executive dashboard

Five flagship measures — one per dimension.

| Dimension | Measure |
|-----------|---------|
| **Value** | % of delivered work with meaningful adoption and repeat usage |
| **Impact** | % of completed work that materially advanced a strategic initiative |
| **Safety** | Regressions + follow-on cleanup burden per shipped item |
| **Timing** | % of engineering capacity spent on high-cost-of-delay work |
| **Adaptation** | Repeated issue types causing fewer regressions over time |

These are intentionally lagging. Executive dashboards should show whether the system is producing the right results, not micro-manage how it gets there.

---

## Delivery leadership dashboard

These measures help engineering managers and directors make structural improvements.

- Review depth matched to risk (are high-risk PRs getting deep review?)
- Verification effectiveness by work type (which categories still surprise us?)
- Activation burden discovered late (how often do we find non-dev dependencies after coding is done?)
- Hindsight quality of priority decisions (did our sequencing choices hold up?)
- Post-merge issue trends by pattern (are the same failure types recurring?)

---

## Team dashboard

These measures help individual teams improve their own judgment.

- Outcome clarity before start (did we know what success looked like before coding?)
- Review depth vs PR risk (are we reviewing proportionally?)
- Similar issue safety trend (are repeated issue types getting safer?)
- Opportunity-cost errors caught early (did we spot better alternatives before committing?)
- Reusable review guidance created (are we turning reviews into future leverage?)
