---
layout: post
title: "Minimum Viable PaaS?"
date: 2012-10-22 12:05
comments: true
categories: PaaS
---
## What is a Minimum Viable PaaS?

### In one phrase
A what point an IaaS becomes a PaaS? When you forget there is an IaaS at all.

### Basis 
We all know the theory, the cloud mainly is broken into:

* IaaS - Infrastructure as a Service (Amazon, OpenStack, etc.)
* PaaS - Platform as a Service (Heroku, Cloudbees, etc.)
* SaaS - Software as a Service (Salesforce, Office 365, etc.)

IaaS brings machines, memories, CPU's, systems.

PaaS brings integration:
<!-- more -->
* Usually as system integration (Abstracting away the infrastructure).
* Maybe as architecture/applicative integration (Bringing Blocks that
  are not only used but compose the deployed product).
* Maybe as a development application (selling support to oil-up your
  dev process).

### Doubts
What the several PaaS offers do actually provide is fluctuting.

The IaaS providers themselves do offer some level of integration (some enter deeply into PaaS-land without really becoming one).

So: What is the minimal set of features that make a PaaS a PasS?

What is the minimum viable PaaS?

### My jab at an answer
My minimum feature set would be:

#### IaaS brokerage
If the PaaS is not an IaaS it should have a way to communicate with one! Which is a given: Nothing revolutionary.

#### IaaS abstraction
The PaaS user do not want to control how much CPU it needs, neither how much memory nor what OS does his virtual machine uses nor that it uses virtual machines at all.

He wants to deploy a product to the platform and have it "magically" handle those details.

Or failing that at least take sensible defaults for everything and mostly "just work".

#### Product installation
A corollary of *IaaS Abstraction* is that the end-user does not deploy a virtual machine, but his product only. His deploying interface is product oriented.

#### Product finding
At least internally, if the unit of a PaaS is a product, it should be able to find where its products are.

#### Simple scalability as a Service
Regardless of the PaaS' own Supervision the user should be able to manually ask for more resources should a sudden need of scalability arise.

IaaS should do that too, but PaaS should hide the "how": the user should ask for more horsepower, without worrying what that horsepower is (machines, memory etc.)

#### Load balancing as a Service
At some point scaling will mean having a product turn on several machines, the PaaS should load balance betwen those.

#### Monitoring
Not something highly developed (like loggly) but at least a way to know your product is down.

#### Configuration management
Not as an external service, but the brunt work of a PaaS is giving a working system completely configured.

That configuration will evolve, in all deployed systems.

The PaaS will need high amounts of configuration management (using tools like puppet or chef probably)

### What would be your answer?
Candid feedback welcome.
