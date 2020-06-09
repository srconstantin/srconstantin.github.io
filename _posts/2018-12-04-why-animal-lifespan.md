
---
layout: tag_post
title: Tradeoffs in Experimental Design: Why Animal Lifespan Studies?
tags: [aging, lit-review]
---

![kaplanmeier]({{ site.baseurl }}/images/kaplanmeier.png)

LRI's research begins by testing potential anti-aging drugs _in animals, _and using _lifespan _as the primary endpoint -- trying to ascertain if the drugs make animals live longer.  

Currently we're doing this in mammals, in experiments that will take years to complete, with a handful of drugs selected from the research literature. Our future plans for invertebrate drug screens will also involve animal lifespan studies, testing many more drugs on shorter-lived animals to see if they extend life.

Why did we choose animal lifespan studies as the primary test of whether a drug "works"?

There are other ways to conduct aging research, which have different benefits and disadvantages.

If you're concerned that animal biology might not translate well to humans, you can use human data rather than animal data.  

But, of course, you can't really test a wide range of drugs on people to see if they make people live longer -- that would take decades and cost an exorbitant amount.  

You can try to find a viable aging _biomarker _as a proxy for survival -- something you can measure with a blood test, and quickly check if your drug improves in humans.  There's a well-known[ methylation pattern](https://www.ncbi.nlm.nih.gov/pubmed/24138928) (Horvath, 2013) that correlates with age, and other groups are working on developing aging biomarkers based on proteomics, cellular morphology under microscopic imaging, gene expression, or other types of biological data.  

This has the advantage of being definitely based on human biology. 

The disadvantage is that these biomarkers are necessarily _correlational _in origin.  You need a dataset including age and mortality, and you're usually learning which mathematical composite of measured biomarkers (like the expression of various genes) best predicts an individual's remaining survival time. This is a regression problem, and like all regression problems, it's vulnerable to gaps in our causal knowledge. 

Maybe, for instance, some pattern of altered gene expression represents the body's protective response as it tries to fight off a disease.  That pattern will correlate with earlier mortality, but if you develop a drug that inhibits the protective pattern, it won't make the patient any healthier, because you're "fixing" the body's defense mechanisms, not the problem they're defending against.

The only safe assumption in biology is that there's more going on than current science understands.  This is why LRI is wary of proxy measures and composite biomarkers.  They're useful, but they're also hard to interpret and verify.

Some research groups and organizations are happy to conduct animal studies, but prefer mechanistic endpoints rather than lifespan.  For instance, people working on discovering senolytic drugs often do experiments on mice where the endpoint variable is the reduction in the number of senescent cells that the drug can produce.  Since we know from other studies that removing senescent cells (through genetic modification, for instance), can reverse many age-related diseases and symptoms of aging as well as extending lifespan, we can much more quickly evaluate drugs if we can test whether they affect a _mechanism _known to be involved in aging, without having to take the expense and time involved in a full lifespan study.

This is a valid approach, especially when (as in the case of cellular senescence) someone has demonstrated that the mechanism plays a causal role in aging and that reversing the mechanism has clear anti-aging properties.  But it's still something of a longer chain of inference than directly testing the effect of the drug on lifespan and direct symptoms of aging (tumor burden, hair loss, kyphosis, motor and cognitive function).  We're still betting, to some degree, on our model of how aging works.  And in biology, those models are continually being revised. 

It wasn't so long ago that drug candidates were being reported as potential aging preventatives because they had antioxidant properties; then we found that many antioxidants _don't _prolong life, and that reactive oxygen species aren't straightforwardly "bad for you" (among other things, they're involved in the body's defenses against cancer).

Betting too hard on any one mechanism is, we believe, taking a dangerous gamble.  It's worth the time to look at simple, ground-level endpoints like mortality and aging-related symptoms, while still doing some supplemental tests for mechanism so we can understand how the drug works, rather than focusing on mechanism first, at the risk of not actually getting the healthspan improvements we care about.

We'd like to discover drugs with _both _effective outcomes and well-understood mechanisms, but the former can occur before the latter, as the examples of aspirin, digitalis, and vaccination show. Accidental discoveries abound in the history of medicine.  And even drugs that supposedly work according to a known mechanism don't always work because of that mechanism alone -- e.g. Gleevec isn't _just _a Bcr-Abl inhibitor.

Any research plan has to sacrifice some advantages to achieve others. At LRI, by choosing to focus on animal lifespan studies, we accept the costs of more expensive, slower experiments and spurious, species-specific effects, in exchange for focusing on the most patient-relevant _outcomes _(survival and aging symptoms).  Other companies and research organizations are making different tradeoffs, and this diversity of approaches is good for the field as a whole.
