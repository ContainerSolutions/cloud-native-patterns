---
title: Full Production Readiness
description: Make sure your platform is fully provisioned with CI/CD, security, monitoring, observability,and other features essential to production readiness before you try to take it live
layout: pattern
---

![Full Production Readiness]({{ site.baseurl }}/assets/images/Full%20production%20readiness.png)

Core Team is stepping up the cloud native platform. The new platform and the first few applications moving over to it are scheduled for full production delivery very soon.

## In This Context

Too many companies try to rush their newly built cloud native platform into production before it is really ready. Typically the container scheduling platform isinstalled, but it’s still missing essential automation elements around maintenance and software delivery. This leads to poor quality of the running system and necessitates long delivery cycles. Many times the platform vendor will confirm production readiness of their tool—but without considering the whole system of delivery and maintenance cycles that are an equally crucial part of production.

- Typical cloud native platforms today include only a partial platform and require significant additional configuration and automation.
- A typical full cloud native platform includes 10 to 20 tools.
- Once the main platform is fully running, there is pressure to deliver.
- In case of poor maintenance automation, platform teams could be overloaded with support tasks as teams onboard.

## Therefore

Before going to production all major elements of the platform, as well as those of any applications initially migrating to it, need to be in place. This includes havinga scheduler, observability, security, networking, storage, and CI/CD. Also, at least basic maintenance automation must be in place.

- System is automated.
- Maintenance is automated or at least documented.
- A bare and basic MVP version of a platform is not enough: there must also be observability, CI/CD, security, etc.

## Consequently

The new platform is functional and maintainable, and major tasks are automated.The Platform Team can continue extending the platform while providing satisfactory support for the development teams using it.

{:.plusminus}
- {:.plus} All major elements of the platform are in place.
- {:.minus} May delay release to production.
