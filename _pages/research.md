---
layout: archive
title: Research
permalink: /research/
author_profile: true
---


My research sits at the intersection of **Medical Image Processing** and **Computer Vision**, with a focused commitment to building deep learning systems that are not only accurate but clinically deployable. I am particularly drawn to problems where standard models fail silently — producing confident but unsafe predictions — and I work toward architectures that enforce precision, interpretability, and robustness as first-class design goals. My long-term vision is to develop AI tools that clinicians can genuinely trust in high-stakes diagnostic and surgical planning workflows.

The key areas I am currently exploring are listed below.

---

## 1. Medical Image Processing & Brain Tumor Segmentation

Brain metastasis segmentation in MRI is a clinically critical yet technically underserved problem. Lesions are typically 5–15 mm in diameter and occupy less than 2% of total tumor volume, creating severe class imbalance that destabilizes standard training objectives. While soft-attention CNNs achieve high recall on such tasks, I identified a systematic failure mode I term the **over-segmentation paradox**: models overfit to sensitivity at the cost of catastrophic precision collapse (precision < 0.23) and boundary errors exceeding 150 mm — margins that render outputs unsafe for stereotactic radiosurgery planning, where millimeter-level accuracy is non-negotiable.

To address this, I proposed **SG-Net (Spatial Gating Network)**, a precision-first architecture built around hard spatial gating. Rather than weighting all spatial features softly, SG-Net applies binary-style gating to aggressively suppress background activations while preserving tumor-relevant features. This enforces selectivity at the feature level, directly attacking the root cause of over-segmentation. Validated on the Brain-Mets-Lung-MRI dataset (n=92), SG-Net delivers substantial and statistically significant improvements over prior baselines:

| Metric | SG-Net | Attention U-Net | ResU-Net |
|---|---|---|---|
| Dice Similarity Coefficient | **0.5578 ± 0.0243** | — | — |
| 95% Hausdorff Distance | **56.13 mm** | 157.52 mm | — |
| Precision | **0.52** | 0.20 | — |
| Parameters | **0.67M** | 5.9M | — |

All improvements over Attention U-Net and ResU-Net are statistically significant (p < 0.001). Beyond accuracy, SG-Net's 0.67M parameter footprint — 8.8× leaner than Attention U-Net — makes it viable for deployment in resource-constrained clinical settings without sacrificing performance.

**Related Paper:**
- [Hard Spatial Gating for Precision-Driven Brain Metastasis Segmentation: Addressing the Over-Segmentation Paradox in Deep Attention Networks](https://arxiv.org/abs/2511.22606). Rowzatul Zannath Prerona. *arXiv:2511.22606 [eess.IV]*, Nov 2025.

---

## 2. Computer Vision & Deep Learning Architectures

Alongside domain-specific medical imaging work, I maintain a strong interest in foundational computer vision research — particularly in the design of attention mechanisms, spatial feature selection, and efficient backbone architectures. My work on SG-Net grew directly from questioning assumptions embedded in standard soft-attention designs, and I continue to explore how architectural choices at the feature-selection level propagate into downstream task performance. I am especially interested in bridging the gap between academically performant models and architectures that remain computationally tractable under real-world deployment constraints.

---

## 3. Trustworthy & Robust Medical AI

Accuracy alone is an insufficient bar for medical AI. A model that performs well on benchmark datasets but fails unpredictably on out-of-distribution clinical scans, or that provides no mechanism for a clinician to audit its reasoning, introduces risk rather than reducing it. My research takes this seriously: I study systematic failure modes in deployed architectures, develop training and evaluation protocols that surface precision–recall trade-offs obscured by aggregate metrics like Dice, and design models whose decision boundaries are structurally constrained rather than post-hoc explained. The goal is AI that earns clinical trust by construction — not by coincidence.