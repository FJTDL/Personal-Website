---
layout: null
title: It's always the damned data
date: 2026-07-17
tags: [research]
---

In all science, the most common point of failure is human error. This obviously takes many forms depending on the problem at hand, but you can imagine that in statistics, the field that really defines what "data" even is, this problem is particularly damaging. 

In our case, we are considering multi-million-dollar or, in some cases, even billion-dollar machines, so we have extremely few to work with. Even worse is that these machines are incredibly sensitive and prone to perturbation from even the most minor of external stimuli. 
Naturally, simulation is the way to go, right? It's cheaper, and we can control for these random effects!

Well, yes, but actually no.

It depends on the event. For my work, a simulation in the correct level of accuracy can take up to three months even on a supercomputer, so "just simulate more" isn't exactly an option. Indeed, this is a problem I should like to fix one day, but for the time being, I have little choice.
It is here I am grateful to our collaborators in Kazakhstan who have simulated a catalogue of signals for us to work with. Myself and one other student have been using this catalogue for our work in CCSN, but it is here our problem arises.

The data is spread across three files—times, parameters, and the waves themselves—yet for no particularly discernible reason, the waves themselves are stored as the columns of the third file, not the rows. This was not a problem when I was working with image processing, as all that mattered there was the shape from the data and making the times line up.

However, for parameter estimation, it became a wild goose chase.

One detail of note is that prior to this research, I hadn't even touched machine learning, much less deep learning. I knew almost nothing of pooling or loss functions, and I suddenly had to work out how to use skip connections and U-Nets on a graphical representation I did not understand the math for, and upon completion of that challenge, jump into the cutting edge of simulation-based inference with neural posterior estimation. Even worse, my seniors under the same supervisor looked at my work with such apprehension, and claimed my techniques were "difficult" or in one case I heard one had "given up on that, it just wouldn't work."

So when I found myself going in circles, I wasn't surprised. As I think my flatmates and close friends can attest to, I was never frustrated with this stage of the process, more amused and curious. However, a month went by and I seemed to fluctuate between dismal underfitting and rampant overfitting, both happening very quickly. It was at this point the structure of the data began to make me suspicious. After all, if the columns are the data in one, but the rows are in another, and we have to clean this ourselves, when we didn't simulate the data ourselves, how much human error have we introduced?

Lo and behold, while staring at a particularly uninformed plot two days ago, the email comes in from my supervisor—a data error. Not the fault of anyone frankly, just a matter of fact. But the hard part? This data had been used for years before this was caught. Almost instantly, my model worked, and worked well at that. I sat back and thought to myself, "How many people must have gone bat-sh*t crazy because of something beyond their control, and never knew?"

I think this proves a central point in science, though. Just because we have a reputation for doing erudite things, does not mean we do not make mistakes. In fact, I'd argue that when people consider a scientist smart and they think of a robust schooling, they don't realise that most of their actual knowledge comes from hours, if not days, weeks, months, or even years, of failure and mistakes.
Failure doesn't feel great, but what I find is that when you love what you do, it doesn't feel bad either. It's still a positive result, really: what doesn't work is as important as what does.