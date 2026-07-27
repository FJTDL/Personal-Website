---
layout: null
title: Connections
date: 2026-07-26
tags: [research]
---

One thing I always found disapointing about the highschool experience was the lack of continuity. Studying physics without also studying the mathematics is lame, boring, and to some extent, both limiting and short sighted. For me, I started wondering very quickly what the point of learning differential equations was in my calculus class if all we ever applied it to was modelling bacterial populations or Newton's law of cooling.

It doesn't stop there. My final year of chemistry included a paper on thermodynamics - but in my chemistry class, not physics. That's not a problem per se, but understanding atomic structure (a unit of said thermodynamics paper) would have paired nicely with my paper in modern physics. In the same way, being taught that an alkane can form a haloalkane in the presence of UV and a halogen reagent but never learning why the UV was needed became a frustrating question my teachers would not, or perhaps *could not* answer.

It is definitely better at a university level, but the same limitations remain. I have completed almost all the papers relevant to the standard frequentist inference of statistics, but it was in my Bayesian class where the lecturer asked a remarkably simple question I had no answer to: "Why is it called Fisher *information*?"

It gets you thinking, and before long you start to see a bigger picture.

The Fisher information of a normal distribution is given as $\frac{1}{\sigma}$, so what happens if we start here? Well, there's only one variable: $\sigma$, which according to our frequentist paradigm is a "fixed but unknown parameter" (I prefer to consider it a random variable, but my opinion counts for nothing). In this sense, we can consider what happens as $\sigma$ changes. 

For a distribution with large spread, the value of $\sigma$ is large, hence the Fisher information is small, as it is the reciprocal of $sigma$. Equally, for a distribution with low dispersion, $\sigma$ will be small, and hence the Fisher information will be large. 

Great so, that was simple enough, but what does the big and small really *mean* here? 

A lot of the frequentist papers teach Fisher information as the handy trick to calculating the asymptotic variance of the estimator by using the reciprocal. So to return to our over-dispersed example, $\sigma$ is large, so the Fisher information is small, so the variance is large - we are very uncertain about our estimator. This makes sense, as we have a highly varied estimator, so the "evidence" is quite spread out, we have a lower confidence. On the other hand, if $\sigma$ is small, thenthe Fisher information is large, so the variance is small - we are *more* confident about our estimator.

So intuitively, having a lot of information means we're more confident in our estimates - it's a simple idea! 

But it begs the question - why did I have to piece this together myself? I'm not complaining, I love pondering this kind of problem, but when I explained it to some friends with the same frequentist background I could visible see the lightbulbs turn on. We now all feel much more confident about asymptotic estimation as well because we understand *why* the Fisher information is relevant.

These kinds of connections are everywhere, yet we have to piece them together. A similar lightbulb went off a few months ago when Wilks' theorem explained that the double the difference between log-likelihoods converges in distribution to a chi-squared distribution. I remembered that in my statistical modelling courses we compared deviance, which is double the difference of the log-likelihoods, to a chi-squared distribution on $n-p$ degrees of freedom to assess model fit, with $n$ being the number of observations and $p$ the number of parameters we're fitting. Right there, not only do we see the connection with the formula, but we also were taught that for low sample sizes this fails. Why, Wilks' theorem is based on asymptotics! We *need* a large(ish) sample size for this to work, and if it doesn't we need to use bootstrapping or similar techniques that do not rely on this parametric result!

Fields really should be studied together and have their connections well taught, as we begin to find fascinating applications that can solve meaningful and long term problems by bringing new perspectives. What worries me is that other students are not making these same connections, and if they are not taught, at what point do we lose them? Has someone else written down my same incoherent rambling elsewhere? Has an AI worked this out in some high dimensional vector space? 

Regardless, I think the biggest change for my was my inference papers. Yes, I am at heart a Bayesian, but the connections we form from understanding the robust mathematics underpining everything we do lifts the fog and allows us to see new opportunities. 
