---
layout: post
title: "What is an elastic datastore?"
date: 2012-10-31 13:57
comments: true
categories: BigData 
---

## In one phrase
Elastic datastores handle *stress* losing neither *consistency* nor *availability*. 

## In detail
To understand that you need to know what is *Elasticity* exactly!

### So, What is *elasticity* ?
<!-- more -->
We have two kinds :

#### General Elasticity

« Ability of *something* to receive a *stress* without deforming. »

Think about a rubber band: you can take it with your hands, stretch it
and abandon it: the band will return to its original shape.

Commonly used in physics.

#### Point elasticity

« *rate* of how much *something* follows another. »

Think about two objects, attach each other by a rubber band:
when one of them moves, the other follows. Not immediately, not in the
same speed (because in the beginning the rubber band will stretch
instead of pull) but follows anyway.

Commonly used in mathematics.

### What is an *Elastic* ?

*Something* with a *high* elasticity.

### So, when is a datastore elastic?

When it shows, in any form, a high degree of *elasticity*. Some common examples:

#### Scaling up and down

If we consider the *General elasticity* :

« Ability of *something* to receive a *stress* without deforming. »

Our *something*: the datastore. Its *stress*: the force of a high
number of concurrent users (say: your blog got featured highly on
reddit).

The datastore would be elastic if it *both*:

1. Scaled up during the stress of that spike in number of visits (say:
   used more nodes in the cluster).
2. Scaled down after the spike back to its original form (say:
   returned by himself to its original number of nodes)

Not scaling at all would of course not qualify as elastic, but only
scaling up is not enough.

#### *Accepting* schema changes

Again we consider the *General elasticity* :

« Ability of *something* to receive a *stress* without deforming. » 

Our *something* : the datastore. Its stress : The data schema changes a lot.

Here our datastore would be elastic if it could handle the changes of
schema on the data and always use its own schema in the end (avoiding deformation).

This is possible in datastores that are effectively schema-less (like mongo).

#### *Adapting to* schema changes

Let’s revisit the same “the data schema changes a lot” problem, but
this time we use *point elasticity*:

« *rate* of how much *something* follows *another*. »

The datastore would be elastic if it would be able to take the new
data schema into consideration and (after some time) evolve its own
schema to handle the difference.

This is the approach used by Graph databases to handle the emergence of
relationships that are unknown initially.

## Remember

Every Elastic has its *Yield strength* : the point of wich, the
*stress* is just too much and the *elastic* loses all *elasticity*.

Every rubber band has a point where it breaks.

You should seek the *Yield strength* of your datastore system under
your production architecture•
