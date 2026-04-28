#  Generator-Invariant Deepfake Detection Framework

##  Overview
Deepfake generation has rapidly evolved with the rise of **GANs (Generative Adversarial Networks)** and **diffusion-based models** such as Stable Diffusion and SDXL. While existing detection systems perform well on known generators, they fail significantly when tested on **unseen generators**.

This repository contains the implementation of a **cross-generator deepfake detection framework** designed to learn **generator-invariant features**, enabling robust detection across multiple generative models.

---

##  Research Objective
The goal of this research is to:

- Develop a **generator-agnostic deepfake detection model**
- Improve **cross-generator generalization**
- Reduce performance drop when testing on unseen generators
- Build a **future-proof forensic system**

---

##  Problem Statement
Current deepfake detectors:
- Learn **generator-specific artifacts**
- Perform well on known datasets
- Fail on unseen generators (especially diffusion models)

This research addresses the **cross-generator generalization problem**

---

##  Proposed Solution
We propose a framework that integrates:

### 1. CNN Backbone
- EfficientNet / ResNet for feature extraction

### 2. Domain-Adversarial Learning (DANN)
- Gradient Reversal Layer (GRL)
- Forces learning of **generator-invariant features**

### 3. Contrastive Learning
- Pulls similar samples together (real-real, fake-fake)
- Pushes different samples apart (real-fake)

### 4. Feature Consistency Learning
- Ensures features remain stable across generators

### 5. Binary Classifier
- Final classification: **Real vs Fake**

---

## 🧪 Experimental Design

### 📂 Dataset Structure (Used in this Repo)
