---
layout: tag_post
title: Extension & Universality
tags: [machine-learning, science-and-epistemics]
---

One of the properties that you’d like a learning agent to have is that, if your old concepts work well, learning a new concept should _extend_ your knowledge but not _invalidate_ your old knowledge. Changes in your ontology should behave in a roughly predictable manner rather than a chaotic manner.  If you learn that physics works differently at very large or very small scales, this should leave classical mechanics intact at moderate scales and accuracies.

From a goal-based perspective, this means that if you make a _desirable_ change in ontology — let’s say you switch from one set of nodes to a different set — and you choose the “best” map from one ontology to another, in something like the Kullback-Leibler-minimizing sense described [here](https://intelligence.org/files/OntologicalCrises.pdf) — then when you take preimages of your “utility functions” on the new ontology onto the old ontology, they come out _mostly_ the same.  The best decision remains the best decision.

In the special case where the old ontology is just a subset of the new ontology, this means that the maps between them are a _restriction_ and an _extension.  _(For example, if we restrict (a, b, c, d, e) to the first three coordinates, it’s just the identity operation on those coordinates, (a, b, c); and if we extend (a, b, c) to (a, b, c, d, e), again the map is the identity on the first three coordinates.)  What we’d like to say is that, when we add new nodes to our ontology, then the function that computes _values_ on that ontology (the _f_ in [Part 3 ](https://srconstantin.wordpress.com/2015/06/08/epistemology-sequence-part-3-values-and-evaluation/)of this sequence) extends to a new _f_ on the new ontology, while keeping the same values on the old nodes.

For example; let’s say I have a regression model that predicts SAT scores as a result of a bunch of demographic variables. The “best” model minimizes the sum of squared errors. Sum of squared errors is my utility function.  Now, if I add a variable to my model, the utility function stays the same, it’s still “sum of squared errors”; so if adding that new variable changes the model but reduces the residuals, my old model “wants” to make the upgrade.  On the other hand, an ‘upgrade’ to my model that changes the utility function, like deciding to minimize the sum of squared errors plus the coefficient for the new variable, isn’t necessarily an improvement unless the “best” model by that criterion also shrinks the sum of squared errors relative to the original regression model.

From the goal-oriented perspective, the only changes you’d _want_ to make to your ontology are those which, when “projected” onto the old ontology, have you making the same “optimal” choices.

(These statements still need to be made precise. There may be a conjecture in there but I haven’t specified it yet. The whole business smells like [Hahn-Banach](https://en.wikipedia.org/wiki/Hahn%E2%80%93Banach_theorem) to me, but I could be entirely mistaken. The [universality of neural nets](http://www.dartmouth.edu/~gvc/Cybenko_MCSS.pdf) might be relevant to showing that this kind of a “rational learner” is _implementable _with neural nets in the first place. )
