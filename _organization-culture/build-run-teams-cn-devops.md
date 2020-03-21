---
title: Build-Run Teams (“CN DevOps”)
description: Dev teams have full authority over the services they build, not only creating but also deploying and supporting them
layout: pattern
---

![Build-Run Teams (“CN DevOps”)]({{ site.baseurl }}/assets/images/build-run%20teams.png)

The company has cross-functional teams (Agile) or teams siloed by technical specialty(Waterfall) and needs to move to a structure compatible with cloud native. Development teams rely on the Ops team to deploy artifacts to production. The company is looking for the right balance between independence and standardization for their dev teams.

## In This Context

When development teams are responsible for building an application and supporting it in production, if they also try to build the build the platform to run it,the organization can end up with multiple irreconcilable platforms. This is unnecessary,expensive to operate (if even possible), and takes time away from teams that should be focusing on delivering features, not the platform they run on.

- Handover between development and operations teams kills production speed and agility.
- Adding an Ops person on each developer team is how you end up with 10 irreconcilable platforms.
- Conway’s law says that software architecture will come to resemble the organization’s structure, so if we want the platform to be independent, then the teams developing an application need to be separate from the team running the production platform.
- There is a limit to the capabilities a team can have. Devs are devs; they can extend their knowledge to a certain level, but they are not Ops.
- Maintaining Ops and Development as separate disciplines/teams is not sustainable in cloud native.
- Too much freedom brings chaos, but too much standardization strangles innovation.

## Therefore

Create teams that each have their own capability to build a distributed system with microservices managed by dynamic scheduling.Build-Run teams will be responsible for building distributed applications, deploying them, and then supporting the applications once running. Build-Run teams all use the same standardized set of platform services and deploy to a single unified platform that runs all applications for the entire company. This platform is the responsibility of the Platform Team, which implements and supports it.

- Build-Run teams are not DevOps teams in the traditional sense that devs and operations people sit together.
- In Agile, the development team also includes software testing capabilities, but the products are handed over to a separate Ops team to be delivered to production.
- In cloud native a true cross-functional team must be able to build distributed systems.
- The Platform Team is a specific kind of Build-Run team in that it builds, deploys,provisions, and supports the cloud native platform and infrastructure, but it works separately from the application development teams.

## Consequently

There is strong separation of defined responsibilities: Build-Run teams handle the applications. The Platform Team is responsible for building and maintaining the operating platform.The Platform Team doesn’t have to be part of the company—public clouds like Google/AWS/Azure, etc., with their automated platforms, could make an internal Platform Team unnecessary. If a Platform Team is designated, they are typically global,supporting all services/applications; Build-Run teams are separate and rely on standardized platform delivered by the Platform Team.

{:.plusminus}
- {:.plus} Teams have a bounded level of autonomy and ability to focus on their true tasks.
- {:.plus} Developers still have freedom to choose components to run on top of the standardized platform so long as they are compatible.
