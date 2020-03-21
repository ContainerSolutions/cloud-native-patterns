---
title: Reference Architecture
description: Provide an easily accessible document laying out a standardized system architecture for all teams to use for building their applications/components. This ensures higher architectural consistency and lowers development costs via better reusability
layout: pattern
---

![Reference Architecture]({{ site.baseurl }}/assets/images/Reference%20architecture.png)

The Core Team is designing the setup of the initial platform and the migration of the first few applications that will test it. The rest of the teams will start migrating soon and will need to understand the platform architecture.

## In This Context

When moving to cloud native, teams have no experience and no clear reference on the right ways to architect cloud native systems. When a transformation proceeds without a proper plan for standardizing the platform, each team will likely choose very different architecture for the particular piece it is in charge of building.This makes interpretation of components difficult and maintenance more complex,and will make it more difficult to move developers across teams due to steep learning curves among the different platforms. Furthermore, in the absence of both knowledge and easy solutions, teams may revert to well-known ways (biases) and significantly diminish the value of the transformation.

- It’s easier to reuse existing architecture.
- Some teams would never extend the original version.
- Given full freedom there will be many different architectures.
- It’s difficult to consider the whole system from within one team.

## Therefore

Document the architectural principles to be used in the company, educate the teams on the standardized way to build software in this system, and create anarchitecture review process to ensure consistency among teams.Standardizing the architecture early on paves the way for more rapid adoption while preventing chaos. This is an extension of the Vision First pattern: rather than making a bunch of random decisions to move the initiative forward, people with an understanding of how to build distributed systems software have helped make proper technical decisions.Providing good reference points coupled with clear architectural guidelines right from the start helps the teams to bootstrap the projects in better ways and may avoid costly mistakes.

- Make the architecture sufficiently high-level to allow flexibility for the teams to choose tools.
- Use demo apps as example implementations.
- Create a procedure to uniformly educate everyone who will be using the system.
- Review and help teams to improve their microservices to run optimally on the standardized platform.
- Include recommended languages and tools.
- Just because we are being creative and doing experiments doesn’t mean we should not be doing architecture.

## Consequently

Components are consistent across all teams and projects. There is a clear understanding regarding the platform and agreement over preferred application architecture styles. The current state of the platform is known, and it is open for improvements.

{:.plusminus}
- {:.plus} Easier to improve and maintain.
- {:.plus} Easier to onboard new devs.
- {:.minus} May limit freedom of choice.
