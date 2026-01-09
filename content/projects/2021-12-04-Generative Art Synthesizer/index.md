---
title: "Generative Art Synthesizer"
description: "A Python program that generates Python programs that generate generative art."
date: 2021-12-04
image: "gas_preview.png"
tags: 
    - "Generative Art"
    - "Open Source"
    - "Procedural Generation"
    - "Meta-Programming"
    - "Experiments"
categories:
    - "Projects"
---

A Python program that generates Python programs that generate generative art.

Most generative art relies on stochastic processes where the initial seed and specific parameters are often lost, making exact reproduction difficult. GAS takes a different approach: instead of storing just the output or the parameters, it generates a fully deterministic, standalone Python script for each artwork. This ensures complete reproducibility—if you have the script, you have the art.

The core mechanism involves initializing a tensor with coordinate data and then applying a random sequence of mathematical transformations (like `transit`, `sin`, `magnitude`, `shift`) to its channels. These operations are restricted to the [-1, 1] range to ensure stability. The final result is a composition of these channels converted into color space.

*   **Self-Contained Art:** Each generated piece is a runnable Python script with zero external dependencies beyond standard scientific libraries (numpy, PIL).
*   **Deterministic:** The generated scripts contain no random elements; running the same script always produces the exact same image.
*   **Method-Based generation:** Uses a palette of composable mathematical functions (`sin`, `prod`, `soft_min`, etc.) to "sculpt" the image in a high-dimensional channel space.
*   **Aesthetic Scoring:** Includes a simple scoring model to estimate the visual quality of generated outputs.

**Status:** Completed Experiment

[View on GitHub](https://github.com/volotat/GAS)