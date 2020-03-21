---
title: Strangle Monolithic Application
description: Gradually split pieces of the old monolithic application one by one, re-architect them intoservices, and move them over time to the new cloud native platform
layout: pattern
---

![Strangle Monolithic Application]({{ site.baseurl }}/assets/images/Strangle%20monolith.png)

You have a monolith and are moving to microservices architecture. The new platform is ready or soon to be ready and you’re preparing the strategy for splitting the monolith into microservices.

## In This Context

Re-architecting a large monolith, built over many years or even decades, is a massive project that can take years. Some companies try to do it all at once, but rewriting a large monolithic application from scratch also carries great risk. You cannot start using the new system until it is developed and functioning as expected, but your company has little cloud native experience or knowledge to get this done.Building a new system from scratch will take a year or (likely) longer. While it is under construction there will be minimal enhancements or new features delivered on the current platform and so the business risks losing market share.There is also a large risk of doing it all wrong in your first attempt. If the first project covers the entire application, then it will be very difficult to step back and start over due to sunk-cost fallacy—even if doing so is the best solution.

- Teams don’t yet know how to split the monolith into microservices.
- The first time you do something you are going to make mistakes; it is a learning experience rather than an execution.
- Monoliths hide unexpected problems inside their huge size.
- A well-scoped migration can handle problems as they emerge, but if you are trying to do everything all at one time, they will cripple the initiative.
- 20/80 principle: it takes 20% of the time to get 80% finished, and then 80% of the time to finish the last 20% (and the last 1% will take as much time as the first 99%, so keep that 1% on the mainframe—see Lift and Shift At the End).

## Therefore

Once the cloud native platform is ready, take small pieces of the monolithic application and, one at a time, re-architect them and then move them to the new platform.The business value of new functionality is achieved much more quickly, and the cloud native architecture of loosely coupled services means future refactoring work will be simple. This is the cloud native version of Martin Fowler’s classic strangler pattern.

- Going piece by piece and over an extended period of time is key.
- First have the final functional platform in place.
- Give priority to pieces that change frequently and those that are easy to extract.
- Create demo apps.
- Document a simple way for migrating pieces to the platform to make the process consistent, replicable, and as quick and effortless as possible.
- Leave the things that are running but not changing at all behind on the old system,and move them at the very end.

## Consequently

There is a mixed environment of old and new applications working together. The team is getting better at re-architecting the pieces of the monolith.

{:.plusminus}
- {:.plus} A plan is in place for moving pieces over time.
- {:.minus} Some teams are still working in the old environment—the entire company is not all moving to Kubernetes on Day One.
- {:.minus} Two different operational models are in place, which can create its own set of problems.
