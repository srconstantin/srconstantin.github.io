---
layout: tag_post
title: Choice Of Ontology
tags: [science-and-epistemics]
---

I noticed an interesting phenomenon while reading[ this paper](http://circres.ahajournals.org/content/114/1/101.full) about a gene therapy that was intended to treat advanced heart failure.

The paper (which documents a Phase I/II study) found an 82% reduction in the risk of cardiac events in the high-dose group vs. the placebo group, with a p-value of 0.048. Weakly significant, but a big effect size.

On the other hand, if you look at the raw numbers you see that some people have a lot of cardiac events, and some have few or none.  If you divide people into “healthy” vs. “unhealthy”, where “unhealthy” people have at least one cardiac event within a year, and “healthy” people don’t, then the placebo group had 7 healthy and 7 unhealthy patients, while the high-dose group had 7 healthy and 2 unhealthy patients.

If you do a one-sided t-test of this, you get a non-significant 0.07 p-value.

And intuitively, it makes _sense_ that 7 out of 14 unhealthy patients vs 7 out of 9 unhealthy patients could very easily be a fluke.

How you frame the problem, what you consider to be an “event” in your probability space, matters. Do you count cardiac events? Mostly healthy vs. mostly unhealthy people? People with no cardiac events vs. people with any cardiac events? (the latter gives you p=0.089).

One way of framing it is that you posit some kind of hierarchical model.  In this case, your risk of having a cardiac event is drawn from a probability distribution which is something like a mixture of two gamma distributions, one with a “low risk” parameter and one with a “high risk” parameter.

You could make a generative model to test the null hypothesis. Under the assumption that the therapy doesn’t work, you could randomly choose the size of the “high risk” vs. “low risk” population, and then for each patient, draw to see whether they’re high risk or low risk, and then draw again (repeatedly) from the appropriate gamma distribution to get their pattern of cardiac events.  Sampling from this can give you the posterior probability distribution of the actual data given the null hypothesis.

You could even make the number of clusters in your mixture, or the cutoffs of the clusters, random variables themselves, and average over different models.  That’s not really _eliminating_ the fact that choice of model matters, it’s just pushing your agnosticism up a meta-level; but it may be general enough to be _practically_ like model-agnosticism (e.g. adding more levels of hierarchy to the model might eventually cease to change the answer to “is this therapy significantly effective?” Note that you’re only getting p-value differences of a few percent even when we’re only tweaking a single parameter.   At some point I should try this empirically and see how much difference added model flexibility actually makes.)

But there’s a basic principle here which I see in a lot of contexts, where the output of a statistical algorithm is dependent on your choice of ontology.  And, I think, your choice of ontology is ultimately dependent on your _goals_.  Do I want to measure reduction in number of heart attacks or do I want to measure number of people who become heart-attack-free? There can’t be an answer to that question that’s wholly independent of my priorities.  Even averaging over models is essentially saying “over a wide range of possible priority structures, you tend to get answers to your question lying in such-and-such a range.”  It doesn’t mean you couldn’t construct a really weird ontology that would cause the algorithm to spit out something completely different.
