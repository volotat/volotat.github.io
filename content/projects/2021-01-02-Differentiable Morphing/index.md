---
title: "Differentiable Morphing"
description: "Image morphing without reference points by optimizing warp maps via gradient descent."
date: 2021-01-02
image: "formula.jpg"
tags: 
    - "Machine Learning"
    - "Open Source"
    - "Experiments"
    - "Research"
categories:
    - "Projects"
math: true
---

Image morphing without reference points by optimizing warp maps via gradient descent.

This project introduces a "differentiable morphing" algorithm that can smoothly transition between any two images without requiring manual reference points or landmarks. Unlike traditional generative models that learn a distribution from a dataset, this approach uses a neural network as a temporary functional mapping to solve a specific optimization problem for a single pair of images.

The algorithm finds a set of maps that transform the source image into the target image.

<!--The algorithm finds a set of maps that transform the source image ($A$) into the target image ($B$) using the following logic:

$$ B = (A \times \text{mult\_map} + \text{add\_map}) \circ \text{warp\_map} $$

*   **Mult Map:** Removes unnecessary parts and adjusts localized color balance.
*   **Add Map:** Introduces new colors not present in the original image.
*   **Warp Map:** Distorts the image geometry to handle rotation, scaling, and movement of objects.-->

By interpolating the strength of these maps, the system produces a smooth, seamless animation where features transform fluidly from one state to another.

**Status:** Completed Experiment

### Cited in Scientific Literature
*   [The explainability paradox: Challenges for xAI in digital pathology](https://www.sciencedirect.com/science/article/pii/S0167739X22000838)
*   [IMPUS: Image Morphing with Perceptually-Uniform Sampling Using Diffusion Models](https://arxiv.org/abs/2311.06792)
*   [FreeMorph: Tuning-Free Generalized Image Morphing with Diffusion Model](https://arxiv.org/abs/2507.01953)

[View on GitHub](https://github.com/volotat/DiffMorph)