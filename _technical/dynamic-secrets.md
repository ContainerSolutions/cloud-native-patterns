---
title: Dynamic Secrets
description: Use a specific tool for managing and abstracting secret data from your applications.
layout: pattern
---

![Dynamic Secrets]({{ site.baseurl }}/assets/images/cs.png)

The team is building applications using distributed microservices architecture. The secrets required by multiple services and environments need to be managed in a manner that doesnt negatively impact agility or security.

## In This Context

Building a distributed, microservices architecture. Many services require passwords, keys, tokens or other sensitive data which cannot be stored in plain text.

Teams tend to end up with one of two sets of problems:

##### High Security - Low Agility

- All credentials are managed (manually) be a security team. Nobody usually knows where this team actually sits, there only interface is an obscure ticket filing system.
- Developers must submit requests to have the necessary credentials created and made available to their application.
- Developers invent 'hacks' to work around the missing credentials locally or on a dev environment.

##### High Agility - Low Security

- Dev teams are responsible for managing their own secrets.
- Credentials are often omitted or set to defaults (admin:admin) in all but production.
- Production credentials are often accessible to nearly everyone, resulting in a large security risk.
- Secrets in this case are almost never rotated.

In both cases:

- Upon deploying their application to a new environment (e.g. local dev to integration or qa to prod) the applications most often fail because the credentials or how the credentials are accessed differs across each environment.
- Applications are heavily coupled to the specific tool and method for retrieving credentials.

## Therefore

Use a specific tool for managing and abstracting secret data from your applications.

- Abstract the tool as well as the method for retrieving secret data from your services.
- Adding/requesting a new secret (e.g. database password) should be self service.
- Secret data is mounted as a volume for applications to read locally.
- Secrets should be rotated often.
- Secret data must be encrypted at rest.

## Consequently

Secrets can be managed without any negative impact to agility without compromising security. 

{:.plusminus}
- {:.plus} Developers do not have to worry about how or from where to retrieve secret data.
- {:.plus} The security team does not need to slow down or stop the release process.
- {:.plus} Secret data is well protected, ideally no human will ever see the actual secrets.
- {:.plus} Risk is greatly reduced as even if compromised, secrets can be easily revoked or rotated.


