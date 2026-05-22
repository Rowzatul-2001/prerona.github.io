---
layout: default
title: Research
permalink: /research/
---

# Research

My research focuses on the intersection of **Medical Image Processing** and **Computer Vision**, with a particular emphasis on developing robust deep learning architectures for clinical applications. I am especially interested in precision-driven segmentation, attention mechanisms, and building reliable AI systems that can be safely deployed in real-world healthcare settings.

The key areas I am currently exploring are listed below.

---

## 1. Medical Image Processing & Brain Tumor Segmentation

Brain metastasis segmentation in MRI poses unique challenges due to diminutive lesion sizes (5–15 mm) and extreme class imbalance (less than 2% tumor volume). Conventional soft-attention CNNs are prone to an *over-segmentation paradox* — achieving high sensitivity but suffering catastrophic precision collapse and large boundary errors, which poses significant risks for stereotactic radiosurgery planning.

To address this, my work introduces **SG-Net (Spatial Gating Network)**, a precision-first architecture that employs hard spatial gating mechanisms. Unlike soft attention, SG-Net enforces strict feature selection to aggressively suppress background artifacts while preserving tumor features. Validated on the Brain-Mets-Lung-MRI dataset (n=92), SG-Net achieves:

- **Dice Similarity Coefficient:** 0.5578 ± 0.0243 (95% CI: 0.45–0.67)
- **95% Hausdorff Distance:** 56.13 mm (vs. 157.52 mm for Attention U-Net)
- **Precision:** 0.52 vs. 0.20 (Attention U-Net), statistically significant (p < 0.001)
- **Model size:** Only 0.67M parameters — 8.8× fewer than Attention U-Net

These findings establish hard spatial gating as a robust solution for precision-driven lesion detection, directly enhancing radiosurgery accuracy.

**Related Paper:**
- [Hard Spatial Gating for Precision-Driven Brain Metastasis Segmentation: Addressing the Over-Segmentation Paradox in Deep Attention Networks](https://arxiv.org/abs/2511.22606). Rowzatul Zannath Prerona. *arXiv:2511.22606 [eess.IV]*, Nov 2025.

---

## 2. Computer Vision & Deep Learning Architectures

Beyond medical imaging, I am broadly interested in developing efficient and interpretable deep learning models for vision tasks. This includes exploring attention mechanisms, feature selection strategies, and lightweight architectures that balance performance with computational feasibility — qualities essential for deployment in resource-constrained clinical environments.

---

## 3. Trustworthy & Robust Medical AI

A core motivation behind my research is ensuring that AI systems designed for healthcare are not only accurate but also safe and trustworthy. This involves studying failure modes of existing models (such as over-segmentation), improving boundary precision, and working toward systems that clinicians can rely on for high-stakes decisions like radiosurgery planning.