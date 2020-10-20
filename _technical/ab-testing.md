---
title: A/B - Testing
description: Description part 1
layout: pattern
---
![A/B - Testing]({{ site.baseurl }}/assets/images/cs.png)

The general concept behind A/B testing is to create an experiment with a control group and one or more experimental groups which receive alternative versions.
A/B testing is a way to compare two versions of a single variable, typically by testing a users's response to variant A against variant B, and determining which of the two variants is more effective.

## In This Context

It needs to be ensured that each member of the control group belongs exclusively to one experiment within a given experiment, where one group is always designated the “default group”. This group represents the control group, which receives the same experience as all other customers not in the test. As soon as the test is live, metrics need to be tracked which are specific and are of importance to determine if an experiment is running successful or not. In order to to draw statistically meaningful conclusions, you need to have enough participants. 

From the participant’s point of view, each member could potentially be part of several A/B tests at any given time, provided that none of those tests conflict with one another (i.e. two tests which modify the same area of a App in different ways).

Multiple teams might run multiple tests at any given time, which might even be conflicting.

Technically you need to find a way to split customer traffic to the different versions of your application.

## Solution

##### Split URLs

This is the classical approach and prevent issues with SEO. It was recommended by Google. As an example: [ab-test-123](https://cn-patterns/ab-test-123/a) .

##### Server-side

Users are grouped on the server when a page is requested. A cookie is then set to ensure the user is in the right controll group, and it’s used to render an interface with whatever experiments the user is in. Using a cookie allows you to also do multivariate tests, feature toggles, parallel experiments etc. 
From the perspective of an user, this is one of the best options, because the performance impact is negligible. If you have a CDN the use of cookies can limit the benefits of a CDN. Cookies will introduce variation in requests (especially if users can enter multiple experiments), and it will lead to cache misses, and content will not be served from the edge servers of your CDN and the request will be served by the origin servers.

##### On the edge

If you use a CDN the edge servers of your CDN if you render all your experiments and then cache it, when a user loads your website, the cached response is served, after the edge worker removes the HTML that is not applicable to the user that requests it. If you care about performance, this is the best choice.

##### Client-Side

If your test don’t have access to the infrastructure, or you want to have maximum flexibility, client-side A/B testing is an option. It means that either no interface is rendered, or the original interface, and as soon, or slightly before this happens, the experiments are activated, and the interface is augmented based on whatever variant the user is in. This choice often makes sense when you do not have access to an engineering team, and are using external tools to run experiments. However, it’s often the worst choice in terms of performance. 

## Consequently

{:.plusminus}
- {:.plus} It allows to test hypothesis and gather data to make decision on the direction to go
- {:.plus} Code that don't add value doesn't get into the master branch and the code base remains clean
- {:.minus} Complexity will increase to create the possibilty of doing the test
- {:.minus} Additional tools might be needed
