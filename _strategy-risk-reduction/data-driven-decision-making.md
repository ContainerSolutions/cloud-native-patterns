---
title: Data-Driven Decision Making
description: Collect data, extract patterns and facts, and use them to make inferences to drive objective decision making
layout: pattern
---

![Data-Driven Decision Making]({{ site.baseurl }}/assets/images/data-driven%20decision%20making.png)

A company is moving to cloud native and sees the complexity and number of components growing exponentially. Each component is built separately. Competitors are changing products on a daily basis.

## In This Context

Managers make decisions based on their expectations from previous experience,which might not apply in the new and unknown environment of a cloud native system.

- Long development and release cycles (six months to a year, or even longer) that are typical in the Waterfall development approach result in products that are no longer relevant by the time they reach the customer.
- Software systems and users are complex systems. It’s impossible to predict behavior.
- In hierarchical organizations managers protect their status by knowing everything and deciding everything.
- Technically it is easy to collect data.
- Measuring the wrong things may lead to bad results.

## Therefore

Make product decisions based on data collected from actual users (observability,measure what matters).Data can be collected automatically by embedding the data collection tools into theplatform and all applications before they are released to customers. However, developers need to be careful not to be overly reliant on, or trusting of, user feedback/data.Users often don’t know what they want, especially in regards to radical innovation.

- Apply the A/B Testing pattern to evaluate different options by exposing them to the real customers.
- Similarly the Learning Loop pattern builds on Data-Driven Decision Making.
- Collect feedback and clicks/business measurements following the release of changes.

## Consequently

The team can quickly make decisions based on objective measurements.

{:.plusminus}
- {:.plus} Instead of arguing on direction, team can set up experiments and measure.
- {:.minus} It is easier to follow the herd.
- {:.minus} It is not always easy to measure and interpret the right things.
- {:.minus} Sometimes data and users are wrong, and the team needs to trust their instinct and pivot to a radical change.
