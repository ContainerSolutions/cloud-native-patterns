---
title: MVP Platform
description: Once Exploratory Experiments and PoCs have uncovered a probable path to success, build a simple version of a basic but fully functional and production-ready platform with one to three small applications running on it in production.
layout: pattern
---

![MVP Platform]({{ site.baseurl }}/assets/images/(platform)%20MVP.png)

The goal is clear, the tech is available, and knowledge is present, and all major questions are answered by a series of PoCs. Now is the time to build a real platform. Development teams are on hold and waiting for the new platform to start building new applications and refactoring old ones.

## In This Context

Trying to add too many functions to the first release will make it very protracted and delay any release to production. In the traditional Waterfall approach a new platform will be used in production only if it’s fully finished and everything is ready. Building a fully featured cloud native platform may take up to three years, but since cloud native components work independently, the platform can be running apps in production even before it’s completely built out. Not using the platform or any of its features until it is 100% complete would be a lost opportunity.

- Minimum basic functionality could be built in a fraction of the time it takes to build the full system.
- There is always something to remove from the list of critical features.
- Custom complex solutions are difficult to build and maintain.

## Therefore

Define and build a system with minimal useful—and production-ready—functionality on a quick timeline. It’s important to release something quickly in order to start getting real feedback so you can then improve things based on that user response.

- “Minimal usefulness” can vary per company.
- Cloud native Platform MVP should take two to six months to produce.
- Build good basics and quality to reduce the need for user support, but don’t go overboard.
- Extendability is critical.
- Plan additional two to three phases to bring the platform to full functionality.
- Use experiments and PoCs to define the MVP.
- Stress assumptions in real life—build a system that works with how people will need and want to use it.

## Consequently

The first MVP of the platform is ready and can be used by a small number of development teams to deliver a few apps to production. The Platform Team has a plan to expand the scale and functionality of the platform as it continues rolling it out to the rest of the organization.

{:.plusminus}
- {:.plus} Teams can begin learning the basics of using a cloud native platform even while the final production version is still being developed.
- {:.minus} The MVP represents 20%–40% of the final platform; further effort is still required to build out a complete, production-ready platform.
- {:.minus} Core team needs to do support for this version while continuing to develop the production platform that will eventually replace it.
