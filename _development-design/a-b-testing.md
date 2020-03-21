---
title: A/B Testing
description: Comparing multiple versions of something (a feature, new functionality, UI, etc.) underreal customer use conditions quickly gives useful data about which performs better
layout: pattern
---

![A/B Testing]({{ site.baseurl }}/assets/images/a-b%20testing.png)

A company has a working cloud native infrastructure in place and is aiming to deliver a lot of useful functionality to its customers. Teams are proficient, and all the tech and processes are in place.

## In This Context

There is no practical way to predict how customers will respond to changes. In the absence of actual customer usage data, design and implementation decisions must be based on guesswork and intuition. Since our intuition is not perfect and full of biases, we may not get the best possible results.

- People don’t always know what they need/want.
- Delivering fast without adjusting the product based on measurement and feedback will change nothing.
- It’s impossible to make logical decisions in an unknown environment.
- There are unlimited variations and combinations of possible solutions.

## Therefore

Prepare multiple versions of a solution to a challenge/problem and present them to randomized small portions of the client base. Measure the customer response in terms of value for them, and based on that choose the solution.

- Famous Google example of testing 41 shades of blue for its toolbar1 to find which inspired the most consumer clicks—because, for Google, clicks equal revenue.
- The Obama campaign raised more money by using A/B testing to choose the most effective messaging.
- Need to provide business people with the opportunity to run the A/B test experiments themselves, and an accessible way for them to do so.

## Consequently

You now have an easy way to test assumptions live in a real-world environment.Instead of making guesses or assumptions regarding which of two ideas, implementation strategies, etc., is better, a team can quickly put together a simple prototype with two or more versions and release them to small subsets of real customers. Based on customer response, the team can choose the more appropriate/preferred solution.This way many options could be tested while costs are ultimately saved because onlythe best option is ever fully implemented.

{:.plusminus}
- {:.plus} Customers see response to their needs.
- {:.plus} If something doesn’t work, you can easily roll back to previous version.
- {:.minus} Human insight might be sidelined when user response data is followed blindly.
