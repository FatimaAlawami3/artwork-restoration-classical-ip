# Artwork Restoration using Classical Image Processing

## Overview

This project focuses on **digital restoration of degraded artwork images** using **classical image processing techniques**. The goal is to improve visual clarity and perceptual quality while **preserving the original artistic characteristics** such as brush strokes, textures, and color gradients.

The project was completed as part of the **ARTI404 – Image Processing** course and emphasizes interpretability, efficiency, and respect for artistic integrity rather than black-box deep learning models.

---

## Problem Statement

Over time, artworks deteriorate due to aging, environmental conditions, and physical damage. These effects introduce noise, blur, contrast loss, and luminance degradation, which obscure artistic details.

The challenge is to restore these artworks **without altering their artistic intent**, using techniques that are:

* Interpretable
* Computationally efficient
* Suitable for cultural heritage preservation

---

## Restoration Pipeline

A **multi-stage image restoration pipeline** was designed and implemented:

1. **Noise Removal (Median Filtering)**

   * Removes salt-and-pepper noise
   * Preserves edges and brush strokes

2. **Detail Recovery (Sharpening)**

   * Enhances edges using a controlled sharpening kernel
   * Avoids over-sharpening artifacts

3. **Contrast Enhancement (CLAHE)**

   * Applied in LAB color space
   * Improves local contrast while maintaining color fidelity

4. **Luminance Adjustment (Gamma Correction)**

   * Subtle brightness correction
   * Ensures balanced tonal distribution

This sequential design allows each degradation factor to be handled independently.

---

## Dataset

* Large collection of degraded artwork images
* Total image pairs evaluated: **8,683** (degraded vs restored)
* Images processed individually and in batch mode

---

## Evaluation Metrics

To objectively assess restoration quality, four complementary metrics were used:

* **PSNR (Peak Signal-to-Noise Ratio)** – pixel-level quality
* **SSIM (Structural Similarity Index)** – structural preservation
* **FSIM (Feature Similarity Index)** – edge and texture preservation
* **LPIPS** – perceptual similarity based on deep features

### Average Results

* PSNR: **18.71 dB**
* SSIM: **0.5985**
* FSIM: **0.4583**
* LPIPS: **0.2267** (lower is better)

These results indicate effective restoration while maintaining perceptual and structural fidelity.

---

## Project Structure

```
├── notebooks/
│   ├── IP_project_image_enhance.ipynb
│   ├── IP_Project_example_Image.ipynb
│   └── IP_Evaluation.ipynb
│
├── report/
│   └── ARTI404_Project_Report.pdf
│
├── README.md
└── requirements.txt
```

---

## Tools and Technologies

* Python 3
* OpenCV
* NumPy
* Matplotlib
* scikit-image
* Jupyter Notebook

---

## Key Learning Outcomes

* Designing interpretable image restoration pipelines
* Applying classical image processing techniques effectively
* Evaluating image quality using objective and perceptual metrics
* Understanding the trade-offs between restoration quality and artistic integrity

---

## Team

This project was completed as a **university group project** for ARTI404 – Image Processing.

---

## Future Work

* Integrating deep learning–based restoration for severe degradation
* Applying super-resolution techniques
* Incorporating expert-based subjective evaluation
