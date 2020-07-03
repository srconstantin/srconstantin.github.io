---
layout: tag_post
title: The Pavlov Strategy
tags: [game-theory]
---

_Epistemic Status: Common knowledge, just not to me_

[The Evolution of Trust](https://ncase.me/trust/) is a deceptively friendly little interactive game.  Near the end, there’s a “sandbox” evolutionary game theory simulator. It’s pretty flexible. You can do quick experiments in it without writing code. I highly recommend playing around.

One of the things that surprised me was a strategy the game calls Simpleton, also known in the literature as Pavlov.  In certain conditions, it works pretty well — even better than tit-for-tat or tit-for-tat with forgiveness.

Let’s set the framework first. You have a Prisoner’s dilemma type game.



*   If both parties cooperate, they each get +2 points.
*   If one cooperates and the other defects, the defector gets +3 points and the cooperator gets -1 point
*   If both defect, both get 0 points.

This game is _iterated _— you’re randomly assigned to a partner and you play many rounds.   Longer rounds reward more cooperative strategies; shorter rounds reward more defection.

It’s also _evolutionary _— you have a proportion of bots each playing their strategies, and after each round, the bots with the most points replicate and the bots with the least points die out.  Successful strategies will tend to reproduce while unsuccessful ones die out.  In other words, this is the [Darwin Game.](https://thezvi.wordpress.com/2017/11/15/the-darwin-game/)

Finally, it’s _stochastic_ — there’s a small probability that any bot will make a mistake and cooperate or defect at random.

Now, how does Pavlov work?

Pavlov starts off cooperating.  If the other player cooperates with Pavlov, Pavlov keeps doing whatever it’s doing, even if it was a mistake; if the other player defects, Pavlov switches its behavior, even if it was a mistake.

In other words, Pavlov:



*   cooperates when you cooperate with it, except by mistake
*   “pushes boundaries” and keeps defecting when you cooperate, until you retaliate
*   “concedes when punished” and cooperates after a defect/defect result
*   “retaliates against unprovoked aggression”, defecting if you defect on it while it cooperates.

If there’s any randomness, Pavlov is better at cooperating with itself than Tit-For-Tat. One accidental defection and two Tit-For-Tats are stuck in an eternal defect cycle, while Pavlov’s forgive each other and wind up back in a cooperate/cooperate pattern.

Moreover, Pavlov can exploit CooperateBot (if it defects by accident, it will keep greedily defecting against the hapless CooperateBot, while Tit-For-Tat will not) but still exerts _some _pressure against DefectBot (defecting against it half the time, compared to Tit-For-Tat’s consistent defection.)

The interesting thing is that Pavlov can beat Tit-For-Tat _or _Tit-for-Tat-with-Forgiveness in a wide variety of scenarios.

If there are only Pavlov and Tit-For-Tat bots, Tit-For-Tat has to start out outnumbering Pavlov quite significantly in order to win. The same is true for a population of Pavlov and Tit-For-Tat-With-Forgiveness.  It doesn’t change if we add in some Cooperators or Defectors either.

Why?

Compared to Tit-For-Tat, Pavlov cooperates better with itself.  If two Tit-For-Tat bots are paired, and one of them accidentally defects, they’ll be stuck in a mutual defection equilibrium.  However, if one Pavlov bot accidentally defects against its clone, we’ll see

C/D -> D/D -> C->C

which recovers a mutual-cooperation equilibrium and picks up more points.

Compared to Tit-For-Tat-With-Forgiveness, Pavlov cooperates *worse* with itself (it takes longer to recover from mistakes) but it “exploits” TFTWF’s patience better. If Pavlov accidentally defects against TFTWF, the result is

D/C -> D/C -> D/D -> C/D -> D/D -> C/C,

which leaves Pavlov with a net gain of 1 point per turn, (over the first five turns before a cooperative equilibrium) compared to TFTWF’s 1/5 point per turn.

If TFTWF accidentally defects against Pavlov, the result is

C/D -> D/C -> D/C -> D/D -> C/D

which cycles eternally (until the next mistake), getting Pavlov an average of 5/4 points per turn, compared to TFTWF’s 1 point per turn.

Either way, Pavlov eventually overtakes TFTWF.

If you add enough DefectBots to a mix of Pavlovs and TFT’s (and it has to be a large majority of the total population being DefectBots) TFT can win, because it’s more resistant against DefectBots than Pavlov is.  Pavlov cooperates with DefectBots half the time; TFT never does except by mistake.

Pavlov isn’t perfect, but it performs well enough to hold its own in a variety of circumstances.  An adapted version of Pavlov won the [2005 iterated game theory tournament](https://bib.irb.hr/datoteka/583494.1818-A-Review-of-Iterated-Prisoner-s-Dilemma-Strategies-v1_2.pdf).

Why, then, don’t we actually talk about it, the way we talk about Tit-For-Tat?  If it’s true that moral maxims like the Golden Rule emerge out of the fact that Tit-For-Tat is an effective strategy, why aren’t there moral maxims that exemplify the Pavlov strategy?  Why haven’t I even _heard _of Pavlov until now, despite having taken a game theory course once, when _everybody _has heard of Tit-For-Tat and has an intuitive feeling for how it works?

In Wedekind and Milinski’s 1996 [experiment](https://www.pnas.org/content/pnas/93/7/2686.full.pdf) with human subjects, playing an iterated prisoner’s dilemma game, a full 70% of them engaged in Pavlov-like strategies.  The human Pavlovians were smarter than a pure Pavlov strategy — they eventually recognized the DefectBots and stopped cooperating with them, while a pure-Pavlov strategy never would — but, just like Pavlov, the humans kept “pushing boundaries” when unopposed.

Moreover, humans basically divided themselves into Pavlovians and Tit-For-Tat-ers; they didn’t switch strategies between game conditions where one strategy or another was superior, but just played the same way each time.

In other words, it seems fairly likely not only that Pavlov performs well in computer simulations, but that humans _do _have some intuitive model of Pavlov.  And, even more suggestively, it might be that “there are two kinds of people” — some people always play Pavlov while others always play Tit-For-Tat.

Human players are [more likely](https://www.pnas.org/content/pnas/95/23/13755.full.pdf) to use generous Tit-For-Tat strategies rather than Pavlov when they have to play a working-memory game at the same time as they’re playing iterated Prisoner’s Dilemma.  In other words, Pavlov is probably more costly in working memory than generous Tit for Tat.

If you look at all 16 theoretically possible strategies that only have memory of the previous round, and let them evolve, evolutionary dynamics can wind up quite [complex and oscillatory.](https://www.pnas.org/content/pnas/90/11/5091.full.pdf)

A population of TFT players will be invaded by more “forgiving” strategies like Pavlov, who in turn can be invaded by DefectBot and other uncooperative strategies, which again can be invaded by TFT, which thrives in high-defection environments.  If you track the overall rate of cooperation over time, you get very regular oscillations, though these are quite sensitive to variation in the error and mutation rates and nonperiodic (chaotic) behavior can occur in some regimes.

This is strangely reminiscent of Peter Turchin’s theory of [secular cycles](http://peterturchin.com/secular-cycles/) in history.  Periods of peace and prosperity alternate with periods of conflict and poverty; empires rise and fall.  Periods of low cooperation happen at the fall of an empire/state/civilization; this enables new empires to rise when a subgroup has better ability to [cooperate with itself and fight off its enemies](http://peterturchin.com/cliodynamica/the-dune-hypothesis/) than the surrounding warring peoples; but in peacetime, at the height of an empire, more forgiving and exploitative strategies like Pavlov can emerge, which themselves are vulnerable to the barbaric defectors.  This is a vastly simplified story compared to the actual mathematical dynamics _or _the actual history, of course, but it’s an illustrative gist.

The big takeaway from learning about evolutionary game theory is that it’s genuinely complicated from a [player-perspective.](https://srconstantin.wordpress.com/2018/12/14/player-vs-character-a-two-level-model-of-ethics/)

“It’s complicated” sometimes functions as a curiosity-stopper; you conclude “more research is needed” instead of looking at the data you have and drawing preliminary conclusions, if you want to protect your intellectual “territory” without putting yourself out of a job.

That isn’t the kind of “complexity” I’m talking about here.  Chaos in dynamical systems has a specific meaning: the system is so sensitive to initial conditions that even a small measurement error in determining where it starts means you cannot even approximately predict where it will end up.

[“Chaos: When the present determines the future, but the approximate present does not approximately determine the future.”](https://en.wikipedia.org/wiki/Chaos_theory)

Optimal strategy depends sensitively on who else is in the population, how many errors you make, and how likely strategies are to change (or enter or leave).  There are a lot of moving parts here.
