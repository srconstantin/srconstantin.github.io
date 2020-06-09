---
layout: tag_post
title: Is Stupidity Strength? Part 3 -- Evolutionary Game Theory
tags: [social, game-theory]
---

![badgerfight]({{ site.baseurl }}/images/badgerfight.jpg)

**Spite Strategies**

Carlo Cipolla [defined](http://www.extremistvector.com/content/stupid.html) stupidity as causing harm to others as well as harming oneself, while benefiting nobody.

Another way of looking at this: a stupid decision is one which you could make a [Pareto improvement ](https://en.wikipedia.org/wiki/Pareto_efficiency)on. A stupid decision means neglecting a win-win opportunity.  

Since people aren't omniscient and omnipotent, and we don't necessarily want to call that stupidity, we can narrow this; a stupid decision is one that _avoidably _causes harm to self and others.

In the previous post, I mentioned a possible incentive for a coalition of individuals to be stupid -- the "too big to fail" strategy.  If enough people commit to take imprudent risks, all at once, then they can force the prudent people to bail them out when catastrophe eventually comes. In the long term, _everyone_ will be worse off in absolute terms than if the catastrophe had been prudently averted; but the Stupids will be relatively better off than the Prudents.

In evolutionary biology, this is a special case of what's called[ Hamiltonian spite](https://en.wikipedia.org/wiki/Hamiltonian_spite), after its originator W.D. Hamilton. Imagine a gene that imposes a fitness cost on organisms that bear it, but an even greater fitness cost on members of the same species that do _not _bear it. This gene might be able to persist in the population, by enabling its bearers to outcompete their neighbors, even though it causes only harm and no benefit to anyone!

**Does spite ever happen?  **

Many apparently spiteful behaviors in nature are actually selfish; when a male bowerbird destroys the nests of other bowerbirds, his own nest appears more attractive in comparison and he gets more mating opportunities. This is a straightforward case of zero-sum competition, not true spite. 

[Hamilton himself thought](https://sci-hub.tw/10.1038/2281218a0) cases of spite would be vanishingly rare in nature; his own equations show that spiteful strategies are less likely to win, the larger the population size; and since spite strategies diminish absolute fitness (ie the number of offspring), spite-dominated populations will tend to shrink towards extinction.  In his original paper, Hamilton proposed that spite strategies might emerge in small, isolated populations and quickly drive those populations out of existence; we shouldn't expect to see them exist for long.

A more recent [paper ](https://onlinelibrary.wiley.com/doi/10.1111/j.1558-5646.2012.01831.x)adds an additional wrinkle, however. Hamilton's original models assumed that populations could be of arbitrary size. But in nature, population sizes are often bounded above by the carrying capacity of the environment -- a given savannah only has enough resources to support so many lions, no matter how fit they are.  If you add a carrying capacity constraint to the equations, you see that spite strategies _can _persist in the long term, provided the harm to those who don't bear the spite gene is enough larger than the harm to those who do bear it. This critical ratio must be larger, the larger the maximum population size can be; it is easier for spite strategies to survive in environments with smaller carrying capacities.

This fact is suggestive for the question of whether spite strategies could have evolved in humans.  We are a highly K-selected species (compared to other mammals like mice) -- we have large bodies, slow metabolisms, and long lives, developing slowly, reproducing infrequently, and investing a lot of care into our offspring.  This pattern tends to evolve in organisms close to their environment's carrying capacity, such as in predators at the top of the food chain. Vast litters of offspring would do a K-selected mother no good; they would bump into the harsh limitations of the food supply and starve before they had children of their own. She would be better off investing resources into making her few offspring more robust; building them bigger, more long-lasting bodies, with bigger brains more able to adapt their behavior to survive; and guarding and feeding them while young; and, perhaps, sabotaging their competition!  It is in K-selected animals like us that spiteful behaviors have a plausible evolutionary advantage, since populations are stably small; just as it is in oligopolies, not competitive markets, where sabotaging a competitor can be a winning strategy.  

(Of course, the environment in which modern Homo sapiens evolved was the harsh Malthusian context of the Pleistocene; for the past 300 years the human population has exploded exponentially. Perhaps the spite strategies we evolved with are no longer adaptive in a context of improving technology and global trade.)

Likewise, there is a wider range of conditions under which spiteful strategies can persist when competition is [more localized](https://onlinelibrary.wiley.com/doi/full/10.1111/j.1420-9101.2004.00775.x), so that only small populations can interact with each other. Global competition punishes lose-lose strategies, since these diminish the absolute fitness of those who carry them and their non-carrier victims; local competition can preserve these strategies in isolated enclaves.

In nature, we see spiteful behavior in the [social insects](https://www.jstor.org/stable/23735842?seq=1#page_scan_tab_contents); worker bees, wasps, and ants prevent other workers from reproducing by killing their eggs, and red fire ant workers kill unrelated queen ants. These actions do not provide any direct fitness benefit to the specific workers that do the killing; rather, they provide an indirect benefit to their sisters, the queens, by killing their unrelated rivals. 

It has been hypothesized that primates engage in spiteful behavior; they certainly engage in _apparently_ spiteful behaviors like harassing copulating couples and killing non-kin infants, but there's no consensus I can find as to whether this is true Hamiltonian spite or mere self-interested competition for food and mates.

**Spite and rent-seeking**

[In Tullock's model of rent-seeking](https://sci-hub.tw/https://doi.org/10.1016/j.ejpoleco.2003.09.002), individuals compete to take a winner-take-all prize; each individual decides how much to spend, and the more you spend, relative to all the other individuals, the more likely you are to get a prize.  What's the optimal amount to spend?

There is a unique Nash equilibrium strategy of how much to spend on trying to get the prize; that is, you can't improve your expected net gain by spending any more or any less. However, this is _not _an evolutionarily stable strategy! Populations that bid the Nash equilibrium will get overtaken by populations that spitefully bid_ more_, at cost to themselves.

The two strategies are rather close, and get closer asymptotically in large populations; the Nash equilibrium bid is (n-1)/n^2 rV (where n is population size, V is the payout value, and r is a shape parameter of the win-probability function), while the ESS bid is rV/n.  Evolutionarily optimal play is _slightly _more aggressive than individually optimal play, in a large population with many-to-many competition. But in a small population, or in a tournament-like setup where pairs of individuals play one on one and losers get knocked out of the game, this difference is magnified, and of course compounds with time.

Direct resource competition between conspecifics is many-to-many competition; as soon as I eat a bite, it simultaneously becomes unavailable to everyone else.

Fighting between conspecifics, however, is one-to-one competition; only two rams can butt heads at once. 

We should expect to see "overinvestment" in adaptations that increase individuals' abilities to win such head-to-head conflicts (pun intended), relative to the individually "rational" Nash equilibrium amount.  Competing for resources is not in general a spite strategy, because the winner of a conflict does directly benefit; but _overinvestment_ in resource competition _can _be a spite strategy.  It's net harmful to the individual, in expectation, but it's _more_ net harmful to his opponent.

**Spite and intergroup conflict**

If we allow different evolutionary strategies to_ detect _each other -- to treat "in-group" members differently from "outgroup" members, as human nations do (as well as other species; ants go to war) we see even more interesting things about the dynamics of spite.

If individuals are assumed to interact only with local neighbors, to migrate around somewhat, but to be able to distinguish kin from non-kin even if migration has occurred, [we observe ](https://royalsocietypublishing.org/doi/pdf/10.1098/rspb.2015.0142)that individuals tend to be altruistic (hurting themselves to help others) towards kin, and spiteful (hurting themselves to hurt others) towards non-kin. 

Moreover, minorities living in non-kin territory tend to be strongly altruistic towards their kin and only mildly spiteful towards the majority; while majorities tend to be only mildly altruistic towards each other and strongly spiteful towards minorities. This seems to match available evidence about human ethnic conflict.

**Spite in human experiments**

Humans display spiteful behavior in [game-theoretic experiments](https://www.econstor.eu/bitstream/10419/49653/1/576834327.pdf):

Zizzo (2003a) in his paper on burning money experiments reported that subjects are often willing to reduce, at a cost for themselves, the incomes of players who had been given higher endowments. In some instances subjects with the same or less endowment were also targeted. In a similar vein, Dawes, Fowler, Johnson, McElreath and Smirnov (2007) find that subjects are willing to reduce other group members’ income independently of the history of interaction...

In their experiments on competitive behavior, Rustichini and Vostroknutov (2007) find that participants are more inclined to reduce someone else’s income if the punished subject has earned more money than the punisher. Surprisingly, this effect is stronger when the higher incomes of the punished subjects are due to merit rather than luck...

The most extreme form of anti-social punishment, where the punishment is directed against those who had previously behaved nicely towards the punisher, has been observed in public good games with punishment. In these games those who are more cooperative than others are frequently punished. Such evidence is reported in Cinyabuguma, Page and Putterman (2006), Gächter, Herrmann and Thöni (2005) and Herrmann et al. (2008).

In a "rent-seeking game" played with 3500 undergraduates, players significantly "over-spent" on winning relative to the Nash equilibrium; in particular, they spent twice as much when playing against another human vs the computer, which suggests that spite is a social emotion.  Players who defected on the Prisoner's Dilemma game engaged in more spiteful overspending than cooperative players, and players who were more risk-prone in a lottery test were also more prone to overspend. Finally,_ afte_r engaging in a rent-seeking game, players cooperated significantly less on the Prisoner's Dilemma.

While players of a public good game punished free riders in all cities, in some cities players also engaged in _[antisocial punishment](https://www.nottingham.ac.uk/~lezsg1/papers/Herrmann-etal.pdf) _-- selectively penalizing the most generous contributors. This happened least in Anglophone cities (Boston, Melbourne, Nottingham) and most in Mediterranean, Middle Eastern, or Slavic cities (Muscat, Athens, Riyadh, Samara, Minsk, Istanbul); countries with high scores on social trust and rule of law displayed more "prosocial punishment" of free-riders and less "antisocial punishment" of contributors.

Several hundred Portuguese schoolchildren were [assigned to play a spite game](https://run.unl.pt/bitstream/10362/14126/1/Andre_Almeida2014_Spiteful_Strategies.pdf), where they could either play cooperatively or spitefully. If both players cooperate, both gain 15 points; if one cooperates and the other spites, the spiteful player gains 11 points (paying a cost) but his opponent only gains 5 points (a greater loss). Finally, if both players spite, they each get 2 points (a severe loss). 

This game can either be played with proportional winnings (each player gets a piece of candy for every 15 points), in which case playing cooperatively is optimal, or with winner-take-all conditions (the player with the most points gets a fancy chocolate), in which case playing spitefully is optimal.

The experiment found that younger children (5th-7th grade) usually played cooperatively, while older children (8th-10th grade) played cooperatively in the proportional-rewards conditions and spitefully in the winner-take-all conditions. Students repeating a grade were much more likely to behave spitefully.  This suggests that spiteful behavior in humans may emerge in the teenage years.

The economic experimental literature is clear that spiteful strategies do exist in humans, that they correlate with social trust and rule of law in the expected (inverse) direction, and that they seem to emerge in adolescence.
