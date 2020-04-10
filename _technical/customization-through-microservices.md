---
title: Customization Through Microservices
description: Description part 1
layout: pattern
---

![Customization Through Microservices]({{ site.baseurl }}/assets/images/Generic.png)

Description part 2

## Context

In a cloud based (SaaS) application, customization is generally an anti-pattern. However, there are certain areas, such as ERP and CRM platforms, where this is an essential feature of the system. A company with such a product, looking to migrate to a modern, SaaS, platform must be able to offer the same customization features to their customers.

## Problem

The goal of a SaaS platform is to leverage multi-tenancy, that is all users of the system share the same paltform. How then can we have custom code for each customer? Adding the custom code into the main application, as is usually done with legacy applications which are run on client's own servers, is not a viable option in a multi-tenant SaaS model.

- Custom code and features can quickly bloat a code base, as more clients are added.
- Isolating custom logic from each customer is challenging.
- High risk of customization code impacting the core functionality.
- Custom code is usually developed by a separate team, this cannot be able to affect other customers.

## Solution

By creating a well defined 'customization' interface (API), customer specific microservices can be created to execute all custom logic. The custom microservices are only called at designated points, and routing is handled by an internal API gateway or service mesh.

## Resulting Context

This pattern has the following benefits:

- Custom code is well contained within it's own microservice.
- If the custom code breaks it does not affect other users.
- We can set network boundaries, and resource limits on the custom microservices to create the necessary level of isolation.
- The core services need have no knowledge of the custom logic or microservices.

This pattern has the following drawbacks:

- This pattern can result in a increase in network traffic, and as a result latency as the amount of customization increases.

## Related Pattern

- Multi-tenancy
