# Design notebook for week ending November 30, 2014

## Description

This week I eventually settled down on a design. Since the last update to the project repository, I decided on how to handle circular systems: each rule can have the same inputs and outputs, and will then be run until a fixed point is reached. Additionally, there can be cycles of multiple rules as long as the following constraints are obeyed:

1. All of the variables in the dependency loop (not necessarily ones that go outside the loop) must be *sets*, not just individual values.
2. All of the inputs that use these variables must be `foreach` inputs.
3. Each assignment to one of these must be a *union* assignment, not a *replace* assignment. I have not discussed the difference in the past, but I figure this is clear.

## Questions

**What is the most pressing issue for your project? What design decision do
you need to make, what implementation issue are you trying to solve, or how
are you evaluating your design and implementation?**

I think this answers all of the major design decisions. There are still implementation decisions to make, given that I have not really started implementing yet.

**What questions do you have for your critique partners? How can they best help
you?**

The fundamental rule of elegant design, especially in a constrained time budget situation like this: is there anything left to take away? I have sets and unions as a required part of the “downloading from the internet” scenario.

**How much time did you spend on the project this week? If you're working in a
team, how did you share the labor?**

This is a bit difficult to answer. Not that much, but it’s also a short week.

## Post-critique summary

## Post-critique reflection
