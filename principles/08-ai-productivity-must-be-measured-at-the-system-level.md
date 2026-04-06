# AI Productivity Must Be Measured at the System Level

## Principle

**AI productivity must be measured at the system level.**

If AI increases code output but also increases review burden, hidden cleanup, product confusion, or low-value work, the system may not actually be improving.

## Why this matters

Measuring AI productivity by output volume — lines of code generated, PRs created, backlog items cleared — misses the costs that show up elsewhere in the system:

- More PRs means more review burden. If review capacity doesn't scale, quality drops or queues grow.
- Faster coding means less natural thinking time. Design decisions that used to happen during implementation now need to happen before it.
- Higher volume means more opportunities for AI-generated slop — code that is syntactically correct but strategically pointless.
- Post-merge cleanup, regressions, and follow-on work may rise even as cycle time falls.

The right question is not "did AI help us produce more?" It's "did AI help us produce *better results* with *better tradeoffs* across the full delivery system?"

## What system-level measurement looks like

Instead of:
- Lines of code generated
- PRs merged per week
- Backlog velocity

Measure:
- Value delivered per unit of total delivery effort (including review, verification, and activation)
- Regression rate relative to throughput
- Adoption and repeat usage of shipped features
- Review burden per PR by lane (AI-first vs human-shaped)
- Hidden post-merge cost trends

---

AI productivity is a whole-system question. Measuring it at the point of code generation is like measuring a factory's efficiency by counting how fast the assembly line moves — without checking how many finished products actually work.
