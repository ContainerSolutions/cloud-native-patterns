---
title: Containerized Apps
description: When an application is packaged in a container with all its necessary dependencies, it does not rely on the underlying runtime environment and so can run agnostically on any platform
layout: pattern
---

![Containerized Apps]({{ site.baseurl }}/assets/images/containerized%20apps.png)

The team is building a distribution app that can scale up and down. Separate teams are meanwhile building microservices, and they need to take them quickly through a variety of dev and test environments all the way to production. There are a variety of different runtime environments, such as personal laptops, during development and different private and public clouds for testing, integration, and production.

## In This Context

Speed of delivery can be slow if an app depends on uniformity among different environments. Maintaining consistency of different tools and their versions on many machines across many on-premises and/or public clouds is difficult, time consuming,and risky.

- All stable environments tend to drift eventually.
- It’s impossible to manage thousands of machines manually.
- Differences in environment are difficult to find and to fix.

## Therefore

Package up an application’s code and everything it needs to run (all its dependencies,runtime, system tools, libraries, and settings) as a consistent unit so the application can be distributed to start up quickly and run reliably in any computing environment.This minimizes dependency on the runtime environment. Build once, run everywhere,and distribute quickly and easily.

- Use industry standards like Docker.
- Ensure proper versioning and simple and quick distribution.
- All dependencies included.
- All environments use the same basic tooling.
- Ensure that containers can run on local or any other environment.

## Consequently

Every part of the app is packaged in a container and can be easily started anywhere.

{:.plusminus}
- {:.plus} Container tools like Docker improve efficiency.
- {:.minus} Large numbers of separate containers increase system complexity.
- {:.minus} Managing container images requires extra effort.
