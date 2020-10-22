---
title: Network Isolation
description: A key feature for having more granular control over connections to workloads.
layout: pattern
---

![Network Isolation]({{ site.baseurl }}/assets/images/cs.png)

Separate applications running on one platform are susceptible to attacks from others.

## In This Context

Within a container platform, we are encouraged to run multiple different systems, environments, shared by multiple teams or even customers.
These can span different applications, teams, environments (e.g. dev/staging) and even clients (multi tenant). While these separate services should not normally access each other across certain boundaries (e.g. Namespaces),
by default there is nothing blocking traffic (either malicious or by error) from crossing these boundaries.

## Therefore

By leveraging a feature such as NetworkPolicies in Kubernetes, we can block all unwanted traffic between services.

- Determine all expected traffic between your services. (A service mesh or tracing tool can generate this dynamically).
- Define rules to block all (other) traffic between services.
- Apply the created rules and monitor your applications for any problems created.
- (Optional) add logging for all blocked traffic
- For any unforeseen traffic, determine if it is a) intended or b) undesired <br/>
    a) -> Add a rule to allow the traffic, update your network topology<br/>
    b) -> Fix the application making the undesired access

## Consequently
{:.plusminus}
- {:.plus} We have created a much more secure solution.
- {:.plus} For any attacker who manages to compromise a service they are now severely limited in terms of damage they can due (#defenceInDepth)
- {:.plus} We are protected against mistakes made in development accessing services which should not be
- {:.plus} We have a clear and auditable picture of the actual network traffic on our environment
- {:.minus} Each change in the source, destination traffic must be configured in the network isolation tool
