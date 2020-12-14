---
title: Network Isolation
description: Leverage a tool to provide more granular control over connections to workloads.
layout: pattern
---

![Network Isolation]({{ site.baseurl }}/assets/images/network%20issolation.png)

An organisation is utilising a container platform which runs multiple different systems, environments, shared by multiple teams or even customers.

## In This Context

Multiple applications, teams, environments (e.g. dev/staging) and even clients (multi tenant) are sharing the platform. While these separate services should not normally access each other across certain boundaries (e.g. Namespaces),
by default there is nothing blocking traffic (either malicious or by error) from crossing these boundaries. 
Separate applications running on one platform can be susceptible to attacks from others.

## Therefore

By leveraging a feature such as NetworkPolicies in Kubernetes, we can block all unwanted traffic between services.

#### Actions
- Determine all expected traffic between your services. (A service mesh or tracing tool can generate this dynamically).
- Define rules to block all (other) traffic between services.
- Apply the created rules and monitor your applications for any problems created.
- (Optional) add logging for all blocked traffic
- For any unforeseen traffic, determine if it is a) intended or b) undesired <br/>
    a) -> Add a rule to allow the traffic, update your network topology<br/>
    b) -> Fix the application making the undesired access

## Consequently

Network security is enhanced within the shared platform with the ability to track subsequent changes.

{:.plusminus}
- {:.plus} We have created a much more secure solution.
- {:.plus} For any attacker who manages to compromise a service they are now severely limited in terms of damage they can due (#defenceInDepth)
- {:.plus} We are protected against mistakes made in development accessing services which should not be
- {:.plus} We have a clear and auditable picture of the actual network traffic on our environment
- {:.minus} Each change in the source, destination traffic must be configured in the network isolation tool
