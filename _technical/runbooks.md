---
title: Runbooks
description: They provide a set of instructions, documents, which help to identify quickly the root cause for the incident and apply solution to it. 
layout: pattern
---

![Runbooks]({{ site.baseurl }}/assets/images/cs.png)

In case of an incident, an effective runbook allows to effectively manage and troubleshoot a system by providing a context for the engineer on duty.

## In This Context:
When an alarm is triggered by breaching a defined threshold or condition a runbook links to information or standard procedures for handling an incident.
For this teams have created a useful runbook that is actively maintained and integrated into the alerting infrastructure for easy reference.

## Therefore:
By using your post-mortems as a record of what actions and activities have worked, you can then leverage the recorded actions (that fixed the problem) to build your runbooks.
The good runbook at a minimum should include answers for following questions:

**WHAT:** Triggered the alarm (which tools and which threshold)\
**HOW:** To start to remediate the problem (i.e. scale-up, roll-back, etc.)\
**WHO:** Who is the product team which needs to be contacted in case of escalation.\
**WHERE:** Where can the on-call engineer find information like: documentation, update statuses, etc.
## Consequently

{:.plusminus}
- {:.plus} It reduces or eliminates the time it takes for your team to “dig” for your runbooks in a file repository or a wiki link. 
- {:.plus} It also reduces the stress accompanied with solving a complex problem at midnight.
- {:.minus} It requires discipline to create them
- {:.minus} The creation is hard to automate
