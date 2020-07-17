---
layout: tag_post
title: Strong AI Isn't Here Yet
tags: [machine-learning]
---

I’ve heard a fair amount of discussion by generally well-informed people who believe that bigger and better deep learning systems, not fundamentally different from those which exist today, will soon become capable of general intelligence — that is, human-level or higher cognition.

I don’t believe this is true.

In other words, I believe that if we develop strong AI in some reasonably short timeframe (less than a hundred years from now or something like that), it will be due to some conceptual breakthrough, and not merely due to continuing to scale up and incrementally modify existing deep learning algorithms.

To be clear on what I mean by a “breakthrough”, I’m thinking of things like neural networks (1957) and backpropagation (1986) [ETA: actually dates back to 1974, from Paul Werbos’ thesis] as major machine learning advances, and types of neural network architecture such as LSTMs (1997), convolutional neural nets (1998), or neural Turing machines (2016) as minor advances.

I’ve spoken to people who think that we will not need even minor advances before we get to strong AI; I think this is very unlikely.

**Predicate Logic and Probability**

As David Chapman points out in [Probability Theory Does Not Extend Logic](https://meaningness.com/probability-and-logic), one of the important things humans can do is predicate calculus, also known as first-order logic. Predicate calculus allows you to use the quantifiers “for all” and “there exists” as well as the operators “and”, “or”, and “not.”

Predicate calculus makes it possible to make general claims like “All men are mortal”.  Propositional calculus, which consists only of “and”, “or”, and “not”, cannot make such statements; it is limited to statements like “Socrates is mortal” and “Plato is mortal” and “Socrates and Plato are men.”

_Inductive reasoning _is the process of making predictions from data. If you’ve seen 999 men who are mortal, Bayesian reasoning tells you that the 1000th man is also likely to be mortal. _Deductive reasoning _is the process of applying general principles: if you know that all men are mortal, you know that Socrates is mortal.  In human psychological development, according to [Piaget](https://en.wikipedia.org/wiki/Piaget's_theory_of_cognitive_development), deductive reasoning is more difficult and comes later — people don’t learn it until adolescence.  Deductive reasoning depends on predicate calculus, not just propositional calculus.

It’s possible to view propositional calculus as an extension of probability theory. For instance, MIRI’s [logical induction paper](https://arxiv.org/pdf/1609.03543.pdf) constructs a (not very efficient) algorithm for assigning probabilities to all sentences in a propositional logic language plus some axioms, such that the probabilities learn to approximate the true computed values faster than it would take to compute the truth of propositions.  For example, if we are given the axioms of first-order logic, the logical induction criterion gives us a probability distribution over all “worlds” consistent with those axioms. (A “world” is an assignment of Boolean truth values to sentences in propositional calculus.)

What’s not necessarily known is how to assign probabilities to sentences in _predicate _calculus in a way consistent with the laws of probability.

Part of why this is so difficult is because it touches on questions of _ontology_. To translate “All men are mortal” into probability theory, one has to define a sample space. What are “men”?  How many “men” are there? If your basic units of data are 64×64 pixel images, how are you going to divide _that _space up into “men”?  And if tomorrow you upgrade to 128×128 images, how can you be sure that when you construct your collection of “men” from the new data, that it’s consistent with the old collection of “men”?  And how do you set up your statements about “all men” so that none of them break when you change the raw data?

This is the problem I alluded to in [Choice of Ontology.](https://srconstantin.wordpress.com/2015/04/30/choice-of-ontology/)  A type of object that behaves properly under ontology changes is a _concept_, as opposed to a _percept _(a cluster of data points that are similar along some metric.)  Images that are similar in Euclidean distance to a stick-figure form a percept, but “man” is a concept. And I don’t think we know how to implement concepts in machine-learning language, and I think we might have to do so in order to “learn” predicate-logic statements.

[Stuart Russell wrote in 2014,](https://people.eecs.berkeley.edu/~russell/papers/ipmu14-oupm.pdf)


    _An important consequence of uncertainty in a world of things: there will be uncertainty about what things are in the world. Real objects seldom wear unique identifiers or preannounce their existence like the cast of a play. In the case of vision, for example, the existence of objects must be inferred from raw data (pixels) that contain no explicit object references at all. If, however, one has a probabilistic model of the ways in which worlds can be composed of objects and of how objects cause pixel values, then inference can propose the existence of objects given only pixel values as evidence. Similar arguments apply to areas such as natural language understanding, web mining, and computer security._


    _The difference between knowing all the objects in advance and inferring their existence and identity from observation corresponds to an important but often overlooked distinction between closed-universe languages such as SQL and logic programs and open-universe languages such as full first-order logic._

How to deduce “things” or “objects” or “concepts” and then perform inference about them is a hard and unsolved conceptual problem.  Since humans _do _manage to reason about objects and concepts, this seems like a necessary condition for “human-level general AI”, even though machines do outperform humans at specific tasks like arithmetic, chess, Go, and image classification.

**Neural Networks Are Probabilistic Models**

A neural network is composed of nodes, which take as inputs values from their “parent” nodes, combine them according to the weights on the edges, transform them according to some transfer function, and then pass along a value to their “child” nodes. All neural nets, no matter the difference in their architecture, follow this basic format.

A neural network is, in a sense, a simplification of a Bayesian probability model. If you put probability distributions rather than single numbers on the edge weights, then the neural network architecture can be interpreted [probabilistically](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.29.274&rep=rep1&type=pdf). The probability of a target classification given the input data is given by a likelihood function; there’s a prior over the distribution of weights; and as data comes in, you can update to a posterior distribution over the weights, thereby “learning” the correct weights on the network.  Doing gradient descent on the weights (as you do in an ordinary neural network) finds the maximum likelihood values of the posterior distributions on the weights in the Bayesian network paradigm.

What this means is that neural networks are _simplifications _or _restrictions _of probabilistic models. If we don’t know how to solve a problem with a Bayesian network, then _a fortiori_ we don’t know how to solve it with deep learning either (except for considerations of efficiency and scale — deep neural nets can be much larger and faster than Bayes nets.)

We don’t know how to assign and update probabilities on predicate statements using Bayes nets, in a coherent and general manner. So we don’t know how to do that with neural nets either, except to the degree that neural nets are simpler or easier to work with than general Bayes nets.

For instance, as Thomas Colthurst points out in the comments, message passing algorithms don’t provably work in general Bayes nets, but do work in feedforward neural nets, which don’t have cycles. It may be that neural nets provide a _restricted domain _in which modeling predicate statements probabilistically is more tractable. I would have to learn more about this.

**Do You Feel Lucky?**

If you believe that learning “concepts” or “objects” is necessary for general intelligence (either for reasons of predicate logic or otherwise), then in order to believe that current deep learning techniques are already capable of general intelligence, you’d have to believe that deep networks are going to figure out how to represent objects somehow under the hood, _without human beings needing to have conceptual understanding of how that works_.

Perhaps, in the process of training a robot to navigate a room, that robot will represent the concept of “chairs” and “tables” and even derive general claims like “objects fall down when dropped”, all via reinforcement learning.

I find myself skeptical of this.

In something like image recognition, where convolutional neural networks work very well, there’s human conceptual understanding of the world of vision going on under the hood. We know that natural 2-d images generally are [fairly smooth](https://srconstantin.wordpress.com/2014/05/14/the-world-is-simple/), so expanding them in terms of a multiscale wavelet basis is efficient, and that’s pretty much what convnets do.  They’re also inspired by the structure of the visual cortex.  In some sense, researchers know some things about how image recognition _works _on an algorithmic level.

I suspect that, similarly, we’d have to have understanding of how concepts work on an algorithmic level in order to train conceptual learning.  [I used to think I knew how they worked](https://srconstantin.wordpress.com/2015/05/27/epistemology-sequence-part-2-concepts/); now I think I was describing high-level percepts, and I _really don’t know what concepts are_.

The idea that you can throw a bunch of computing power at a scientific problem, without understanding of fundamentals, and get out answers, is something that I’ve become very skeptical of, based on examples from biology where [bigger drug screening programs and more molecular biology understanding don’t necessarily lead to more successful drugs.](http://www.nature.com/nrd/journal/v11/n3/full/nrd3681.html)  It’s not in-principle impossible that you could have enough data to overcome the problem of multiple hypothesis testing, but modern science doesn’t have a great track record of actually doing that.

Getting artificial intelligence “by accident” from really big neural nets seems unlikely to me in the same way that getting a cure for cancer “by accident” from combining huge amounts of “omics” data seems unlikely to me.

**What I’m Not Saying**

I’m not saying that strong AI is impossible in principle.

I’m not saying that strong AI won’t be developed, _with _conceptual breakthroughs.  Researchers _are _working on conceptually novel approaches like [differentiable computing](https://deepmind.com/blog/differentiable-neural-computers/) and [program induction](http://web.mit.edu/cocosci/Papers/Science-2015-Lake-1332-8.pdf) that might lead to machines that can learn concepts and predicates.

I’m not saying that narrow AI might not be a very big deal, economically and technologically and culturally.

I’m not trying to malign the accomplishments of people who work on deep learning. (I admire them greatly and am trying to get up to speed in the field myself, and think deep learning is pretty awesome.)

I’m saying that _I don’t think we’re done_.
