---
layout: null
title: "Deep Learning Architectures for Gravitational Wave Detections"
date: 2026-07-14
published: false
---

Over the past few weeks, I've been experimenting with spatial-temporal neural networks to parse simulated strain data for the Advanced LIGO setup. 

### Model Performance

Our target optimization is governed by the following log-likelihood formulation:

$$ \ln \mathcal{L}(\theta) = -\frac{1}{2} \sum_{i} \frac{\left| d_i - h_i(\theta) \right|^2}{\sigma_i^2} $$

Where $d_i$ represents the frequency domain strain data. Here is a visualization of the loss curves from the initial training runs across different network layers:

<!-- Adding an image -->
![Loss curves over 150 epochs](./Static/images/loss_curves.png)

*Figure 1: Convergence speeds up drastically when applying amortized deep learning wrappers.*

The next phase involves parsing actual data variations from next-generation interferometers.