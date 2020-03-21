---
title: Automated Testing
description: Shift responsibility for testing from humans (manual) to automated testing frameworks so the quality of the released products is consistent and continuously improving, allowing developers to deliver faster while spending more of their time improving features to meet customer needs
layout: pattern
---

![Automated Testing]({{ site.baseurl }}/assets/images/automated%20testing.png)

CI and CD are in progress. Legacy code is being refactored to MS, and the team is aiming to deliver changes a few times a day.

## In This Context

Humans are too slow and inconsistent to be a blocking factor in the pipeline for deployment to production.Any human handover or task performed by a human will significantly reduce the number of changes a team can deliver and increase the time required to deliver them.

- Humans can never be as fast as computers.
- Poor testing quality undermines trust in the delivery process, and testing is a waste of time.
- People tend to delay and combine changes if each delivery is risky.
- When tests are slow, people tend to avoid running them as frequently as they should.

## Therefore

Automate all the testing required to take any product change to production.Most functionality should be tested using fast and local unit tests, integration tests can ensure that components are working well together, and only a small portion of the test coverage needs to be on the system UI levels. All long-running and manual tests should be gradually refactored and automated, and they should not block consistent flow of changes to production.

- Use testing pyramid.
- Long tests should not block release.
- Manual and long-running processes happen only in background.
- Continuously add and change tests.
- Consider test-driven development.
- Add advanced in-product testing like A/B, canary, blue/green, etc.

## Consequently

The team can trust that the delivery process will catch most issues and that changes will flow to production quickly.

{:.plusminus}
- {:.plus} The team is ready to deliver changes and take the risks.
- {:.plus} Developers write tests, which gives deeper insight into the code.
- {:.minus} If there is a team in charge of manual testing, they may need to be retrained for new responsibilities.
