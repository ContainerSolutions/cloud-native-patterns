---
title: Continuous Integration
description: Frequent integration of small iterative changes speeds overall delivery and improves the quality of the code
layout: pattern
---

![Continuous Integration]({{ site.baseurl }}/assets/images/continuous%20integration.png)

Many developers are working within the same codebase and need to integrate their changes.

## In This Context

When a team of developers works on a set of features that integrates only when all features are finished, the integration process tends to be very complex. The code base change is large, and in the meantime other devs have integrated separate large changes that can further complicate the integration. To increase productivity,devs often delay interim integration—which leads to a single “big bang” integration just prior to release. A minor bug or conflict that could have been easily caught in an interim integration can now end up delaying the entire release.

- Memory of the change you made fades with time, so delayed integration can increase difficulties.
- Chance of conflicts is smaller when the change is small.
- Frequent execution of the same task creates incentives for automation.
- It is very easy to lose trust in the system if reports are not available.

## Therefore

All developers integrate their changes at least once per day. Integration of all changes is done on a main codebase for each microservice. Code differences are small, less than one day of work, which leads to simpler integration.The main codebase is continually rebuilt and tested to ensure that every developer has functioning and up-to-date code to work with, which minimizes unexpected conflicts with any other newly integrated code.

- Introduce test automation and unit tests.
- Build each change and test it immediately.
- Immediately fix any broken build.
- Commit to the same mainline on the codebase.
- Must have good reporting.
- Use feature toggling.

## Consequently

Integration is a nonevent. Products are always in a releasable state.

{:.plusminus}
- {:.plus} Code is always good-quality, tested, and functional.
- {:.plus} Collaboration is easier.
- {:.plus} Minor bugs and conflicts are caught before they cause major problems.
- {:.minus} There is some overhead.
