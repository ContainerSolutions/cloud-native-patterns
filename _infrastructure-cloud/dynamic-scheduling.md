---
title: Dynamic Scheduling
description: An orchestrator (typically Kubernetes) is needed to organize the deployment and management of microservices in a distributed container-based application to assign themacross random machines at the instant of execution
layout: pattern
---

![Dynamic Scheduling]({{ site.baseurl }}/assets/images/dynamic%20scheduling.png)

An application has dozens of independent microservices, and the development teams want to deploy each of them multiple times a day on a variety of private and public cloud platforms.

## In This Context

The traditional hardware approach assumes “This app runs on this server”—which is not practical in a distributed system running on the cloud. Attaching specific microservices to specific pieces of hardware significantly compromises the stability and resilience of the system and leads to poor use of the hardware. Everytime you want to improve something you need someone to understand how it is all related, so they can safely make the change.The market demands that companies deliver value to clients very quickly, in a matter of hours or even minutes. However, the traditional deployment of applications to specified static servers using manual or semi-automatic procedures cannot support the growing demands of the development teams to deploy each component separately on multiple environments once, or even more times, perday.

- Software systems become more distributed overall and are required to run on many platforms.
- Dynamic scheduling tools (i.e. container orchestrators like Kubernetes, Nomad,and Docker Swarm, among others) are becoming mature and available for general use.
- Small pieces of applications can fail at random times.
- Advanced technology companies deploy thousands of times a day to large and varied array of development, testing, and production environments.
- In a system with hundreds of components, designating where each one runs increases complexity in the code because this must be specified in the build and is impractical.
- Predicting how a distributed system will behave in runtime is practically impossible.
- All major public clouds have managed dynamic scheduling as a service.

## Therefore

All application scheduling needs to be done using an orchestration system in a fully automatic way.Dynamic schedulers function as container management, in the form of a platform for automating deployment, scaling, and operations of application containers across clusters of hosts. This helps to achieve much more efficient hardware use as the scheduler understands the latest state of the system and can squeeze many components to the same piece of hardware. It also helps to achieve much higher resilience by adding health checks and elements of self-healing and abstracts away the target hardware to simplify the development.

- Cross-functional teams need to understand how to use such tools effectively, and they need to become part of the standard development process.
- Dynamic scheduling also handles stability and resilience by autoscaling and restarting failing applications.

## Consequently

Developers build distributed systems and define how components will run and communicate with one another once they are deployed.

{:.plusminus}
- {:.plus} Applications can scale up and down.
- {:.plus} Non-functional parts can be restarted and healed automatically.
- {:.minus} In a distributed system you invest in mechanisms for disaster recovery and disaster maintenance, which carry a high cost.
- {:.minus} Maintenance is more complex.
- {:.minus} Even when letting the public cloud handle it for you, Dynamic Scheduling is still exponentially more complex than running a single server.
