# Neural Stochastic Embedded Clustering (NSEC)

**NSEC** is a deep clustering framework that integrates stochastic latent embeddings with clustering refinement. Unlike deterministic clustering methods, NSEC models uncertainty in the latent space, producing robust, interpretable cluster assignments. This repository contains the implementation in **PyTorch**, along with scripts for data preprocessing, training, evaluation, and visualization.

---

## Features

- **Stochastic Latent Embeddings:** Each data point is represented as a distribution in the latent space, capturing uncertainty.
- **Clustering Refinement:** Learnable cluster centroids with soft assignments, optimized jointly with the embeddings.
- **Uncertainty Quantification:** Provides calibrated entropy-based measures for ambiguous samples.
- **Baseline Comparison:** Evaluated against Bayesian Deep Clustering (BDC) and $k$-means.
- **Mixed-type Dataset Support:** Works with numerical and categorical features (one-hot encoded or factorized).

---

## Dataset

The model has been evaluated on an **obesity-related dataset** with 17 features, including physiological, lifestyle, and dietary attributes. Labels are used only for evaluation.  

- Numerical features are standardized (zero mean, unit variance).  
- Categorical features are factorized or one-hot encoded.  
- Class distribution is imbalanced, motivating stochastic embeddings.

---

## Installation

1. Clone this repository:
```bash
git clone https://github.com/<your-username>/NSEC.git
cd NSEC
