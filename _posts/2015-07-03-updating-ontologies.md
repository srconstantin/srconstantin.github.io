---
layout: tag_post
title: Updating Ontologies Based On Values
tags: [science-and-epistemology, cog-psych]
---

What’s a _good_ ontology?

Well, the obvious question is, _good relative to what?_

Relative to your values, of course. In the [last post](https://srconstantin.wordpress.com/2015/06/08/epistemology-sequence-part-3-values-and-evaluation/) I talked about how, given an ontology for describing the world, you can evaluate a situation.  You compute the inner product

f(N)*V

where V represents a value function on each of the concepts in your ontology, and f(N) is a function of which concept nodes are “active” in a situation, whether by direct perception, logical inference, predictive inference, association, or any other kind of linkage.  For instance, the situation of being a few yards away from a lion will activate nodes for “tan”, “lion”, “danger”, and so on.

If you can evaluate situations, you can choose between actions. Among all actions, pick the one that has the highest expected value.

One particular action that you might take is _changing your ontology_.  Suppose you add a new node to your network of concepts.  Probably a generalization or a composition of other nodes. Or you subtract a node.  How would you decide whether this is a good idea or not?

Well, you build a model _using your current ontology_ of what would happen if you did that. You’d take different actions.  Those actions would lead to different expected outcomes. You can evaluate how much you like those outcomes _using your current ontology and current values_.

For  modeling the world, the kinds of things you might optimize for are accuracy (how often does your model come up with correct predictions) and simplicity (how few degrees of freedom are involved.)  This is often implemented in machine learning with a [loss function ](http://www.mit.edu/~9.520/spring11/slides/class02.pdf)consisting of an error term and a regularization term; you choose the model that minimizes the loss function.

Notice that, in general, changing your ontology _is_ changing your values. You can’t prioritize “civil rights” if you don’t think they exist.  When you learn that there are other planets besides the Earth, you might prioritize space exploration; before you learned that it was possible, you couldn’t have wanted it.

The question of value stability is an important one. When should you self-modify to become a _different kind of person_, with different values?  Would you take a pill that turns you into a sociopath?  After all, once you’ve taken the pill, you’ll be happy to be free of all those annoying concerns for other people.  Organizations or computer programs can also self-modify, and those modifications can change their values over time.  “Improvements” meant to increase power or efficacy can cause such agents to change their goals to those that present-day planners would find horrifying.

In the system I’m describing, proposed changes are always evaluated _with respect to current values_.  You don’t take the sociopath pill, because the present version of you doesn’t want to be a sociopath. The only paths of self-modification open to you are those where future states (and values) are backwards-compatible with earlier states and values.

The view of concepts as [clusters in thingspace](http://lesswrong.com/lw/nl/the_cluster_structure_of_thingspace/) suggests that the “goodness” of a concept or category is a function of some kind of metric of the “naturalness” of the cluster.  Something like the ratio of between-cluster to within-cluster variance, or the size of the margin to the separating hyperplane.  The issue is that choices of metric matter enormously.  A great deal of research in image recognition, for example, involves competing choices of similarity metrics. The best choice of similarity metric is subjective until people agree on a _goal_ — say, a shared dataset with labeled images to correctly identify — and compete on how well their metrics work at achieving that goal.

The “goodness” or “aptness” of concepts is a real feature of the world. Some concepts divide reality at the joints better than others. Some concepts are “natural” and some seem contrived.  [“Grue” and “bleen”](https://en.wikipedia.org/wiki/New_riddle_of_induction) are awkward, unnatural concepts that no real human would use, while “blue” and “green” are natural ones.  And yet, even blue and green are not _human_ universals (the Japanese _[ao](https://en.wikipedia.org/wiki/Ao_(color)) _refers to both blue and green; 17th century English speakers thought lavender was [“blue”](https://en.wikipedia.org/wiki/Lavender's_Blue) but we don’t.)  The answer to this supposed puzzle is that the “naturalness” of concepts depends on _what you want to do with them_.  It might be more important to have varied color words in a world with bright-colored synthetic dyes, for instance; our pre-industrial ancestors got by with fewer colors.  The goodness of concepts is _objective_ — that is, there is a checkable, empirical fact of the matter about how good a concept is — but only _relative_ to a goal, which may depend on the individual agent.  Goals themselves are _relative to_ ontology.  So choosing a good ontology is actually an iterative process; you have to build it up relative to your previous ontology.

(Babies probably have some very simple perceptual concepts hard-coded into their brains, and build up more complexity over time as they learn and explore.)

It’s an interesting research problem to explore when major changes in ontology are desirable, in “toy” computational situations.  The early MIRI paper [“Ontological crises in artificial agent’s value systems”](https://intelligence.org/files/OntologicalCrises.pdf) is a preliminary attempt to look at this problem, and says essentially that _small_ changes in ontologies should yield “near-isomorphisms” between utility functions.  But there’s a great deal of work to be done (some of which already exists) about _robustness_ under ontological changes — when is the answer spit out by a model going to remain the same under perturbation of the number of variables of that model?  What kinds of perturbations are neutral, and what kinds are beneficial or harmful?  Tenenbaum’s [work](http://cims.nyu.edu/~brenden/LakeTenenbaum2010CogSci.pdf) on learning taxonomic structure from statistical correlations is somewhat in this vein, but keeps the measure of “model goodness” separate from the model itself, and doesn’t incorporate the notion of goals.  I anticipate that additional work on this topic will have serious practical importance, given that model selection and feature engineering is still a labor-intensive, partly subjective activity, and that greater automation of model selection will turn out to be valuable in technological applications.

_Most of the ideas here are from [ItOE](http://www.amazon.com/Introduction-Objectivist-Epistemology-Expanded-Edition/dp/0452010306); quantitative interpretations are my own._
