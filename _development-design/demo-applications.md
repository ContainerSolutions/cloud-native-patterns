---
title: Demo Applications
description: Teams onboarded to the new cloud native system receive demo applications as an educational starting point for building their own cloud native applications
layout: pattern
---

![Demo Applications]({{ site.baseurl }}/assets/images/Demo%20applications.png)

The Core Team has built the initial platform and is ready to start onboarding the rest of the organization to cloud native. Developers have gone through platform trainings and soon need to start moving apps to cloud native. The level of cloud native experience is low.

## In This Context

Teams newly onboarded to cloud native have limited knowledge and no experience creating cloud native applications. They will tend to apply established skills and approaches carried over from previous experience in non-cloud native systems.This will lead to re-creating tightly coupled, interdependent applications—suboptimal architecture that conflicts with cloud native. This reduces overall quality for the apps they deliver and fails to capture cloud native’s development velocity benefits. Re-architecting apps later is much harder than building them the right way in the first place.

- People tend to use known methods to solve new problems.
- Much easier to start from something rather than nothing.
- People learn by doing and from experiencing examples.

## Therefore

Build a number of simple, functional apps that fully fit cloud native practices.Make those apps known and available to new teams as they join the cloud native setup. Keep the demo apps up to date and adjust them to the latest best practices developed by the Core Team.

- Applications are basic but fully functional with a UI and a database, and built on microservices architecture with services communicating via APIs.
- Continuously improving—as the teams learn, they can incorporate new tools and methods to expand the application.
- Emphasize clean and high-quality code.
- Tests need to be automated/built in.
- The apps are to be delivered using CI/CD, and the delivery scripts are part of the applications.
- Always up and running—practice Build-Run Teams delivery workflow.

## Consequently

Teams moving to the new system have a way to practice their new skills and prepare to deliver a full enterprise application.

{:.plusminus}
- {:.plus} Devs can start from the right place.
- {:.plus} Core team can apply their knowledge.
- {:.plus} Architecture is more consistent.
- {:.minus} Demo apps could limit creativity (default effect).
- {:.minus} Core Team spends time on writing demo applications.
