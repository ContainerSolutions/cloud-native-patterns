---
title: Lift and Shift at the End
description: It’s important not to approach a cloud native transformation by simply attempting a full“lift and shift” of your existing system onto the cloud. But it can be smart to move some intact pieces of it at the very end
layout: pattern
---

![Lift and Shift at the End]({{ site.baseurl }}/assets/images/lift%20and%20shift%20at%20the%20end.png)

Most of your existing apps have been re-architectured and moved to the new platform.Some old stuff remains, but it is stable and doesn’t change too often.

## In This Context

Companies often first approach a cloud native transformation with the belief that it simply means migrating their existing system and processes onto the cloud. This is so common that it’s earned the name “lift and shift” and it categorically does not work if you try to do this at the beginning of a transformation. An organization has to change not only its technology but also its structure, processes, andculture in order to succeed with cloud native.When organizations do a lift and shift at the very beginning, they expect it will be a quick and easy project to execute, since the applications themselves do not change significantly. In most cases, however, it ends up being a large and expensive initiative requiring triple the anticipated time and budget. This is due both to the complexity related to the underlying platform and the new knowledge required for operating on the cloud. Such a painful experience may lead to delays or even total cancellation of the following refactoring initiatives.

- An expensive project to rebuild/refactor an app may prevent further improvements on app.
- “Moving to cloud” may look like a quick win.
- Public cloud vendors may offer incentives for you to move—lift and shift—inappropriately early in the transformation initiative.

## Therefore

Move functioning and stable legacy apps as-is from data centers to the new cloudn ative platform without re-architecture at the very end of the initiative.An organization has to change not only its technology but also its structure, processes,and culture in order to succeed with cloud native. Once the cloud native transformation is close to the end, however, it could be valuable to move any remaining parts of the old system to the new platform. This avoids the extra cost of supporting the legacy platform as well as gaining at least some benefits of the new platform for the old applications.At the end of a successful refactoring, when the last few, rarely changing applications remain, the team continues to refactor them all, ignoring the piling costs and few benefits coming from such refactoring.

- Keep old tech like VMS and monoliths intact on the new platform.
- Spend minimal effort.
- Create easy ways to strangle remaining old apps.
- Lift and shift only apps that almost never change but cannot be retired easily.

## Consequently

You can retire the old platform, shut down the servers, and end the datacenter contracts.

{:.plusminus}
- {:.plus} Benefits are gained from some features on new platform.
- {:.minus} But this is a missed opportunity to update/re-architect these legacy apps/services,which will likely remain the same forever.
- {:.minus} Some teams are stuck with old tech.
