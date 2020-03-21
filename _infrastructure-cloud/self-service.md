---
title: Self Service
description: In cloud native everyone can do their own provisioning and deployment with no handoffs between teams
layout: pattern
---

![Self Service]({{ site.baseurl }}/assets/images/Self%20service.png)

The company is moving from Waterfall/Agile and, within a structure of separate operations and development teams, is aiming to set up microservices, CD, and public(or private) cloud. Teams are running many experiments and PoCs and aiming to reduce the cost of experimentation.

## In This Context

In traditional organizations, provisioning hardware or doing maintenance work requires filling out a form, sending it to Ops, and waiting for them to do it on your behalf. Each handover creates a delay of hours, days, even weeks, and this slows down the entire system. This process also discourages frequent releases from developers to production, and without that there is no Continuous Delivery (CD),no learning loop from delivering to customers and receiving feedback.

- Anything manual is, by definition, too slow for cloud native.
- People will do more of something if they can do it themselves.
- Premature optimization—automating the wrong thing—can be particularly bad in this context.

## Therefore

Across the company, everything related to software development should be self service:everyone should be able to provision infrastructure or deploy their applications on their own without handoff to another team.Self-Service is the requirement—Automate Everything is the way you achieve that.

- Create full automation around the platform. All manual or semi-manual processes must be fully automated.
- Create UIs and APIs so people can include this in their automation.
- Grant access to all developers (within reasonable security limits).
- Start during the MVP stage: Prerequisite is basically having the entire cloud native toolset.

## Consequently

Whenever anyone needs something done, they can do it on their own without handing off to Ops.

{:.plusminus}
- {:.plus} Reduced cost of experimentation because there is less waiting for results.
- {:.plus} Reduced dependencies.
- {:.minus} Functional self-service needs a much higher-quality interface, which is a much higher cost.
- {:.minus} The system is automated to be bulletproof against wrong behavior by nonexperts using it, which is valuable but also has cost. If you have experts working on infra, they don’t need foolproof systems—but most people aren’t experts.
