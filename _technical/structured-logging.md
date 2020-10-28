---
title: Structured Logging
description: A way to get information about what is going on with your application in a structured form.
layout: pattern
---

![Structured Logging]({{ site.baseurl }}/assets/images/cs.png)

Structured Logging can provide critical information that helps you quickly determine which function is causing the issue.

## In This Context: 
Once you’re alerted to the fact that something is wrong in your production environment, the next step is to determine what causes the problem. For this Logging is used. 

## Therefore:
Forwarding of all exceptions to a centralized system that aggregates and tracks exceptions.
Based on standard RFC 5424 on how to log from applications, setup of the severity of logs is required and only severity 0 or 1 are events which should trigger an alarm:

- 0 Emergency: the system is unusable
- 1 Alert: action must be taken immediately
- 2 Critical: critical conditions
- 3 Error: error
- 4 Warning: warning
- 5 Notice: normal but significant
- 6 Informational: informational
- 7 Debug: debug-level messages

As the RFC is a standard there are standard libraries available for different programming languages/frameworks. Logging itself an agnostic practice and is not coupled to the programming language or framework in use.

## Consequently

{:.plusminus}
- {:.plus} Logging allows to easily locate what caused an issue 
- {:.minus} Additional components are required
- {:.minus} Tend to generate a lot of noise if configured wrong

