---
title: Service Priority
description: Services should be assigned different priorities depending on its importance.
layout: pattern
---

![Service Priority]({{ site.baseurl }}/assets/images/cs.png)

You have deployed multiple applications in a dynamically orchestrated environment. In dynamic/cloud environment we want to over provision our infrastructure in order leverage dynamic nature of our applications to use our resources (CPU/Memory) as efficiently as possible. 

## In This Context
When resources (usually memory) are exhausted on a node/server our dynamic orchestration platform is forced to choose an application(s) to evict in order to avoid the entire node crashing. This can have negative effects if our critical applications are taken down.
- The dynamic nature of our applications make prediction of resource usage difficult
- We want to leverage the dynamic nature of our applications and utilization to over provision.
- Certain applications react differently to unscheduled termination

## Therefore

We can specify the relative priority of our different applications in order to pre-determine which ones will be evicted first. This allows us to protect our more critical services.

##### Actions
- Determine which of our services are the most critical
- Define priority levels for all services
- Assign priorities with the platform
- E.g. PodPriority in Kubernetes

## Consequently

{:.plusminus}
- {:.plus} All services will be assigned a priority.
When resources are exhausted on a node, the orchestration platform is able to make more intelligent decisions about which applications to kill/reschedule
- {:.plus} When higher priority services are needed to be scheduled, and sufficient resources are not currently available, the orchestration platform is able to evict lower priority applications to make space.
