---
title: Strangle Monolithic Organization
description: Just as the new tools, technologies, and infrastructure gradually roll out over the course of a transformation initiative, the organization and its teams must also evolve to work with them properly
layout: pattern
---

![Strangle Monolithic Organization]({{ site.baseurl }}/assets/images/Strangle%20monolithic%20organisation.png)

A cloud native transformation is in progress and some teams are moving to cloud native, while others may not move to cloud native for a long time.

## In This Context

Migrating an existing company to the cloud can take years, and it happens very gradually.There are two types of moves that rarely work. First, trying to move everyone over at once does not lend itself to good training. Without a solid background in the newtech, teams will be less effective and get frustrated over time or fall back on old habits that don’t work well in cloud native. If the cultural and organizational change is not supported to evolve equally along with the cloud native technology, this also creates frustration.Second, simply leaving one part of the organization in legacy while everyone else moves to cloud native stratifies the company so that the teams that never get moved to cloud native are stalled professionally. They’ll never get to play with the cool new tech and build modern developer skills if they are left behind to babysit the legacy system. This, naturally, leads to frustration, resentment, and reduced motivation, not to mention difficulty hiring and retaining engineers.

- Cloud native transformation takes a long time.
- When people learn something, they need to apply it very soon.
- Tech and org/culture misalignment leads to frustration.
- People are motivated by hope of future improvements or frustrated by lack of hope.

## Therefore

Move the teams from the legacy organizational structure to the new one gradually(Gradual Onboarding pattern). Restructure teams and change from hierarchy shortly before the new onboarding to the cloud native platform when it is fully ready.This is an organizational version of Martin Fowler’s architectural strangler pattern: Slowly strangle the process, and Waterfall cultural relics like specialized teams, alongwith the monolith itself. The two systems, old and new, can coexist well during the migration process. Once complete, the remaining pieces of the legacy system can be ported over to the new cloud native platform (Lift and Shift at the End) and gradually refactored into microservices until the old monolith is no more, and the maintainers are now experienced with cloud native.

- Educate constantly.
- Promote experimentation.
- Shift from hierarchy to tribes and delegation.
- Avoid training and restructuring if the team is not planning to move to cloud native soon.
- Create a plan for all legacy teams but execute only when the move is close.

## Consequently

The old system keeps working as always while the new one is built, and teams are gradually moved over. Teams get restructured and retrained only when it is time for them to actually move. While you are on the old platform you keep delivering with excellence; then you move to the new one and deliver equally well there.

{:.plusminus}
- {:.plus} There is a clear plan for all the teams.
- {:.plus} Organizational/cultural changes are aligned with tech changes.
- {:.plus} Original and new cultures are coexisting but only temporarily until the full cloud native transfer is complete.
- {:.minus} Potential clashes between teams.
- {:.minus} Legacy teams could be disappointed by lack of change.
