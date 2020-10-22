---
title: GitOps
description: GitOps - a single source of truth for infrastructure configuration
layout: pattern
---

![GitOps]({{ site.baseurl }}/assets/images/Generic.png)

You have setup all your infrastructure as code (see #InfrastructureAsCode pattern).

## In this Context

You want to deliver changes quicker, but require security and reliability. How do you coordinate application delivery and infrastructure management in a controlled, secure manner without reducing velocity?

- Multiple tools, technologies
- Changing landscape (deployment environments, clusters, etc)
- Often need multiple clusters and deployment environments
- Manual actions are slow and error prone

## Therefore

Use a Git repository to store the current (desired) state of your infrastructure and applications in production. An in cluster service to monitor the repository and adjust the current state as needed.

- Store all infrastructure configuration in a declarative format in a Git repository
- Deploy a service (operator) into your cluster to monitor repo and apply changes
- All infrastructure changes are made via branch/pull requests on the repository

## Consequently

You get the single source of truth about your infrastructure and an easy way to audit changes to it.

{:.plusminus}
- {:.plus} We end up with a single source of truth for the (desired) state our infrastructure and applications
- {:.plus} We use existing (tested) tools (Git) and workflows for managing changes to our system.
- {:.plus} We can much more easily scale out, e.g. to multiple clusters environments.
- {:.plus} We have a built-in approval process and auditing of all changes.
- {:.minus} All manual access and changes must be removed. This needs to be enforced and requires education across teams.
- {:.minus} Secret management is quite challenging and very often requires use of 3rd party tools.
- {:.minus} Not designed for programmatic updates, multiple CI processes can end up writing to the same GitOps repo, causing conflicts.

