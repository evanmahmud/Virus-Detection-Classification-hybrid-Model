# Hybrid CNN–Transformer Framework for TEM Virus Classification

## Overview

This repository contains the implementation of a deep learning framework for multi-class virus classification using Transmission Electron Microscopy (TEM) images. The study evaluates convolutional neural networks (CNNs), transformer-based architectures, and their hybrid ensemble for robust classification under class imbalance conditions.

The framework includes:

* 6 individual models (CNN + Transformer)
* Equal-weight and performance-weighted ensemble methods
* Comprehensive evaluation (Accuracy, Precision, Recall, F1, ROC, PR, Confusion Matrix)
* Visualization and result logging

---

## Dataset

The experiments are conducted on the **TEM Virus Dataset**:

* 1,245 images
* 22 virus classes
* High class imbalance
* Weak annotations (center points / centerlines)

Reference:
Matuszewski & Sintorn (2021)

---

## Models Implemented

### CNN Models

* ResNet50
* EfficientNetV2
* ConvNeXt

### Transformer Models

* Vision Transformer (ViT)
* Swin Transformer
* DeiT

### Hybrid Models

* Equal-weight ensemble
* Performance-weighted ensemble

---

## Project Structure

```
├── data/
├── models/
├── results/
│   ├── confusion/
│   ├── reports/
│   ├── plots/
├── train.py
├── evaluate.py
├── ensemble.py
├── utils.py
└── README.md
```

---

## Installation

```bash
pip install torch torchvision timm scikit-learn matplotlib seaborn tqdm
```

---

## Training

```bash
python train.py
```

Trains all models with:

* AdamW optimizer
* Cosine Annealing scheduler
* Weighted CrossEntropy loss (class imbalance handling)

---

## Evaluation

```bash
python evaluate.py
```

Generates:

* Accuracy, Precision, Recall, F1 Score
* Confusion matrices
* ROC curves
* Classification reports

All outputs are saved in the `results/` directory.

---

## Ensemble Evaluation

```bash
python ensemble.py
```

Includes:

* Equal-weight ensemble
* Weighted ensemble (based on model performance)

---

## Metrics

The following metrics are used:

* Accuracy
* Precision (macro)
* Recall (macro)
* F1 Score (macro)
* ROC-AUC (one-vs-rest)
* Precision-Recall curves

---

## Key Results

* Best standalone model: **Swin Transformer**
* Best overall model: **Weighted Hybrid Ensemble**
* Improved performance under class imbalance
* Better class-wise balance observed in hybrid models

---

## Features

* Handles class imbalance using weighted loss
* Supports multiple architectures
* Modular and extensible design
* Automatic visualization saving
* Reproducible training pipeline

---

## Future Work

* Detection + classification hybrid model
* Feature-level fusion strategies
* Scale-aware learning
* Larger TEM datasets

---

## Citation

If you use this work, please cite:

```
@article{your_paper,
  title={Hybrid CNN–Transformer Framework for TEM Virus Classification},
  author={Your Name},
  year={2026}
}
```

---

## License

This project is intended for research purposes.

---

## Contact

For questions or collaboration:

* Email: [cse.mahmud.evan@gmail.com](mailto:cse.mahmud.evan@gmail.com)
* GitHub: [Md Mahmudul Hoque](https://github.com/evanmahmud)
