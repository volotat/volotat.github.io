---
title: "ConGAN"
description: "Continuous Adversarial Image Generator that can produce high-quality images with few training examples and resolution independence."
date: 2018-01-29
image: "faces_table.png"
tags: 
    - "Machine Learning"
    - "Experiments"
    - "Open Source"
    - "GAN"
categories:
    - "Projects"
math: true
---

Continuous Adversarial Image Generator that can produce high-quality images with relatively few examples and resolution independence.

This project implements a Generative Adversarial Network (GAN) that learns a continuous function mapping coordinates (x, y) and a latent vector z to an RGB color, rather than generating a fixed grid of pixels. By treating images as continuous functions, the model creates a "vector-like" representation that can be sampled at any resolution.

The architecture differs from traditional GANs by using a coordinate-based generator. The system includes an "Ident" network to map images to a latent space, a Generator that predicts colors based on position and latent codes, and a Discriminator that validates pixel data in context.

Results demonstrated that the model could generalize well from small datasets (10-20 images is enough for reasonable results, while training the network completely from the scratch)  and produce smooth interpolations in the latent space, effectively hallucinating plausible variations between training examples.

**Status:** Completed Experiment

[View on GitHub](https://github.com/volotat/ConGAN)