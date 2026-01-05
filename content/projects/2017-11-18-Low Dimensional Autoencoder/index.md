---
title: "Low Dimensional Autoencoder"
description: "An experimental approach to training autoencoders for extremely dense low-dimensional data representation."
date: 2017-11-18
image: "latent_space.png"
tags: 
    - "Machine Learning"
    - "Experiments"
    - "Open Source"
    - "Dimensionality Reduction"
categories:
    - "Projects"
---

An experimental approach to training autoencoders for meaningful low-dimensional data representation.

This project was one of my first experiments in machine learning, serving as a deep dive into how autoencoders process information. The goal was to address the difficulty of encoding high-dimensional data (like images) into very low-dimensional latent spaces (like 2D) without the model getting stuck in local minima. Usually it takes at least 16 or more dimensions for bottleneck embeddings to get decent results, but I wanted to see if it was possible to achieve this in just 2 dimensions.

The method involves training the autoencoder in a typical fashion, alongside with the encoder that trains on a dynamic set of target representations. It works by initially setting random points for each datapoint and then, at each step, stretching the latent space to touch the predefined space boundaries while applying a repulsion force to keep datapoints distinct. This prevents points from clustering too densely and encourages a more uniform distribution.

The result, as seen in the project image, is a continuous 2D embedding space that successfully compacts the entire MNIST dataset, allowing for smooth transitions between different digits.

**Status:** Completed Experiment

[View on GitHub](https://github.com/volotat/Low-Dimensional-Autoencoder)