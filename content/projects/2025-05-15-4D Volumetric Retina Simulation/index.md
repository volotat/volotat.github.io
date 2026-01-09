---
title: "4D Volumetric Retina Simulation"
description: "A physics-based 4D path tracing simulation visualizing how a four-dimensional being might perceive the world through a 3D volumetric retina."
date: 2025-05-15
image: "4D_eye_preview.png"
tags: 
    - "4D"
    - "Open Source"
    - "Research"
    - "Experiments"
categories:
    - "Projects"
---

A physics-based 4D path tracing simulation visualizing how a four-dimensional being might perceive the world through a 3D volumetric retina.

Current visualizations of 4D space often rely on wireframe projections or simple 3D cross-sections. This project takes a more biologically plausible approach: analogous to how we 3D beings perceive our world via 2D retinas, a 4D creature would likely possess a 3D (volumetric) retina.

This simulation implements a custom 4D path tracing engine (using Python and Taichi for GPU acceleration) to model light interactions within a hyper-scene containing a rotating tesseract. It simulates image formation by casting 4D rays onto a defined 3D retinal volume.

The simulation features physically-based rendering that models light bounces, shadows, and perspective in four spatial dimensions. Simulates a 3D sensor array rather than a flat plane. Implements a Gaussian fall-off for retinal sensitivity, mimicking foveal vision where the center of the 3D gaze is most acute. To make this comprehensible to human eyes, the 3D retinal image is composited from multiple depth slices, additively blended to represent the density of information a 4D being would process simultaneously.

**Status:** Completed Experiment

[View on GitHub](https://github.com/volotat/4DRender) | [Video Showcase](https://www.youtube.com/shorts/T697zlLvvHw)