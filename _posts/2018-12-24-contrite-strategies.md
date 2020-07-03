---
layout: tag_post
title: Contrite Strategies and the Need for Standards
tags: [game-theory]
---

_Epistemic Status: Confident_

There’s a really interesting paper from 1996 called [The Logic of Contrition](https://homepage.univie.ac.at/Karl.Sigmund/JTB97a.pdf), which I’ll summarize here.  In it, the authors identify a strategy called “Contrite Tit For Tat”, which does better than either Pavlov or Generous Tit For Tat in Iterated Prisoner’s Dilemma.

In Contrite Tit For Tat, the player doesn’t only look at what he and the other player played on the last term, but also another variable, the _standing_ of the players, which can be good or bad.

If Bob defected on Alice last round but Alice was in good standing, then Bob’s standing switches to bad, and Alice defects against Bob.

If Bob defected on Alice last round but Alice was in _bad _standing, then Bob’s standing stays good, and Alice cooperates with Bob.

If Bob cooperated with Alice last round, Bob keeps his good standing, and Alice cooperates.

This allows two Contrite Tit For Tat players to recover quickly from accidental defections without defecting against each other forever;

D/C -> C/D -> C/C

But, unlike Pavlov, it consistently resists the “always defect” strategy

D/C -> D/D -> D/D -> D/D …

Like TFT (Tit For Tat) and unlike Pavlov and gTFT (Generous Tit For Tat), cTFT (Contrite Tit For Tat) can invade a population of all Defectors.

A related contrite strategy is Remorse.  Remorse cooperates only if it is in bad standing, or if both players cooperated in the previous round. In other words, Remorse is more aggressive; unlike cTFT, it can attack cooperators.

Against the strategy “always cooperate”, cTFT always cooperates but Remorse alternates cooperating and defecting:

C/C -> C/D -> C/C -> C/D …

And Remorse defends effectively against defectors:

D/C -> D/D -> D/D -> D/D…

But if one Remorse accidentally defects against another, recovery is more difficult:

C/D -> D/C -> D/D -> C/D -> …

If the Prisoner’s Dilemma is repeated a large but finite number of times, cTFT is an evolutionarily stable state in the sense that _you can’t do better for yourself when playing against a cTFT player through doing anything that deviates from what cTFT would recommend._ This implies that no other strategy can successfully invade a population of all cTFT’s.

REMORSE can sometimes be invaded by strategies better at cooperating with themselves, while Pavlov can sometimes be invaded by Defectors, depending on the payoff matrix; but for all Prisoner’s Dilemma payoff matrices, cTFT resists invasion.

Defector and a similar strategy called Grim Trigger (if a player ever defects on you, keep defecting forever) are evolutionarily stable, but not good outcomes — they result in much lower scores for everyone in the population than TFT or its variants.  By contrast, a whole population that adopts cTFT, gTFT, Pavlov, or Remorse on average gets the payoff from cooperating each round.

The bottom line is, adding “contrition” to TFT makes it quite a bit better, and allows it to keep pace with Pavlov in exploiting TFT’s, while doing better than Pavlov at exploiting Defectors.

This is no longer true if we add noise in the _perception_ of good or bad standing; contrite strategies, like TFT, can get stuck defecting against each other if they erroneously perceive bad standing.

The moral of the story is that there’s a game-theoretic advantage to not only having _reciprocity_ (TFT) but _standards_ (cTFT), and in fact reciprocity alone is not enough to outperform strategies like Pavlov which don’t map well to human moral maxims.

What do I mean by standards?

There’s a difference between saying “Behavior X is better than behavior Y” and saying “Behavior Y is unacceptable.”

The concept of “unacceptable” behavior functions like the concept of “standing” in the game theory paper.  If I do something “unacceptable” and you respond in some negative way (you get mad or punish me or w/e), I’m not supposed to retaliate against _your_ negative response, I’m supposed to accept it.

Pure reciprocity results in blood feuds — “if you kill one of my family I’ll kill one of yours” is perfectly sound Tit For Tat reasoning, but it means that we can’t _stop_ killing once we’ve started.

_Arbitrary_ forgiveness fixes that problem and allows parties to reconcile even if they’ve been fighting, but introduces the new problem that now you’re vulnerable to an attacker who just won’t quit.

Contrite strategies are like having a court system. (Though not an enforcement system!  They are still “anarchist” in that sense — all cTFT bots are equal.)  The “standing” is an assessment attached to each person of whether they are in the wrong and thereby restricted in their permission to retaliate.

In general, for actions not covered by the legal system and even for some that are, we don’t _have_ widely shared standards of acceptable vs. unacceptable behavior.  We’re aware (and especially so given the internet) that these standards differ from subculture to subculture and context to context, and we’re often aware that they’re arbitrary, and so we have enormous difficulty getting widely shared clarity on claims like “he was deceptive and that’s not OK”.  Because…was he deceptive in a way that counts as fraud? Was it just “puffery” of the kind that’s normal in PR?  Was it a white lie to spare someone’s feelings?  Was it “just venting” and thus not expected to be as nuanced or fact-checked as more formal speech?  What _level or standard _of honesty could he reasonably have been expected to be living up to?

We can’t say “that’s not OK” without some kind of understanding that he had failed to live up to a shared expectation.  And _where is that bar?  _It’s going to depend who you ask and what local context they’re living in.  And not only that, but the fact that nobody is keeping track of where even the separate, local standards are, eventually standards will have to be dropped to the lowest common denominator if not made explicit.

[MBTI ](https://en.wikipedia.org/wiki/Myers%E2%80%93Briggs_Type_Indicator)isn’t science but it’s illustrative descriptively, and it seems to me that the difference between “Perceivers” and “Judgers”, which is basically the difference between the kinds of people who get called “judgmental” in ordinary English and the people who don’t, is that “Judgers” have a clear idea of where the line is between “acceptable” and “unacceptable” behavior, while Perceivers don’t.  I’m a Perceiver, and I’ve often had this experience where someone is saying “that’s just Not OK” and I’m like “whoa, where are you getting that? I can certainly see that it’s _suboptimal_, this other thing would be better, but why are you drawing the line for acceptability here instead of somewhere else?”

The lesson of cTFT is that _having _a line in the first place, having a standard that you can either be in line with or in violation of, has survival value.
