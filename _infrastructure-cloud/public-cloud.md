---
title: Public Cloud
description: Instead of using your own hardware, rely on the hardware managed by public cloud vendors whenever possible
layout: pattern
---

![Public Cloud]({{ site.baseurl }}/assets/images/public%20cloud%20.png)

You are moving to microservices, you are continuously growing your codebase, and teams now require automation for Continuous Delivery. The amount of manual workis going down, but the cost of maintaining hardware is going up.

## In This Context

Procuring, installing, and maintaining hardware becomes a bottleneck that slowsdown the entire organization .For most businesses, infrastructure and hardware are not their core business, so they do not invest heavily in maintaining and improving them. Public cloud vendors, however, invest a great deal of money and talent to optimize their services. Furthermore, when you own the hardware, costs are typically higher: you need to overprovision for peak consumption. If Black Friday traffic is 10 times higher, thenyou must maintain that 10-times capacity the other 364 days of the year—there is noelastic capacity expansion.

- Private clouds quickly become outdated because they are not a high priority for the business.
- Never enough resources to make a private cloud as good as public cloud.
- In some business areas regulations may not allow use of public cloud due to security concerns and explicit data regulation.

## Therefore

Hand over the management of hardware and rent capacity from public cloud vendors like Amazon, Microsoft, Google, and similar instead of owning, managing,and creating full automation for infrastructure.

- Rely on full automation.
- Use APIs to connect with public cloud.

## Consequently

You rent fully automated, scalable, resilient infrastructure from a public cloud provider that can be increased and decreased on demand. You pay only for the resources you are actually using.

{:.plusminus}
- {:.plus} Take advantage of integrated services.
- {:.plus} Public cloud vendors constantly upgrading to latest software and services.
- {:.plus} Built-in services like maintained databases, machine learning frameworks, and all kinds of SaaS continuously being built by the vendors.
