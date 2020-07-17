---
layout: tag_post
title: The World Is Simple
tags: [math]
---

In the world of image and signal processing, a paper usually takes the form “We can prove that this algorithm gives such-and-such accuracy on images that have such-and-such regularity property.  We tried it on some examples and it worked pretty well.  We’re going to assume that most of the images we might care about have the regularity property.”

For instance, sparse coding and compressed sensing techniques assume that the representation of the image in some dictionary or basis is “sparse”, i.e. has very few nonzero coefficients.

There’s some biological justification for this: the mammalian brain [seems ](http://www.neuro.uoregon.edu/wehr/coursepapers/olshausen-field-2004.pdf)to recognize images with an overcomplete dictionary of Gabor filters, only a few of which are firing at any given time.

There’s a basic underlying assumption that the world is, in some sense, simple. This is related to ideas around the “unreasonable effectiveness of mathematics.”  Observations from nature can be expressed compactly.  That’s what it means to live in an intelligible universe.

But what does this mean specifically?

One observation is that the [power spectrum](http://en.wikipedia.org/wiki/Spectral_density), that is, the square of the (discrete) Fourier transform, of natural images obeys a power law

S(k) = A/k^(2 - eta)

where eta is usually small.  It’s been [hypothesized ](http://redwood.berkeley.edu/bruno/npb261b/ruderman97.pdf)that this is because natural images are composed of statistically independent objects, whose scales follow a power-law distribution.

What does this mean?  One way of thinking about it is that a signal with a power-law spectrum exists at all scales.  It’s referred to as [“pink noise”](http://en.wikipedia.org/wiki/Pink_noise).  You can generate a signal with a power-law spectrum by defining a “[fractional Brownian motion](http://en.wikipedia.org/wiki/Fractional_Brownian_motion)“.  This is like a Brownian motion, except the increment from time t to time s
 is a normal distribution with mean zero and variance |t-s|^(2H)
 for the Hurst exponent H
, which equals 1/2 in the special case of a Brownian motion.  The covariance function of a fractional Brownian motion is homogeneous of degree 2H.  Fractional Brownian motions are Lipschitz-continuous with exponent H.

As a [matter of fact](http://www.wisdom.weizmann.ac.il/~zeitouni/pdf/fbmfanc.pdf), any function whose wavelet transform is homogeneous of degree 
lambda is a fractional Brownian motion of degree (lambda-1)/2

[Cosma Shalizi](http://vserver1.cscs.lsa.umich.edu/~crshalizi/notabene/power-laws.html) has a good post on this phenomenon.  Systems in thermodynamic equilibrium, i.e. “boring” systems, have correlations that decay exponentially in space and time. Systems going through phase transitions, like turbulent flows, and like most things you’ll observe in nature, have correlations that decay _slower_, with a power law. There are many simple explanations for why things might wind up being power-law-ish.


    Imagine you have some set of piles, each of which grows, multiplicatively, at a constant rate. New piles are started at random times, with a constant probability per unit time. (This is a good model of my office.) Then, at any time, the age of the piles is exponentially distributed, and their size is an exponential function of their age; the two exponentials cancel and give you a power-law size distribution. The basic combination of exponential growth and random observation times turns out to work even if it’s only the _mean_ size of piles which grows exponentially.

If we’re in a domain with eta < 1 and H > 1/2, we’re looking at a function with a square-summable Fourier transform.  This is why L^2 assumptions are not completely insane in the domain of signal processing, and why it makes sense to apply wavelet (and related) transforms and truncate after finitely many coefficients.

Not all regularity assumptions in the signal-processing and machine-learning world are warranted.  Image processing is full of bounded-variation methods like Mumford-Shah, and at least one paper is [claiming](http://perso.telecom-paristech.fr/~Gousseau/gm01.pdf) to observe that natural images are not actually BV.  My own research deals with the fact that Riemannian assumptions in manifold learning are not realistic for most real-world datasets, and that manifold-learning methods need to be extended to sub-Riemannian manifolds (or control manifolds).  And I’m genuinely uncertain when sparsity assumptions are applicable.

But decaying power spectra _are_ a pretty robust empirical observation, and not for shocking reasons. It’s a pretty modest criterion of “simplicity” or “intelligibility”, it’s easy to reproduce with simple random processes, it’s kind of unsurprising that we see it all over the place. And it allows us to pretend we live in Hilbert spaces, which is _always_ a win, because you can assume that Fourier transforms converge and discrete approximations of projections onto orthogonal bases/dictionaries are permissible.

Power-law spectrum decay is a sort of minimum assumption of simplicity that we can expect to see in all kinds of data sets that were not generated “adversarially.”  It’s not a great mystery that the universe is set up that way; it’s what we would expect.  Stronger assumptions of simplicity are more likely to be domain-specific.  If you know what you’re looking at (it’s a line drawing; it’s a set of photographs of the same thing taken at different angles; it’s a small number of anomalies in an otherwise featureless plane; etc) you can make more stringent claims about sparsity or regularity.  But there’s a certain amount of simplicity that we’re justified in assuming almost by default, which allows us to use the tools of applied harmonic analysis in the first place.
