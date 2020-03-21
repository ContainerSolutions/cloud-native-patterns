---
title: Platform Team
description: Create a team to be in charge of architecting, building, and running a single, consistent,and stable cloud native platform for use by the entire organization so that developers canfocus on building applications instead of configuring infrastructure
layout: pattern
---

![Platform Team]({{ site.baseurl }}/assets/images/platform%20team.png)

An enterprise is moving to the cloud and adopting microservices architecture. Many teams are building many different services, and they need extra tools to create the infrastructure to run their pieces of the application.

## In This Context

If there is no single team in charge of creating an official cloud native production platform for the transformation, each team responsible for different microservices will have to build its own platform.This duplicates effort, wastes time, and—most critically—sows conflict when it comes time to deploy. Because each service was built using a different approach on a bespoke platform, they will have conflicting needs and be difficult, if not impossible,to run all on one unified platform. Ops is stuck trying to come up with some kind of Frankenstein solution, but it’s unlikely they will be able to make it work.

- Different teams will build different solutions if not coordinated.
- Basic cloud is not enough; complex and custom configuration is required.
- Standardization maximizes the possibility of reuse.
- Freedom of choice is needed for finding the best solutions.
- People are creative in finding ways to circumvent the roadblock set by lack of platform, leading to a “shadow IT” effect.

## Therefore

The Platform Team will handle the platform itself—everything between the cloud and the apps (or, to put this in terms of the current technological landscape,Kubernetes and below)—while developers are responsible only for building the applications themselves (again, in the current tech landscape, Kubernetes andabove).

- Set up a separate team responsible for choosing, building, and configuring a basic set of tools and practices to be used by all of the development teams.
- Build one platform to be used by the entire organization.
- Create a standard and reusable set of tools to simplify work for the devs.

## Consequently

Developers are able to focus on building individual application services, features,and functionality while the Platform Team takes care of running the platform itself. Developers are allowed to introduce custom tools but they will have to support them as part of their own application unless the tools are proven stable and/or requested by other development teams.

{:.plusminus}
- {:.plus} There is a consistent, reusable, and, above all, stable platform that ensures all services work together seamlessly.
- {:.plus} There is less work for developers: they can just focus on building apps and not worry about the platform they will run on.
- {:.minus} There is also less freedom for developers to choose their tools, although choice is still possible.
