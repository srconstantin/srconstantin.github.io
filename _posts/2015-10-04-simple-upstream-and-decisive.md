---
layout: tag_post
title: Simple, Upstream, and Decisive
tags: [cancer, medicine, science-and-epistemics]
---


Lewis Thomas’s classic 1974 essay, [“The Technology of Medicine”](http://biologywatcher.tumblr.com/post/119091944920/lewis-thomas-the-technology-of-medicine), argued that there are three kinds of “technology” in medicine.



*   nontechnology, or “supportive therapy” — basically nursing and reassurance and caring for patients, but not directly affecting the course of disease. Indispensable, expensive, but not really problem-solving.
*   halfway technology — compensating for the damage done by disease when we do not know how to affect its course. Thomas uses organ transplantation as the main example here, as well as all cancer treatment, including surgery, irradiation, and chemotherapy.  It is also very expensive.
*   “decisive technology”, which genuinely reverses or prevents disease. Antibiotics and immunizations are the key examples of this, as are vitamin supplements for vitamin deficiencies, and treatment of endocrine disorders with hormone supplementation. “The point to be made about this kind of technology-the real high technology of medicine–is that it comes as the result of a genuine understanding of disease mechanisms, and when it becomes available, it is relatively inexpensive, and relatively easy to deliver.”

This categorization reminds me of an essay I like about the difference between [solving a problem and managing a problem.](https://www.fourmilab.ch/hackdiet/e4/)


    _“The world of the manager is one of problems and opportunities. Problems are to be managed; one must understand the nature of the problem, amass resources adequate to deal with it, and “work the problem” on an ongoing basis. Opportunities are merely problems that promise to pay off after sufficient work…An engineer believes most problems have solutions. A solution might not be achievable in the short term, but he’s sure somewhere, somehow, inside every problem there lurks a solution. The engineer isn’t interested in building an organisation to cope with the problem. Instead, the engineer studies the problem in the hope of finding its root cause. Once that’s known, a remedy may become apparent which eliminates the need to manage the problem, which no longer exists.”_

In Thomas’s classification, nontechnology and halfway technology are “management” approaches to illnesses, while decisive technology is an “engineering” approach.  If you want to actually _cure_ a disease, eradicate it from Planet Earth, you have to have an engineering approach.  Otherwise you’ll be managing it forever.

James Watson (yes, [that one](https://en.wikipedia.org/wiki/James_Watson), who has spent the last forty years researching cancer), argues a [similar case](http://rsob.royalsocietypublishing.org/content/3/1/120144.full) about cancer research in particular.

The decades of the War on Cancer have seen a vast expansion of our understanding of the genetics of cancer; we now know several hundred different genes whose mutations give rise to cancer, and increasing amounts about the molecular pathways that regulate cell growth and differentiation.  We also know that cancer cells develop resistance to most treatments over time as part of this process of accumulating mutations and increasingly abnormal growth patterns.

The most popular approaches to developing cancer drugs tend to involve attacking the growth promoting pathways (such as HER2, RAS, RAF, MEK, ERK, PI3K, AKT and mTOR). But slowing the growth of cancer cells is a priori likely to fail; given that cancer cells adapt, we expect them to develop resistance to such methods. This drives researchers towards increasingly complex cocktails of drugs and “personalized” genomic solutions, in a game of whack-a-mole that can consume arbitrary amounts of resources investigating complex molecular networks, for little practical benefit.  Watson argues that we should focus on strategies that completely kill cancer cells, stop them from dividing, or prevent them from developing resistance — such as Myc inhibitors and p53-activating drugs such as the diabetes drug metformin.

Cancer cells are less genetically stable than normal cells.  This is the principle by which radiation therapy works; it introduces noise into the genome, and because cancer cells are more sensitive to noise than normal cells, the radiation kills the tumor faster than it kills the rest of you. Most traditional chemotherapy also works by introducing “noise”, in the form of reactive oxygen species that disrupt the genome.  Rapidly dividing cells, like cancer cells, suffer more than normal cells (except for normal cells that also divide rapidly, like hair and bone marrow; this is why chemo makes your hair fall out and compromises the immune system.) Of course, these are imperfect solutions, since cancer often becomes resistant to radiotherapy and chemotherapy. Watson’s thesis is that cancer cells protect themselves against reactive oxygen species via antioxidants, and attacking this key ability will make them generically more sensitive to all kinds of cancer treatments; it will essentially make randomness work in your favor against cancer.

Whether or not this theory is valid, the general heuristic seems to be correct. If you want to _solve_ rather than _manage_ cancer, you want an effect simple enough and universal enough that even if there are unknown unknowns (there is always another regulatory gene yet to be discovered) your treatment will still work. You don’t want a treatment strategy that depends on getting every last epicycle right.

However, (to be cynical for a moment) if you wanted to maximize the flow of funding in the long term, you _might_ want to increase complexity without bound…

The classic Hanahan and Weinberg paper, [The Hallmarks of Cancer](http://www.sciencedirect.com/science/article/pii/S0092867400816839), and its [sequel paper](http://www.sciencedirect.com/science/article/pii/S0092867411001279), lay out a related model of cancer formation.  The key abnormalities in the development of cancer (which can occur in any order), are



*   self-sufficiency in growth signals
*   insensitivity to anti-growth signals
*   evading apoptosis
*   limitless replicative potential
*   angiogenesis
*   metastasis

This model has a few critical implications for cancer treatment.

The first consequence is that we should not have high confidence that a treatment that attacks only one of these six factors will cause remission.  If the abnormalities can develop in any order, and if acquiring one abnormality makes it easier to acquire others, then blocking one doesn’t necessarily block cancer from becoming metastatic.

The second consequence is that early-stage cancers are easier to kill than late-stage cancers; catching cancer early or preventing it should be more effective than attacking one of the “downstream” consequences of the transition to a cancerous state.  (A major difficulty with this strategy is regulatory: new cancer drugs must usually be tested after conventional chemotherapy fails, so we might never know if an early-stage “chemopreventative” drug would work.)

A third consequence, paradoxically, is that all these changes make cancer cells more vulnerable in certain ways. More reproduction means that their energy demands are higher and their genomes more unstable. Cancer cells use much more glycolysis than normal cells (the famous [Warburg effect](https://en.wikipedia.org/wiki/Warburg_effect)) and are more vulnerable to genetic damage.  In particular for treating late-stage cancers, it would make sense to focus on the fragility caused by out-of-control growth itself (such as inhibiting glycolysis) rather than trying to slow growth.

In general, we should look for successful treatments (of any disease, including cancer), to be _simple, upstream, and decisive._

Simple, because complexity and expense can often be a sign of compensating for continuing damage or omitted factors (like attacking one but not all of the “hallmarks of cancer.”)  Simplicity is also a guard against abuse of multiple hypothesis testing; too many conjunctive details suggest cherry-picking or statistical artifacts.

Upstream, in the sense of focusing on the causal bottleneck, rather than cleaning up after its manifold effects.

Decisive, because effective medical technology works _completely_.  In other words, look for tumor death, not just shrinkage or slowed growth; look for big effect sizes; look for actual survival improvements, not just changes in some intermediate biomarker or other. Decisiveness is even more important if we consider the impact of statistical malfeasance; it’s much easier for a researcher to massage data into looking just barely significant than to show a clear, dramatic, qualitative result.

Bigness is _tempting_.  (As a data scientist, I can attest to that.)  Vast quantities of data, infinitely complex models, arbitrary flexibility, all look exciting and powerful.  And there’s the unspoken siren song of overfitting: _look, with so many degrees of freedom, you literally can’t be wrong! You can do cool high-tech shit with no risk of embarrassing yourself!_  But when it comes to getting things done, as I’ve found even in mundane business settings, this is exactly the wrong mentality; the scientific method is about embarrassing yourself as quickly as possible.

“Simple, upstream, and decisive” is a way of counteracting the temptation towards hiding your failures in bigness.  Of course, it’s a heuristic, not anything like a scientific theory; but viewed through this lens, some research approaches look _a priori_ improbable while others look fruitful.

If _some approaches to cancer research are much more likely to work than others, but the scientific community systematically favors the unsuccessful approaches_, then the difficulty of curing cancer isn’t just a lack of low-hanging fruit, it’s a strategic problem.  (I haven’t demonstrated yet that this is in fact the case; I hope to provide evidence for that later.)  If it’s a strategic problem and we can distinguish between more-promising and less-promising approaches, then strategic funding might be able to make an impact on cancer even given the vast amount of resources already being poured into it.
