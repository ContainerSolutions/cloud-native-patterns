---
title: Reproducible Dev Environments
description: Developers need to test their daily work in an environment that is easy to spin up and that matches production tooling as closely as possible
layout: pattern
---

![Reproducible Dev Environments]({{ site.baseurl }}/assets/images/Reproducible%20dev%20environment.png)

Developers are building containerized microservices and deploying them to the containerized platform. Each microservice is built by a team, and microservices are interpreted into the larger system. There are many devs on many teams.

## In This Context

Shared environments and databases are difficult to keep in good shape and create dependencies that lead to delays.When developers can’t create their own test environments, they may avoid running proper tests before submitting the code or run them on shared environments that may affect the work of their teammates. This affects other developers by making interpretation more difficult.

Differences between development environments and the eventual production environment may lead to the introduction of bugs that happen only in production and are related to those differences.In all of these scenarios, product quality and developer productivity suffer.

- Local testing reduces interpretation problems.
- If setup for the developer environment is too slow, devs will reuse the same environments.
- If not refreshed, local environments tend to undergo configuration drift.
- Shared environments create dependencies that lead to delays.
- Developers tend to create many test environments if it is easy and fast.
- Developers often have multiple changes that require testing at the same time.
- CI and CD are much more difficult to achieve without being able to test each change thoroughly.

## Therefore

Establish a fully automated and fast process to create development environments where devs can test-run their apps. Each developer should be able to have their own environment, or multiple environments, that resemble the eventual production environment.

- Provide the same (or at least close to the same) tooling to deploy apps as in production.
- It is possible to do this on the cloud but will require cost management.

## Consequently

Each developer can run tests on their own without delays or disturbing the rest of the team.

{:.plusminus}
- {:.plus} Productivity and product quality are high.
- {:.minus} Could require a lot of hardware to create, at high cost.
- {:.minus} If on cloud, devs may forget to switch them off and accidentally create large use charges.
