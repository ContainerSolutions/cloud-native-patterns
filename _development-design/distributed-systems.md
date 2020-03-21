---
title: Distributed Systems
description: When software is built as a series of fully independent services, the resulting system is,by design, fast, resilient, and highly scalable
layout: pattern
---

![Distributed Systems]({{ site.baseurl }}/assets/images/distributed%20systems.png)

System complexity has grown beyond the capabilities of the key architects to understand it, but additional growth is still required.

## In This Context

Once the system has grown beyond the capacity of a single architect/engineer to understand, it becomes difficult and time-consuming to add functionality. With the growth of the old software systems, more people join the team and the system constantly collects technical depth, which leads to fragility and unpredictable side effects that come with every change. This creates fear of adding new functionality and stagnates development.

- Human mental capacity for grasping complex systems is finite.
- Monolithic systems require someone with full understanding of the complex relationships among components to make/approve any changes to the system.
- Almost all software systems start out as small monoliths.

## Therefore

Build the software system as a number of independent components (microservices)running on different computers and communicating through APIs. Development,delivery, and scheduling of each component is completely independent, andany component can fail without affecting the others.Distributed systems are much more complex to initially architect and implement, but once that initial work is invested they are much simpler to grow—and evolve with improvements, new features, and changes.

- Split the system into small pieces (microservices components).
- Define APIs.
- Use more, but simple, computers that are less expensive and easy/fast to provision.Public clouds are most effective.

## Consequently

Higher complexity through many decoupled components makes a more resilient and scalable system. Each component can become more complex until it is divided into smaller independent pieces to allow the system to grow indefinitely in scale and complexity.

{:.plusminus}
- {:.minus} At this level of complexity truly no one is capable of fully understanding the system, which makes it difficult to maintain.
- {:.plus} High levels of automation and good observability help prevent problems.
