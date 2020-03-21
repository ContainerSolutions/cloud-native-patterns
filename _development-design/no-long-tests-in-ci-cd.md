---
title: No Long Tests in CI/CD
description: Execute non-critical long-running tests in the background so they don’t block delivery to production
layout: pattern
---

![No Long Tests in CI/CD]({{ site.baseurl }}/assets/images/No%20long%20tests%20in%20CI-CD.png)

CI/CD is in place, and most tests are automated. Some are taking hours or even longer, and others require manual execution.

## In This Context

Delivering changes quickly is a major goal of the cloud native approach to delivering software.Long-running performance tests, reliability tests, and manual and other types of full-system tests can take too long and delay delivery for hours—rendering CI/CD less valuable. Instead of dozens or even hundreds of times a day, delivery frequency gets reduced to just a few times per day. Similarly, fixing a bug or problem goes from taking a few minutes to instead requiring several hours.

- Manual intervention can create very long delays.
- Frequent integrations require a fast build/test cycle.

## Therefore

Run your fastest tests earliest in the process. Schedule all tests that are manual, or which take longer than a few minutes to run, outside of the normal delivery process.If you have a test that is critical for functionality, however, it should be run asa blocking test.Mitigating risk is an equally important cloud native goal, which is why automated testing is a core tenet of the architecture. These two things need not conflict. There are strategies that allow adequate testing while enabling teams to still release quickly and constantly. Short-running tests can be incorporated into the pre-deployment process, while long-running tests can be executed in the background without blocking delivery to production.

- Run tests periodically post-delivery, and if a problem is found, either roll back the change or fix the problem and roll forward in a new release.
- Run long tests in parallel.
- Split the test automation into smaller test segments.

## Consequently

Testing does not delay or disturb delivery. Quality of the products is kept high by the right balance of ever-changing tests.

{:.plusminus}
- {:.plus} Non-blocking long-running tests reveal problems without slowing velocity.
- {:.plus} Release is quick and easy.+ Devs can deliver many times a day.
- {:.minus} Some issues can carry through to production.
- {:.minus} Requires strong roll back/roll forward protocol and procedures in place.
