# Microtexture Inpainting

## Overview
This project focuses on **micro-texture inpainting**, where missing parts of an image are reconstructed using stochastic modeling techniques. Micro-textures, which lack strong geometric patterns, can be effectively modeled as **Gaussian random fields**, enabling their synthesis through probabilistic methods.

The inpainting technique is based on the **Asymptotic Discrete Spot Noise (ADSN)** model. This model allows us to:
- Generate micro-textures from grayscale or color images.
- Condition the synthesis process to ensure continuity at the edges of masked regions.
- Achieve visually coherent and statistically consistent results.

This project, supervised by Arthur Leclaire, implements the methodology presented in his [research paper](https://hal.science/hal-01428428/file/gaussian_inpainting.pdf)

---

## Methodology

#### **Grayscale Synthesis**
Below are examples of grayscale micro-texture synthesis:

<div align="center">
  <figure>
    <img src="images/microtexture1.png" alt="Original micro-texture" width="25%">
    <figcaption>Original Micro-Texture</figcaption>
  </figure>

  <figure>
    <img src="images/microtexture1 synth.png" alt="ADSN Grayscale Result" width="25%">
    <figcaption>ADSN Grayscale Result</figcaption>
  </figure>
</div>

---

#### **Color Synthesis**
Below are examples of color micro-texture synthesis:


<div align="center">
  <figure>
    <img src="images/bois.png" alt="Original micro-texture" width="25%">
    <figcaption>Original Micro-Texture</figcaption>
  </figure>

  <figure>
    <img src="images/bois synth.png" alt="ADSN Colour Result" width="25%">
    <figcaption>ADSN Grayscale Result</figcaption>
  </figure>
</div>

---

#### **Kriging Conditioning**
The following images demonstrate the continuity achieved through Kriging-based conditioning:

<div align="center">
  <figure>
    <img src="images/kringing_masked.png" alt="Original micro-texture" width="25%">
    <figcaption>Masked Micro-texture</figcaption>
  </figure>

  <figure>
    <img src="images/kringing.png" alt="ADSN Colour Result" width="25%">
    <figcaption>Kriging component</figcaption>
  </figure>
</div>

---

## Results

### **Visual and Statistical Analysis**
- The inpainted images showed smooth transitions with no visible edges at the mask boundaries.
- The mean squared error (MSE) at the contour was in the order of $10^{-21}$, demonstrating excellent continuity.

#### **Examples of Inpainting**
Below are examples of the inpainting results on masked images:

<div align="center">
  <img src="images/2.png" alt="Grayscale Inpainting 1" width="25%">
  <img src="images/2_inpaint.png" alt="Grayscale Inpainting 2" width="25%">
</div>

<div align="center">
  <img src="images/11.png" alt="Color Inpainting 1" width="25%">
  <img src="images/11_inpaint.png" alt="Color Inpainting 2" width="25%">
</div>

---

Feel free to explore the code and results for further insights.
For a deeper understanding of the methodology and results, you can refer to the report.pdf (in French).
