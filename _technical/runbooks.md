---
title: Runbooks
description: Description part 1
layout: pattern
---

![Runbooks]({{ site.baseurl }}/assets/images/Generic.png)

Description part 2

## Context:
When an alarm is triggered by breaching a defined threshold or condition a runbook links to information or standard procedures for handling an incident. For this teams have created a useful runbook that is actively maintained and integrated into the alerting infrastructure for easy reference.
## Problem:
In case of an incident, an effective runbook allows to effectively manage and troubleshoot a system by providing a context for the engineer on duty.
## Solution:
By using your post-mortems as a record of what actions and activities have worked, you can then leverage the recorded actions (that fixed the problem) to build your runbooks. You need to implement a rules engine using an if this, then that where the runbook at a minimum should include:

WHAT: Triggered the alarm (which tools and which threshold)

HOW: To start to remediate the problem (i.e. scale-up, roll-back, etc.)

WHO: Who is the product team which needs to be contacted in case of escalation.

WHERE: Where can the on-call engineer find information like:
* documentation
* update statuses
* post questions
* etc.
## Resulting Context:
This pattern has the following benefits:
* It reduces or eliminates the time it takes for your team to “dig” for your runbooks in a file repository or a wiki link. 
* It also reduces the stress accompanied with solving a complex problem at midnight.
This pattern has the following drawbacks:
* It requires discipline to create them
* The creation is hard to automate
## Related Pattern:
* Alerting
* Post-Mortem
