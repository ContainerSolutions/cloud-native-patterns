---
title: Continuous Delivery
description: Keeping a short build/test/deliver cycle means code is always ready for production and features can be immediately released to customers—and their feedback quickly returned to developers
layout: pattern
---

![Continuous Delivery]({{ site.baseurl }}/assets/images/continuous%20delivery.png)

Teams are doing Continuous Integration, so each change is automatically built and tested separately in a very short time. Developers commit changes at least once a day.Teams are building distributed systems using microservices architecture.

## In This Context

A full quality test of a distributed system can be done only when the entire system is fully deployed and used. Teams try to reduce complexity and increase quality through infrequent and coordinated multiple-team deployments to the test environment,and then handing off to the operations team for more extensive testing and, finally, delivery.Large-scale deployments at long intervals are usually difficult and time consuming,so teams tend to minimize their number. This leads to painful integrations between services, reduced independence of teams, slower time to market, and—eventually—lower quality and higher costs for building the product or service.

- There is more incentive to automate an operation if it happens more frequently(if something is painful do it more often).
- Some issues cannot be caught by automation.
- People gain trust in an action when it’s executed frequently and rarely fails.
- People lose trust quickly if quality is low or reporting unreliable.
- Small changes delivered by the teams themselves are easy to fix or revert.
- Recent changes are still fresh in developers’ minds.

## Therefore

Deliver every change to a production-like environment where all the services are delivered continuously and independently.Reduce the pain by using full automation coupled with increased speed and frequency of releases.- No manual handovers on the way to deployment.

- Full automation is now in place.
- Test automation is now in place.
- Products are always in a releasable state.
- Experiments are more effective, as getting feedback from real customers is fast and painless.

## Consequently

The business can release to customers anytime.

{:.plusminus}
- {:.plus} A feature can be tested very quickly with customers.
- {:.minus} Some failures will sneak in through automation.
- {:.minus} Very high level of automation is critical; any manual steps slow the process and introduce problems.
