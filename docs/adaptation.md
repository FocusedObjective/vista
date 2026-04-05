# Adaptation

## Definition

**Adaptation** asks:

**Is the system learning and improving over time?**

This is the dimension that turns VISTA from a reporting framework into a performance improvement framework.

A system that only measures outputs or incidents can tell you what happened.
A system with Adaptation can tell you whether it is getting better.

## Why it matters

Many organizations collect:
- delivery metrics
- incident reports
- review comments
- postmortems
- bug histories

But they do not reliably convert those into:
- better future prioritization
- better review depth choices
- better AI routing decisions
- fewer repeated regressions
- more reusable review guidance

A useful shorthand is:

**Adaptation is evidence that the system is improving its judgment, not just recording its history.**

## Typical signals of strong Adaptation

- repeated issue types cause fewer regressions over time
- similar risky PRs produce fewer downstream problems
- review patterns become more targeted and more effective
- teams get better at predicting which work will create value
- lessons are reused, not merely documented

## Typical signals of weak Adaptation

- the same mistakes recur across projects or teams
- postmortems produce no visible process improvement
- review comments are not reused as guidance
- risky change patterns continue to surprise the organization

## Questions Adaptation should force

Across time:
- Are repeated issue types becoming safer?
- Are similar PR patterns getting better review treatment?
- Are value predictions improving?
- Are opportunity-cost errors being caught earlier?
- Are we learning what AI should and should not do?

## ODIM example for Adaptation

- **Outcome:** Reduce repeated engineering mistakes and improve future decision quality
- **Decision:** How should similar future work be reviewed, routed, or reshaped?
- **Insight:** Which patterns repeatedly create regressions, weak value, or hidden cleanup?
- **Measure:** Repeated issue-class regression rate, known preventable pattern recurrence, and reuse of review guidance

## Summary

Adaptation is the dimension that asks whether the system is actually learning.

**VISTA uses Adaptation to measure whether engineering and product systems are getting smarter over time, not just busier.**
