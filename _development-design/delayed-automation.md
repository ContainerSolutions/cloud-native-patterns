---
title: Delayed Automation
description: Automate processes only after a problem has been completely solved and the solution has been run manually a few times
layout: pattern
---

![Delayed Automation]({{ site.baseurl }}/assets/images/delayed%20automation.png)

The team is building a complex system that needs to support stress and a large and fluctuating number of users. The problem and the domain are not fully known. The solution is new and not easily uncovered.

## In This Context

Automation is essential for success in cloud native, but people tend to try to create a full and automated solution in the beginning before real pain points are uncovered(taking an academic approach rather than experimental). This leads to automation of the wrong thing when the problem is not fully understood. Or,paraphrasing Bill Gates, who describes this conundrum as “Crap in, crap out,only faster.”

- Universities teach to solve the problem in the “right” way.
- Engineers prefer automation versus manual work.

## Therefore

Understand the problem well, create a solution, make it work, and only then automate,scale, optimize, and improve.Before automating anything, first solve the problem manually. The team needs to seethe solution by doing it manually for a bit to experience and identify the pain points.Focus first on low-hanging fruit of automation (i.e., tasks that demand a lot of humantime and are easy to automate).

- Run the process manually a few times.
- Create a blueprint (a document with steps).
- Do crude automation first (experiments, then an MVP version).
- Optimize and scale.
- Continually improve.

## Consequently

Only the right things get automated. All the important and time-consuming tasks get automated eventually.

{:.plusminus}
- {:.plus} Scaled work becomes a well-understood process.
- {:.minus} Process is manual for a while.
