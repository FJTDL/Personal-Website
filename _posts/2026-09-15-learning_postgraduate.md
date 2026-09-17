---
layout: null
title: Learning as a postgraduate
date: 2026-09-15
tags: [research]
---

Part of the joy (and challenge) as a research student is having to adapt to new techniques.

I knew my work was going to be using PyTorch, and as I already have a Python background, I started learning PyTorch. Except I wasn't going to be working with MNIST, nor was I going to be making a linear predictor. No, I needed to replace sections of an image with something as close to the ground truth as possible, meaning I needed to learn not only how to process images with deep learning and thus the necessary architectures, I needed to learn how to handle the replacement aspect *and* what the image was. I have no background in time-frequency domain mathematics, or really even the frequency domain, so the jump going *past* the standard Fourier analysis straight to continuous wavelet transforms (CWT) and scalograms was very intimidating. I still don't completely understand the math, but I know it works, and it produces images I can work with. Learning I can't easily work directly on the image was helped by my computer science background in understanding data loss, but was still difficult, especially to explain to my supervisor. Granted, we had misunderstood someone else's work, and she cleared it up for us, but it was a very confusing time; fascinating, but confusing.

I have found similar in my postgraduate taught papers. I don't really agree with the idea of making all students take either professional skills or statistical computing courses as postgraduates because the timing of them is poor (opposite semesters) and neither are especially relevant to my work, although I am grateful for the LaTeX exposure in professional skills. And Excel, for that matter. What I find is the same for many other students, whether they have to pick up new estimation methods, distributions they've never heard of, or programmes totally alien to them. The value of a postgraduate should be how they think; indeed, universities should be about teaching us how to think in ways relevant to our fields: think like an engineer, geologist, doctor, criminologist, economist, and whatever else. I also think there is great value in being a bit of a hybrid, knowing your own field but having exposure to others, which I think is especially valuable in statistics seeing as we go between other fields.

Most recently, I have had to learn about chip architectures. Why? My code is *awful*.

I have access to incredibly powerful data-centre-grade GPUs that my models hardly use, because while the PyTorch I used in my first network can be optimised for GPUs easily, my new code cannot. This is largely because the libraries are still young, but you can imagine my horror when I got an email that essentially read, "*Finn, your code is starving the CPU and drastically slowing everything down.*" 

My confusion was simple: "*My code is optimised as much as possible, I don't generate data on the fly; it's on the disk...*" The consideration I had made to store on the disk results in a constant go-between for the GPU and CPU, meaning I actually use the CPU more than the GPU. Thankfully, my co-supervisor put me on a new machine benefitting from Apple silicon chips. Funnily enough, I originally trained models on my own M2 chip using MPS before I got access to the NVIDIA L40s, so this is familiar territory, albeit with a very different network to what I had in March.

Better understanding cores, architectures, computation, and other hardware aspects is proving to be my current problem. I have a background in algorithmic analysis and in computational efficiency. Optimisation is something I enjoy anywhere, so I know how that works, but when faced with a breadboard, I'm hopeless. Not for lack of trying, but by total accident rather than design, I have a skillset totally geared towards using computers rather than building them or, indeed, understanding them. That may be a sad reflection of modern computer science degrees essentially being software development degrees in disguise. Come to think of it, my minor isn't called "Computer Science"—it is literally called "Software Development"! 

The last time I tried to do anything with hardware myself, I ended up getting electrocuted by the same dishwasher twice in a 10-second interval.

If you had told the me from six months ago the problem would be hardware, I don't think he'd (I'd?) be surprised, but perhaps misunderstand the problem. For years, the consensus in computer science was "memory is cheap, you can always buy more"—like *hell* I can just buy more! It means I can't really win on either front. It's rough, but it's really just peanuts when you consider my supervisor used to have MCMC algorithms running for weeks.

I keep hearing about TPUs and "neural acceleration", but without laying eyes on them it's hard to tell exactly how beneficial they'd be. I know in computing 9% faster is a lot, but for me it's the difference between an eight-hour job and a just-over-nine-hour job, so it's really still marginal compared to models that take days to run.

Times change, and I am ultimately extremely grateful for very intelligent people making things run better, but I would like it if I could actually afford the equipment I need.