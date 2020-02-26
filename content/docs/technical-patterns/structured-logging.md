# Pattern: Structured Logging
## Context: 
Once you’re alerted to the fact that something is wrong in your production environment, the next step is to determine what causes the problem. For this Logging is used. Logging can provide critical information that helps you quickly determine which function is causing the issue.
## Problem:
In case of an application problem, to be able to:
* Alert on conditions that require attention.
* Start a root cause analysis and diagnose those issues.
* For regression.
## Solution:
Forwarding of all exceptions to a centralized system that aggregates and tracks exceptions. Based on standard RFC 5424 on how to log from applications setup of the severity of logs is required and only severity 0 or 1 are events which should trigger an alarm:

* 0 Emergency: the system is unusable
* 1 Alert: action must be taken immediately
* 2 Critical: critical conditions
* 3 Error: error
* 4 Warning: warning
* 5 Notice: normal but significant
* 6 Informational: informational
* 7 Debug: debug-level messages

As the RFC is a standard there are standard libraries available for different programming languages/frameworks. Logging itself an agnostic practice and is not coupled to the programming language or framework in use.

Example:
https://godoc.org/github.com/influxdata/go-syslog/rfc5424

## Resulting Context
This pattern has the following benefits:
* Logging allows to easily locate what caused an issue 
This pattern has the following drawbacks:
* Additional components are required
* Tend to generate a lot of noise if configured wrong
* ...
### Related patterns
* Observability - Alerts on the fact that something is not working
* Alerting
