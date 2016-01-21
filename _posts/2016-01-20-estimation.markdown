---
published: true
title: Agile Estimation
layout: post
---
## Absolute Estimation Sucks.

Our brains aren't designed for it resulting in all sorts of cognitive biases such as [Optimism Bias & Planning Fallacy](https://en.wikipedia.org/wiki/Optimism_bias#Policy.2C_planning.2C_and_management). Their impact on project planning, timescale estimation and predicting project success are explored by Daniel Kahneman in [Thinking Fast and Slow]( https://en.wikipedia.org/wiki/Thinking,_Fast_and_Slow).

This means that estimation errors aren't randomly distributed around the true value (for example a normal distribution with the true value as the mean) but are systematically wrong.

The British Government has even compiled a [report](https://www.gov.uk/government/uploads/system/uploads/attachment_data/file/191507/Optimism_bias.pdf) showing how it effects public projects. This even includes suggested values to compensate for Optimism Bias.

## Relative Estimation can be more accurate

Kahneman talks about how relative estimation is one way of avoiding these biases.

A practical example used in the [two factor estimation webcast](http://www.oreilly.com/pub/e/3592) is the time it took to build two bridges, the brooklyn and covington-cincinnati bridges. It is hard to estimate the time it took from first principles, but easier to estimate the other when one is known, based on their relative length and complexity.

This is the foundation of agile estimation using story points.

## This is counter to __Legacy__ Estimation best practice 

Relative Estimation, particularly using macro-estimates (i.e. length of bridge instead of number of tasks, people, or time worked) is hard for business to accept since it runs counter to the __legacy way of estimating of 
- breaking down the the project into work to be done to the smallest possible level of detail
- estimating each task
- adding it all back together again.

This approach feels wrong due to another bias, [precision bias](https://en.wikipedia.org/wiki/Precision_bias) , where we assume precise estimates and figures are more accurate. This is why every _experienced_ product, finance and sales manager provide forecasts to 2 decimal places. It shows you that a formula has been used, as opposed to 'Wild Ass Guesses'.

## Why Story Points?

Story points are designed to help promote the following
- Relative estimation, since they aren't based on how long you think it will take you to do something
- Avoid conflating time spent with work done, another common mistake. 
- Avoiding precision to acknowledge they are estimates

When used to measure velocity it acknowledges that work is delivered by teams, that are not just the sum of the person days available. This includes such factors as
-- new team members getting up to speed
-- not every team member produces at the same rate (aka super star developer)
-- some team members don't code but help deliver, such as QA for example
-- some development practices, such as pairing increase productivity whilst reducing work done.

The last point is also why it is often recommended to use the Fibonacci sequence.

## The use of feedback loops to improve estimates

Story points become more useful when they are used as part of feedback loops.

Estimating is a complex task, and not just due cognitive biases. This is when unknown unknowns come into effect including both unknown tasks (aka undiscovered work) and unknown impediments come into effect.

The recommended way to try and deal with complexity is by using feedback loops.

When we use story points and velocity, the goal is to use a feedback loop to
1. account for systemic biases impacting both work estimates and the amount of work that can be delivered by a team.
2. adapt this to take into account environmental factors.

However, in my opinion, this is often easier said than done.

## Story Point Anti-Patterns

Like any process or method there are anti-patterns, where the process is followed without the desired results, normally to a misunderstanding of how the process delivers benefit.

Ones I have seen include
- resizing estimates for delivered work after the fact (hindsight bias ignores that the error is not systemic and will be repeated)
- estimate from first principles and convert between time worked and story points (
can be impossible to do when man/days are used to estimate the team velocity)
- don't gather metrics
- don't use metrics as feedback for velocity
- use decimal places in estimates (too much accuracy)
- conflation of user stories and tasks