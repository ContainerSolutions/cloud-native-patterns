---
title: Decide Closest to the Action
description: Those nearest to a change action get the first chance to make any decisions related to it
layout: pattern
---

![Decide Closest to the Action]({{ site.baseurl }}/assets/images/Decide%20closest%20to%20action.png)

Cloud native transformation is underway, and there is a lot of uncertainty. People are still learning about the tech, which itself is continually evolving, and the market is changing frequently and erratically. Each team is responsible for delivering its own microservice, and there are many moving pieces. Managers and lead architects have only a broad, high-level understanding of the product and little grasp of the technical details that underlie the actual development process.

## In This Context

Decision making via chain of command is not sustainable in cloud native. Using hierarchy to resolve conflicts and agree on decisions takes too long, and solutions are limited to the capabilities of the managers making that level of decision. Engineers might find a superior solution that never gets implemented because it takes too much time and effort to navigate the bureaucracy to get permission. So they will give up and just move on with whatever they have.

- Recent speed of technological change is growing exponentially.
- Market is now also changing frequently, with unexpected new competitors appearing.
- In traditional organizations, managers make all the decisions and give instructions to engineers.
- Further you go from the change, the slower the decision over time.

## Therefore

Push the decision power as close as possible to any change as it is happening. It is typically best if the dev team itself makes the decisions.Because your team works as part of a bigger tribe of teams, sometimes your decision must involve others. For example, if you want to change APIs, you must inform those who use them—and they may object to the change. So whatever happens inside of a microservice is fully the domain of its development team, but anything going in/outis also the domain of the teams that consume them.

- Put in place security and regulation to make sure people are allowed to make these decisions.
- Complete separation of duties: execs in charge of strategy, managers in charge of setting objectives, engineers free to execute their work as they see best.
- Instill that it’s OK to fail into the organization’s values.
- Use hierarchical management for conflict resolution.

## Consequently

Executives delegate the power to create the vision and objectives to middle management,and middle managers delegate power over technical decisions to the execution teams.

{:.plusminus}
- {:.plus} Strong incentive to resolve conflicts first within team, then within tribe, only then go to management.
- {:.minus} Time and effort are required to coordinate with any teams who are consuming your particular service to make sure it works all around.
