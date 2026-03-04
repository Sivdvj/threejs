# Particle Scroll Animation

A 3D background scroll animation featuring particles that morph between geometric states based on the user's scroll position. Built with Three.js, GSAP, and Simplex Noise.

![Capture](capture.gif)

## Features

- Dynamic morphing between 3 distinct states - a scatter, torus and circle
- Uses Simplex-Noise to create movement within the particle cluster
- GSAP ScrollTrigger to map the animation progress to the browser's scroll bar
- Parallax effect on mouse movement
- GUI controls to tweak particle color, speed of particles and noise amplitude

---

## The morphing engine

The core of the visual is the **Linear Interpolation (LERP)** function. As the user scrolls, the script calculates a `localProg` (local progress) between two sets of coordinate arrays:

$$pos = (1 - t) \cdot startShape + t \cdot endShape$$

Where $t$ is the scroll percentage between sections

---
