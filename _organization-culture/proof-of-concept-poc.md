---
title: Proof of Concept (POC)
description: Before fully committing to a solution that can significantly affect the future, build as mall prototype to demonstrate viability and gain a better understanding
layout: pattern
---

![Proof of Concept (POC)]({{ site.baseurl }}/assets/images/proof%20of%20concept.png)

You have run experiments and identified a solution path that you think could be the right one, but there are still some big unknowns. You are at a decision point: adopt this solution, or not?

## In This Context

Once some initial experiments have uncovered a likely transformation path, it is time to test it. Committing to it right now could, if it is wrong, cause large problems and expense as the initiative continues.

You simply don’t know enough to make a large commitment at this point. Any full commitment right now carries massive risk because switching to an alternative later will be very difficult. Adopting a solution you don’t fully understand too early in the process compounds the risk, because you will continue to build further functionality on top of this solution.

- Hands-on work, rather than promises or explanations, is better for demonstrating value to skeptics.
- Changing early decisions is costly in the later stages of a migration project.

## Therefore

Build a basic functional prototype to demonstrate the viability of a solution.Define the questions that need answers before starting the PoC and stop the workonce the questions are answered.

- This should take a few days to a few weeks.
- Build the most primitive version you can get away with. Be ready to throw it away when you are finished. (This doesn’t that mean you must throw it away, but often when initial quality is intentionally low, it’s cheaper and easier to just scrap it and rebuild from scratch).
- Only work on hard issues related to the specific needs of the current project, and stop when the solution is clear.
- Try to demo something functional so you can collect business-related information regarding how this solution will impact future development.

## Consequently

Risk is reduced for the overall project in the early stages of the migration. Criticalknowledge and experience are gained during the experimentation process.

{:.plusminus}
- {:.plus} You have gained the knowledge and proved the solution works, and now understand how it fits into the overall project.
- {:.plus} You now have reasonable confidence that this is the correct decision.
- {:.minus} Running PoCs carries cost. Every time you do it, you pay for it.
