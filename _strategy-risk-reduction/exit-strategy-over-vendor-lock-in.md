---
title: Exit Strategy Over Vendor Lock-in
description: Public cloud or other major product vendors can handle all aspects of building and operating a cloud native platform, and their tools are often excellent—but when committing to a vendor/technology/platform, it’s important to identify an alternate solution and any costs associated with switching over
layout: pattern
---

![Exit Strategy Over Vendor Lock-in]({{ site.baseurl }}/assets/images/exit%20strategy%20over%20vendor.png)

Companies need to use tools/products provided by vendors (commercial or open source communities) but are afraid to get locked into a single vendor. Some industries require supporting multiple choices for some key platforms, tools, or technologies used to develop company products. Being fully committed to a single tool or technology can drive costs up or hinder tech progress down the line.

## In This Context

Committing to a single-vendor (or simply a single large solution) creates reliance upon their ongoing stability and availability and pricing, but the cost of maintaining active alternative/backup options is prohibitive.This leads to full dependency on the vendor. If the vendor is in trouble or when a better option becomes available on the market, the company cannot afford to switch—which leads to using unmaintained or inferior technology.

- There is risk in any choice.
- Every decision can be reversed; it’s just a matter of cost.
- Some industries require multiple vendors for each solution.

## Therefore

Instead of blindly refusing to commit to a single vendor, explore the options for a second migration, if necessary, and what they would cost. Then make an educated decision based on the tradeoff between short-term gains from a vendor with the best tool and the long-term risk of migrating out of it if needed. Often lower costs and higher productivity outweigh the risk.

Consider implementing architectural changes that will reduce the cost of migration in case it will be required. Such changes can be inexpensive if done in the earliest stages of the project, and they can significantly reduce the risk of the future migration.

- Prepare a migration plan just in case.
- Consider reducing dependencies that significantly increase risk.
- AWS could be a big help now.
- Closed ecosystems often offer an excellent set of tools/options.
- Invest in commonly used tools and technologies that may become industry standards.

## Consequently

The team can focus on getting the maximum performance out of and benefit from each tool, and they are aware of what it would cost to migrate to alternative solutions should the need arise.

{:.plusminus}
- {:.plus} There is a good understanding of the different backup options.
- {:.plus} High-level plan is in place for a major migration scenario.
- {:.minus} There is always risk when only one tool is used.
