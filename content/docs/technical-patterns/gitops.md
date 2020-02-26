# Pattern Name - GitOps

## Context

You have setup all your infrastructure as code (see #InfrastructureAsCode pattern). You want to deliver changes quicker, but require security and reliability.

## Forces

* Multiple tools, technologies
* Changing landscape (deployment environments, clusters, etc)
* Often need multiple clusters and deployment environments
* Manual actions are slow and error prone

## Problem

How do you coordinate application delivery and infrastructure management in a controlled, secure manner without reducing velocity?

## Solution

Use a Git repository to store the current (desired) state of your infrastructure and applications in production. An in cluster service to monitor the repository and adjust the current state as needed.

## Actions

* Store all infrastructure configuration in a declarative format in a Git repository
* Deploy a service (operator) into your cluster to monitor repo and apply changes
* All infrastructure changes are made via branch/pull requests on the repository

## Consequences

* We end up with a single source of truth for the (desired) state our infrastructure and applications
* All manual access and changes must be removed. This needs to be enforced and requires education across teams.
* We use existing (tested) tools (Git) and workflows for managing changes to our system.
* We can much more easily scale out, e.g. to multiple clusters environments.
* We have a built-in approval process and auditing of all changes.

## Example - ?
