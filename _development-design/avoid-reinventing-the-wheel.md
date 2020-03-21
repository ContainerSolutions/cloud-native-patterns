---
title: Avoid Reinventing the Wheel
description: When possible, use open source or purchase commercial solutions for any need that is not your actual core business instead of trying to custom-build perfect tools
layout: pattern
---

![Avoid Reinventing the Wheel]({{ site.baseurl }}/assets/images/avoid%20reinventing%20the%20wheel.png)

A team is in the middle of a cloud native transition and missing some functionality.Out-of-the-box solutions are available on the market, although the team is capable of creating its own.

## In This Context

Many development teams tend to create their own tools/solutions even when reasonable alternatives are available. Custom solutions are expensive and slow to build, difficult to maintain, and quick to become outdated. They don’t take advantage of developments in the industry, and the eventual cost is high.

- Internal devs are most content to build core products.
- Tools that are not core business rarely get full attention.
- Everything that is not business logic or user interaction is not your core business.
- Every off-the-shelf product is a core business for the company or the community that makes it.
- Cloud native ecosystem is growing very fast.
- Many engineers think “they know better.”
- Open source attracts many devs.

## Therefore

Use existing tools whenever possible, even when the fit isn’t perfect.

Whether commercial or open source, existing products are typically better quality,better maintained, and more frequently extended than anything you can build yourself.Spend most of the development time on your core business functionality. This will significantly increase the time and effort available for investment into the core business parts that separate your company from the competition, while making sure that the rest of the components are easily maintainable and up to the latest industry standards.

- Make use of third-party libraries, off-the-shelf products, and existing architectures when possible.
- Focus your internal resources on delivering your core business.
- Build only if nothing else is available; give preference to an open source solution unless it’s related to your core business.
- Seek the fullest possible solution; trying to fit together a variety of open source solutions, each addressing a separate business function, can lead to maintaining a complex environment of many moving parts.

## Consequently

The team can focus on core business.

{:.plusminus}
- {:.plus} New functionality is constantly introduced with third-party product releases.
- {:.plus} Quality of off-the-shelf products is typically higher.
- {:.plus} There is external product/user support.
- {:.plus} Easier to hire people when using common tools.
- {:.minus} Some problems are too specific for any off-the-shelf solution to address.
- {:.minus} Third-party products are often expensive.
- {:.minus} Less control over functionality.
