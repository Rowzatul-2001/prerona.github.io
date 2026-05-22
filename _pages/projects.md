---
layout: archive
title: Projects
permalink: /projects/
author_profile: true
---

# Projects

A collection of research-oriented and applied projects spanning medical image analysis, computer vision, and software development.

---

## 1. EfficientNet-CBAM: Attention-Guided Brain Tumor Classification

Early and accurate brain tumor diagnosis is critical for guiding therapeutic decisions and improving patient outcomes. This project presents a novel attention-guided deep learning framework for multi-class brain tumor classification from MRI scans, combining high accuracy with clinical interpretability. The architecture integrates a **Convolutional Block Attention Module (CBAM)** into an EfficientNetB3 backbone, enabling the model to focus on pathologically relevant regions rather than irrelevant background features. Explainability is addressed through **HiResCAM** gradient-based visualizations, which highlight tumor regions influencing each prediction — directly improving clinical trust. The model is trained and validated on publicly available MRI datasets covering Glioma, Meningioma, and Pituitary Tumor classes, achieving a classification accuracy of **99.29%** with comparative benchmarking against ResNet50, MobileNetV2, and EfficientNetB3 baselines.

**Tech Stack:** Python, TensorFlow, Keras, EfficientNetB3, CBAM, HiResCAM, OpenCV, NumPy, scikit-learn

**[View on GitHub](https://github.com/rowzatul-2001/pattern-recognition-and-machine-learning-Project-4.1)**

---

## 2. Deforestation Mapping in Dhaka — Semantic Segmentation

Rapid urbanization and industrialization in Dhaka, Bangladesh have caused significant land use changes over the past decade. This project builds a high-resolution satellite imagery dataset of Dhaka spanning 2012–2022 and applies deep learning-based semantic segmentation to detect and monitor deforested areas over time. Three architectures are implemented and benchmarked — **U-Net**, **Attention U-Net**, and a hybrid **ResNet50-Attention U-Net** — evaluated using Dice Score, IoU, F1-Score, Precision, and Recall. The project handles complex urban-forest boundary transitions and provides a reproducible framework for environmental change monitoring using remote sensing data.

**Tech Stack:** Python, TensorFlow, Keras, PyTorch, U-Net, Attention U-Net, ResNet50, NumPy, OpenCV, scikit-learn, matplotlib

**[View on GitHub](https://github.com/rowzatul-2001/Soft-Computing-Project-4.1)**

---

## 3. Spreed Love for Pet — Pet Management Desktop Application

A feature-rich desktop application designed to address the diverse day-to-day needs of pet owners. The application provides user profiles for personalized experiences, comprehensive pet profiles to track health and activity, an expense tracker for financial management, and an extensive pet health encyclopedia for quick reference. It also includes a community connectivity module for pet owners to interact, a pet BMI calculator, and a built-in tic-tac-toe game for leisure. The goal was to deliver a seamless, user-friendly interface that consolidates pet management, health monitoring, and community engagement in a single platform.

**Tech Stack:** Java

**[View on GitHub](https://github.com/rowzatul-2001/spreed_love_for_pet)**

---

## 4. Planet Paw — Animal Rescue & Welfare Platform

A multifaceted web platform designed to address critical gaps in animal rescue and welfare services. Planet Paw integrates donation processing, a pet adoption platform, educational resources on pet care, medical aid listings, and food sales — all within a single community-driven ecosystem. The platform emphasizes transparency, seamless user engagement, and environmental sustainability alongside animal welfare. Built with a PHP/MySQL backend and managed via XAMPP and phpMyAdmin, the system supports full CRUD operations for rescue listings, donor management, and inventory.

**Tech Stack:** PHP, HTML, CSS, JavaScript, MySQL, XAMPP, phpMyAdmin

**[View on GitHub](https://github.com/rowzatul-2001/planetPaw)** · **[Watch Screencast](https://www.youtube.com/watch?v=lbUFbhwnwf0)**

---

## 5. LeafLedger — Bookshop Management System

A full-stack bookshop management system built to streamline inventory, sales, and customer operations for a bookstore environment. The system supports book and genre management, shopping cart functionality, stock level monitoring, order processing, and admin-level operations including book approvals and homepage content management. Built on an ASP.NET Core MVC backend with a Bootstrap frontend and SQL Server database, LeafLedger provides a clean administrative interface suitable for real-world retail deployment.

**Tech Stack:** ASP.NET Core MVC, Bootstrap, HTML, CSS, SQL Server, .NET 8 SDK, SSMS

**[View on GitHub](https://github.com/rowzatul-2001/LeafLedger)**