---
title: Automated Infrastructure
description: The absolute majority of operational tasks need to be automated. Automation reduces interteam dependencies, which allows faster experimentation and leads in turn to faster development
layout: pattern
---

![Automated Infrastructure]({{ site.baseurl }}/assets/images/automated%20infrastructure.png)

A company is moving to cloud native and adopting cloud native patterns such as Microservices Architecture, Continuous Delivery, and others. Teams are independent and require fast support services from the Platform Team. Most of the operational tasks are performed on demand by the Ops team.

## In This Context

Manual or semi-automatic provisioning of infrastructure leads to dependencies among the teams and to long waiting times for results, hindering experimentation and slowing development.

- Traditional operational teams don’t have sufficient levels of automation and, dueto high workload, no time to learn new technologies.
- Public clouds provide full automation of infrastructure resources.
- Manual requests and handover between development and operations teams is very slow.
- Number of operations engineers in manual systems must scale up proportionally to growth in infrastructure demands.
- Experimentation and research take longer and require more resources due to involvement of an already-busy operations department.

## Therefore

Dedicate at least 50% of the Ops team’s time to automating the operational tasks,and eliminate all manual infrastructure provisioning and maintenance tasks.Any manual work that is required in between the changes committed by the developerand the delivery to production will significantly reduce the speed of delivery and introduce interteam dependencies.

- Treat infrastructure automation scripts with equal importance as the rest of the company codebase.
- Automate, fully and completely: compute, storage, networking, and other resources;patching and upgrading of operating systems; and deployment and maintenance of systems running on top of the infrastructure.

## Consequently

Developers spend less time waiting for infrastructure resources and can conduct quick experiments and scale running systems rapidly and easily.

{:.plusminus}
- {:.plus} Ops team spending significantly less time on repetitive support tasks and investing more time and resources in ongoing improvement of the system.
- {:.plus} Full automation will allow the provisioning of exponentially more resources per member of operational staff.
