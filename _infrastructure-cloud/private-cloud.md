---
title: Private Cloud
description: A private cloud approach, operated either over the internet or on company-owned on premises infrastructure, can offer the benefits of cloud computing services like AWS while restricting access to only select users
layout: pattern
---

![Private Cloud]({{ site.baseurl }}/assets/images/private%20cloud.png)

A company in a highly regulated industry that is, by law, not allowed to use public cloud or a company in any sector that has recently made a major investment in new on-premises infrastructure. In the Private Cloud context, services are provisioned over private—though not necessarily on-premises—infrastructure for the dedicated use of a single organization and typically managed through internal resources.

## In This Context

Connecting designated hardware to specific apps reduces their mobility and resilience.Building any kind of manual intervention by the Ops team into an application’s life cycle will create long delays in deployment and reduce quality.

- There is a lot of fear around data on the public cloud.
- Public cloud vendors are very knowledgeable about, and experienced in, running large infrastructure.
- In much of the world, public cloud is allowed for almost all industries.
- A private cloud is under full control of the company, so you can optimize in different ways and customize different things that are not possible on public clouds.
- Proficient support is required to keep private clouds up and running, so you must have all that knowledge in your (typically limited) team.

## Therefore

Decouple the setup of your physical infrastructure from the provisioning required for the application itself.Treat all the servers and the rest of the infrastructure as a single large machine managed fully automatically through a set of APIs. Aim to use the same set of tools as would be required on at least one public cloud to ease any future migration.

- Fully automate everything related to running the application.
- Treat your on-premises infrastructure like a cloud; the hardware needs to be completely abstracted away from the users.
- Set up physical servers, network, storage, etc., all separately.
- Deploy and maintain applications through full APIs.
- Even if you need dedicated hardware, treat it as a part of the cloud so it is fully automated.

## Consequently

The company enjoys the benefits of cloud native architecture with the additional control and security—but also expense—of hosting your own private cloud setup.Applications are running on the private cloud in exactly the same way as they would run on a public cloud.

{:.plusminus}
- {:.plus} Developers can get infrastructure on their own, and delivery is faster.
- {:.plus} There is full control over the platform and data.
- {:.minus} Private clouds carry a high cost of ownership and quickly become outdated.
