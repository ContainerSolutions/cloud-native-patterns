---
title: SRE Team
description: The SRE (Site Reliability Engineering) team helps the development teams to maintain and improve the application (not the platform or infrastructure)
layout: pattern
---

![SRE Team]({{ site.baseurl }}/assets/images/SRE%20team.png)

A big company has a large, mission-critical application with very high demands for quality and availability, and significant resources for creating dedicated improvement teams.

## In This Context

Once a platform is built and in production, attention is often directed away from improving internal processes and runtime performance. This can cause degradation over time, reducing quality and performance.

- Dev teams are measured on functionality, Ops on stability, SRE on improvements.
- SRE is a very expensive team to operate because it requires the most experienced and knowledgeable engineers.
- Opportunity cost arises when you pull your best engineers from development teams to SRE.
- If improvements are the priority for this team, then this is somewhat removed asa responsibility/priority for the Build-Run teams.
- SRE is more relevant when an application enters maintenance mode, rather than during the initial build.

## Therefore

Create a team that is focused 50% on reliability and 50% on continuous improvement of internal processes and development practices.This SRE team worries about overall site (platform) availability overall. However,each individual service has its own operational needs as well. It can be helpful to add SREs into each individual build squad (or at least tribe) to focus on service availability.

- SRE engineers are in charge of improving whatever it takes to create better infrastructure,better runtime, and better user support.
- The SRE team makes the error budgets and helps the dev team define its operational model and the Platform Team to improve the platform.
- Most tasks are automation rather than manual support.
- Every 18 months the SRE team needs to automate everything it is doing manually(so it can move to the Platform Team’s responsibility).
- You have a highly knowledgeable and experienced team, with good knowledge of operations but also devs who can write code.

## Consequently

The runtime stability and quality is continuously increasing, and automation is also increasing.

{:.plusminus}
- {:.plus} Developers are aware of operational concerns and incorporate that knowledge into their development cycle.
- {:.plus} The SRE team works closely with the Build-Run teams and the Platform Team.
- {:.minus} SRE teams are expensive and take top engineering talent away from other projects.
