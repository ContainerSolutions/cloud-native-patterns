# Pattern: Metrics over Logs

## Context

A team is moving from a legacy style monolithic system to a cloud native platform. Traditionally most information from applications gets pushed into logs. Cloud Native systems offer a better approach to gaining insight into our applications.

## Problem

When building applications, traditionnally we send all relevant information out as logs. Monitoring or metrics were mainly used for the health of our physical infrastructure. Applying this pattern to a modern distributed system composed of dozens of components results in a petabytes of mostly useless data.

- The lack of well defined structure makes parsing logs nearly impossible across multiple services.
- 99% of log data is never used, or seen and serves only to run up cloud costs.
- Logs are not a viable set of data on which we can build alerts or notifications.
- There is no clear view on the actual health of our system.
- Metrics based on a single instance (e.g. application container or cluster node) are meaningless.

## Solution

The purpose of each type of data, logs and metrics, must first be well established. Logs should be used as a secondary method for gaining further knowledge on a specific incident (i.e. debugging). Metrics are a way to get a holistic view on your applications and system as a whole.

- Data sent to logs should be minimized as much as possible.
- Relevant global metrics must be defined.
- For each service, the owner must define metrics which are relevant and make them available to the monitoring system.
- Metrics should comply with the Open Metrics (<https://openmetrics.io/)> standard.

## Resulting Context

This pattern has the following benefits:

- Log data is greatly simplified and reduced (saving cost).
- When logs are needed (to debug an issue) finding the relevant logs becomes much easier.
- An accurate view on the health of your system is available.
- The standardized metrics can easily be shipped to a variety of monitoring platforms and tools.
- Comprehensive alerts can be built on top of the available metrics.

## Related Pattern

- Structured Logging
- Observability
- Alerting
