---
title: Risk-Reducing Deployment Strategies
description: Employ release tactics to decrease the chance of problems happening when changes are introduced into the production system
layout: pattern
---

![Risk-Reducing Deployment Strategies]({{ site.baseurl }}/assets/images/Risk%20reducing%20deployments.png)

You have a cloud native system with high availability requirements. Teams are building microservices and releasing them independently and often.

## In This Context

Deployment is like a plane taking off: it’s the most dangerous part of flying. System failures typically don’t happen during normal operation but rather during maintenance and updating. This is because change always carries risk, and these are times when you are introducing change into the system.Deployments are the most frequent and common type of change, and if not treated carefully can introduce a lot of instability. In cloud native, deployment happens very frequently, so this is an important area of concern.

- Maintenance tasks are risk points.
- Deployment frequency in cloud native is high.
- Impact of changes to a complex distributed system is impossible to predict and can lead to cascading errors.
- Modern web users expect 100% availability and high levels of system responsiveness.

## Therefore

Use a variety of advanced release strategies to reduce the impact to end users whendeployments occur.There are multiple ways to more safely release a new version of an application to production,and the choice is driven by business needs and budget. Options that work well for cloud native are:

- Re-create: First the existing version A is terminated, then new version B is rolled out.
- Ramped (also known as rolling-update or incremental): Version B is slowly rolled out and gradually replaces version A.
- Blue/Green: Version B is released alongside version A, then the traffic is switched to version B.
- Canary: Version B is released to a subset of users, then proceeds to a full rollout.
- Shadow: Version B receives real-world traffic alongside version A until stability and performance are demonstrated, and then all traffic shifts to B.When releasing to development/staging environments, either a re-create or a ramped deployment is usually a good choice. If releasing directly to production, a ramped or blue/green deployment is a good potential fit but proper testing of the new platform is necessary. Blue/green and shadow strategies require double resource capacity and so are more expensive, but reduce the risk of user impact. If an application has not been thoroughly tested or if confidence is lacking in the software’s ability to carry a production load, then a canary or shadow release should be used.Shadow release is the most complex, especially when calling external dependencies with mutable actions (messaging, banking, etc.). But it is particularly useful in common cloud native situations like migrating to a new database technology due to the ability to monitor live system performance under load while maintaining 100% availability.(If your business requires testing of a new feature against a specific demographic filtered by parameters like geolocation, language, device platform, or browser features,then you may want to use the A/B testing technique. See the A/B Testing pattern.)
- Dynamic scheduling used in conjunction with other technologies supports a variety of deployment strategies to make sure infrastructure remains reliable duringan application update.
- Use redundancy and gradual rollout to reduce risk.
- Limit the blast radius by deploying small parts of the system independently.

## Consequently

Risks to the system during deployment/maintenance are anticipated and managed.

{:.plusminus}
- {:.plus} Deployments are frequent, and the Dev teams are confident.
- {:.plus} Users get high availability and seamless responsiveness.
- {:.minus} These setups are complex, and cost can be high.
- {:.minus} The complex nature of these techniques can introduce new risks.
