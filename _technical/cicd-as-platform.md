---
title: CI/CD as Platform
description: The CI/CD system is treated as a platform on top of the cloud platform.
layout: pattern
---

![CI/CD as Platform]({{ site.baseurl }}/assets/images/Generic.png)

The complexity of software delivery in an enterprise company can easily reach a level when
a dedicated team would have to be responsible for its maintenance.

## Context

Enterprise company is developing Cloud Native CI/CD services during a transormation or
cloud migration. CI/CD services include building of container images, code quality checks,
security scans and deployment of artifacts to environments. CI/CD plays a significant
part in compliance requirements and making sure production systems are secure.

## Problem

CI/CD services on an Enterprise scale are difficult to implement. Taking into account 
requirements for auditing, compliance and team flexibility will lead to a system
which is customized to a high degree. Often the responsibility for the these services
end up with the Platform Team, which is managing infrastructure. While CI/CD is related
to the infrastructure platform, it has it's own goals and a different domain (in DDD terms).

## Solution

Create a dedicated product team, which will build and manage CI/CD services. This team will
be a consumer of the infrastructure platform and a service provider towards development
teams. The CI/CD Platform Team should treat CI/CD services as a product offered to all
development teams. This means feature requests should be phrased in way that is useful to
all users of the platform. All platform services should be self-service, CI/CD Platform Team 
members should only interact with application developers in limited ways (e.g. support) so
they can focus on building functionality. Thus the team is an internal product team, not an
enabler team.

## Resulting Context

This pattern has the following benefits:
* CI/CD services are treated as first class citizens in the larger Cloud Native Platform
* Application teams can consume CI/CD services without waiting for actions from another team
* Specialist knowledge can be more easily built up and used in a team with fewer reponsibilities

This pattern has the following drawbacks:
* Development teams have to wait until features get prioritized in a product backlog.
* CI/CD Platform Team can't solve Infrastructure Platform issues affecting them.

## Related Patterns

* GitOps
* Continuous Deployment
* Continuous Delivery
* Continuous Integration
* Platform Team