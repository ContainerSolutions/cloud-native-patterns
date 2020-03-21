---
title: Observability
description: Cloud native distributed systems require constant insight into the behavior of all running services in order to understand the system’s behavior and to predict potential problems or incidents
layout: pattern
---

![Observability]({{ site.baseurl }}/assets/images/Observability.png)

Teams are moving to MS, and there are more and more pieces—the number of components is growing. Traditional responsive monitoring cannot recognize service failures.

## In This Context

Traditional systems practice assumes the goal is for every system to be 100% up and running, so monitoring is reactive—i.e., aiming to ensure nothing has happened to any of these components. It alerts when a problem occurs. In traditional monitoring if a server fails, you will have an event; response, even if automatic, is manually triggered. This assumption is not valid for distributed systems.

- A distributed system is by definition not 100% stable—when you have so many pieces, some of them will go up and down at random times.
- Resilience is built into the system to handle the assumption that eventually everything in the system will go down at some point.
- The number of components is always increasing while the number of people working on the application remains reasonably stable.
- Always a cost: if you get something, you must pay for it in some way. Here it is complexity, and you must manage it.
- Manual response is never fast enough in a cloud native system.

## Therefore

Put in logging, tracing, alerting, and metrics to always collect information about all the running services in a system.

- Switch from a centrally planned system to distributed self-governing system.
- Continually analyze availability of services and behavioral trends of the individual services and entire system.
- Instead of focusing on specific pieces of hardware, focus on functional behavior of components.
- Consistently collect as many metrics as possible.
- Analyze the trends.
- Create an interface to make system state accessible to all stakeholders: anyone involved in system maintenance or development who needs to understand the system at any given time must be able to observe the system’s behavior.

## Consequently

There is a continuous overview of the state of the system, visible to anyone for whom this is relevant information.

{:.plusminus}
- {:.plus} Analytics and proactive monitoring can be used to discover trends, which can be used to predict failure.
- {:.minus} Any response to a single specific failure is extremely difficult.
