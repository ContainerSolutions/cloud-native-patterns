---
title: Ephemeral Environments
description: Leverage automation to create ephemeral environments on demand
layout: pattern
---

![Ephemeral Environments]({{ site.baseurl }}/assets/images/cs.png)

A team running applications on modern cloud native platform (such as Kubernetes) often requires a variety of environments. Getting a production like environment running on a developers laptop is often not possible. The benefit of automated infrastructure means the cost of creating these environments is cheap. Running and managing them not so much.

## In This Context

Container technology has taken us a long way to resolving the 'it works on my machine' problem. However, in a microservice environment, the number of dependencies for truly validating the functionality of service can still make this a big challenge.

- Mimicking production on a developer's laptop is often not feasible.
- Creating clusters and environments becomes easy with automation, but the cost, both monetary as well as resources to manage all the clusters can grow quickly.

## Therefore

By leveraging automation, and a modern cloud platform, environment's can be created on demand, and removed once they are no longer needed. There's no reason why we need to keep the old ways of having permanent (testing, qa, staging) environments.

- Add stages to the build pipeline to create a new environment for each deployment.
- Validation tests are automated against the newly created environment.
- A temporary URL can be made availble for any manual validation which needs to be done.
- The environments shoud be automatically removed, either after completion of the pipeline, or after a set period of time.

## Consequently

{:.plusminus}
- {:.plus} In the spirit of immutable infrastructure, having short lived on demand environments reduces the risk of configuration drift with long lived environments.
- {:.plus} Infrastrucutre automation gets frequently validated and optimisation of the automation becomes essential.
- {:.plus} The confidence of the build pipeline increases as all changes are validated against production like environments.
- {:.plus} Cloud costs are greatly reduced as we only run the environments when needed.
- {:.minus} If environments are not automatically removed, this can have the opposite effect on your cloud costs.
- {:.minus} When environments take too long to create, this can drastically slow down build pipelines. 

