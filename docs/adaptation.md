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

## How learning actually happens

Adaptation requires infrastructure, not just intention. Concrete mechanisms include:

- **Closed-loop feedback from delivery outcomes.** When work ships, capture what happened: review friction, rework cycles, regressions, scope sprawl, follow-on work. Feed that evidence back into how similar future work gets assessed and routed.
- **Similar-work pattern matching.** When a new issue or PR arrives, surface prior items with overlapping file paths, module boundaries, or label patterns. If those prior items triggered rework or repeat feedback, flag it before anyone repeats the same review.
- **Review guidance reuse.** Turn recurring review comments into persistent checklists that surface automatically for similar future changes, instead of relying on individual reviewers to remember.
- **Lane accuracy tracking.** Track whether work routed to AI-first execution actually delivered clean results, or whether it needed human rescue. If a lane consistently produces rework, the routing criteria need recalibration.

## Concrete example

A team notices that changes touching the notification subsystem have triggered regressions in three of the last five sprints. In a non-learning system, each incident produces a postmortem that says "add more tests." Nothing structurally changes.

In a system with Adaptation, the pattern is captured: notification-subsystem changes carry elevated risk. Future PRs touching those files automatically get flagged for deeper review and stronger verification. Over the next quarter, the regression rate for that subsystem drops from 60% to 15%. That decline *is* the adaptation signal.

---

Adaptation asks whether the system is actually learning — not just accumulating history.
