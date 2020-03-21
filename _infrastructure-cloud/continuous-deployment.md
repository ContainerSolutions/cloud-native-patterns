---
title: Continuous Deployment
description: Continuous Deployment automatically and seamlessly pushes code that has been accepted in the Continuous Integration/Continuous Delivery cycle into the production environment
layout: pattern
---

![Continuous Deployment]({{ site.baseurl }}/assets/images/continuous%20deployment.png)

The team is using Continuous Delivery and building a distributed system using microservices. There is no regulation nor any other restriction on fully automated delivery.

## In This Context

Changes are frequently delivered to a production-like environment in a quick and automated way, but then they get stuck there.Many teams using CI/CD still have a human gate at the end, meaning that beforechanges can go live they may need to wait for the Ops team to do extensive testing,whether automated or manual, and/or wait for manual deployment. This means changes are not tested in a real live environment and carry high deployment risk duet o potential differences in tools and processes. Time to market is slower; release manager delays releases due to risk and complexity.

- Any handover point slows down the process and introduces risk.
- Some industries have regulations that define roles during development and deployment (for example, release must be manually approved by a designated person of responsibility, as is common in financial sector regs).
- Frequent delivery better helps perceive customer needs.

## Therefore

Create a fully automated deployment process to take all changes to production all of the time. Use gradual deployment strategies and prepare for failure mitigation.Every change committed to the source code repository needs to be tested and ready for delivery to production at any given moment based on business needs and according to the relevant regulations.

- Build in full automation throughout system.
- No team or service dependencies are allowed.
- Make sure there is very good overview of the content and risks to the release manager.
- In case of regulatory restrictions that require a manual delivery step, automate everything before and after the release review point and make the release point as simple as pressing a button. Provide sufficient information to the release manager to allow fast and sound decisions.

## Consequently

Speed of delivery to customers is very high, and the changes are flowing to the customers daily or even hourly. Products or services are continuously providing higher value to the customers while allowing the developers to get real live feedback very quickly and learn and improve the products even further.

{:.plusminus}
- {:.plus} Experiments can be done quickly and changes rolled back if necessary.
- {:.minus} Some issues can still sneak in.
- {:.minus} You have less control over feature release cadence.
