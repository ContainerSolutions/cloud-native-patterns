---
title: Communicate Through APIs
description: In a highly distributed system, microservices must communicate with one another via stable and strongly segregated APIs
layout: pattern
---

![Communicate Through APIs]({{ site.baseurl }}/assets/images/Communicate%20through%20API.png)

A company is building a microservices application. Some teams work on a single microservice, others on multiple microservices. Teams are independent and aim to reduce inter team dependencies on both technical and organizational levels.

## In This Context

If APIs among microservices are not well-defined and fully segregated, they will require tighter coupling in development and/or delivery. This in turn introduces dependency, both service-to-service and among teams on an organizational level.This process essentially undoes the move to decouple the monolithic app in the first place, as it leads to coordinated development for the delivery of multiple services and requires very tight collaboration across teams.This reduces the speed and agility of the organization and effectively re-creates the original monolithic architecture and organizational structure.

- Tight coupling begins with a simple decision to share data directly.
- Conway’s law: a software application’s architecture will evolve to mirror the organizational structure of the company producing it.
- A single team working on multiple microservices may take shortcuts and introduce tight coupling.

## Therefore

Microservices should communicate with one another only through the network,using simple, consistent, and stable APIs.

- Build stable APIs with backward compatibility.
- Place most of the service logic within the service itself, keeping the API simple and easily maintainable.
- Smart endpoints, dumb pipes (most of the business logic is in the microservices themselves and not in the APIs).
- Ensure each microservice has no direct access to data of other microservices.
- Make sure there is version control and version management for APIs.

## Consequently

Microservices are kept decoupled and independent.

{:.plusminus}
- {:.plus} Old microservices can easily be replaced when needed as long as APIs are preserved.
- {:.minus} Communication through network can be slower and is more complex to architect.
