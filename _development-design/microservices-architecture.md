---
title: Microservices Architecture
description: To reduce the costs of coordination among teams delivering large monolithic applications,build the software as a suite of modular services that are built, deployed, and operated independently
layout: pattern
---

![Microservices Architecture]({{ site.baseurl }}/assets/images/microservices%20architecture.png)

A company has decided to move to cloud native and is looking at ways to speed up feature development and to optimize their use of cloud resources. The size of the development/engineering staff can range from a few tens, for a small to medium business, up to a few thousand for a large enterprise.

## In This Context

Delivery of large monolithic applications developed by large teams require long and complex coordination and extensive testing, leading to longer TTM (Time to Market). Hardware use by such applications is inefficient, which leads to wasted resources.

- People tend to delay painful moments; since integration and delivery are typically painful, their frequency tends to decrease as system longevity increases.
- Larger monolithic systems are increasingly difficult to understand as they grow in size and complexity.
- Monoliths are easier to work with than modular applications as long as they are small enough to be understood by each developer.
- Tiny monoliths (not big ones) are often the quickest, simplest solution to relatively easy problems.
- Conway’s law: architecture tends to resemble the organizational structure.

## Therefore

Split applications into smaller, loosely coupled microservices that can be built,tested, deployed, and run independently from other components.

- Small and independent teams work on separate modules and deliver them with only limited coordination across the teams.
- Independent components allow different teams to progress at their own pace.

## Consequently

New systems are created from many small and independently built components with a complex web of connections.

{:.plusminus}
- {:.plus} Faster-moving teams are not held back by slower ones.
- {:.plus} Teams can choose the most appropriate tools for delivering their particular service.
- {:.minus} Independence and freedom of choice are achieved, but with the tradeoffs of reduced standardization and certain types of reusability.
