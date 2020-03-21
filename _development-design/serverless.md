---
title: Serverless
description: The soon-to-arrive future is event-driven, instantaneously scalable services (functions)on the cloud
layout: pattern
---

![Serverless]({{ site.baseurl }}/assets/images/Serverless.png)

The team is building a highly scalable system or using tools that require integration maintenance tasks. Tasks are well-defined and repeatable and may require aggressive scaling for short bursts.

## In This Context

There are a lot of small tasks that can eat up a developer’s time: writing boilerplate code, setting up infrastructure, and of course later maintaining everything they created. Meanwhile, it’s very challenging to create scaling mechanisms that can respond in milliseconds. The first set of challenges leads to wasted developer effort plus extra costs related to setup and maintenance. The second typically results in over-provisioning of compute resources that have to be paid for whether they’re used every day or only on Black Friday.

- Serverless is a recent and somewhat still emerging execution model for cloud computing.
- Some applications may change hardware requirements quickly and dramatically.
- Scaling up and down manually is difficult.
- Software components (microservices) become smaller all the time.
- Maintaining servers and/or container schedulers is an expensive task.

## Therefore

Package small pieces of code into fully independent executable functions that can be individually triggered on a serverless platform. Functions get one input source and return one output. Any number of functions can be executed in parallel.Functions are self-contained and repeatable.Thought leaders and experts in distributed systems believe serverless technologies arethe next evolution of application infrastructure—the horizon that lies beyond microservices.Serverless architecture is “serverless” in that users never need to take care of,or even ever really think about, individual machines: infrastructure is fully abstracted away. Instead, developers simply pick from a nearly limitless menu of compute, network,and storage resources via managed services from public cloud providers. Serverlessis truly pay-as-you-go, calculated according to actual real-time consumption instead of pre-purchased services based on best guesswork. While this makes for cost-efficient application development, the true benefit is velocity: developers finally get to focus on writing code instead of managing servers or sharding databases.Currently there are many challenges to serverless adoption, such as operational control,the introduction of even greater complexity into (already highly complex) distributed systems, and effective monitoring.For now this falls under the H2/innovation and H3/research categories in the Three Horizons pattern, but some companies on the leading edge of cloud native have already embraced serverless. Those able to dedicate skilled engineers to conquering its current challenges are able to dramatically reduce operational overhead and streamline the DevOps cycle even further, while increasing scalability and resilience.Think of Serverless as basically like cloud native, with superpowers.

- Functions only consume resources while running.
- Very short startup time.
- Highly scalable.
- Cheap to use.

## Consequently

Some software tasks can be executed very fast at any scale; the rest of the system is containerized.

{:.plusminus}
- {:.plus} Some tools/tasks are running in functions.
- {:.plus} Running a function requires almost zero overhead.
- {:.plus} Developers will never have to think about provisioning infrastructure ever again.
- {:.minus} Creating a full serverless app is difficult due to current architectural limitations.
