---
title: Customization Through Microservices
description: Use a customization API to handle customizations
layout: pattern
---

![Customization Through Microservices]({{ site.baseurl }}/assets/images/cs.png)


In a cloud based (SaaS) application, customization is generally an anti-pattern. However, there are certain areas, such as ERP and CRM platforms, where this is an essential feature of the system. A company with such a product, looking to migrate to a modern, SaaS, platform must be able to offer the same customization features to their customers.

## In This Context

The goal of a SaaS platform is to leverage multi-tenancy, that is all users of the system share the same platform. How then can we have custom code for each customer? Adding the custom code into the main application, as is usually done with legacy applications which are run on client's own servers, is not a viable option in a multi-tenant SaaS model.

- Custom code and features can quickly bloat a code base, as more clients are added.
- Isolating custom logic from each customer is challenging.
- High risk of customization code impacting the core functionality.
- Custom code is usually developed by a separate team, this cannot be able to affect other customers.

## Therefore

By creating a well defined 'customization' interface (API), customer specific microservices can be created to execute all custom logic. The custom microservices are only called at designated points, and routing is handled by an internal API gateway or service mesh.

## Consequently

Customization can be offered to customers without negatively impacting the core services or other customers.

{:.plusminus}
- {:.plus} Custom code is well contained within it's own microservice.
- {:.plus} If the custom code breaks it does not affect other users.
- {:.plus} We can set network boundaries, and resource limits on the custom microservices to create the necessary level of isolation.
- {:.plus} The core services need have no knowledge of the custom logic or microservices.
- {:.minus} This pattern can result in a increase in network traffic, and as a result latency as the amount of customization increases.


