# Rice Varieties Bangladesh Classification

<p align="center">
  <img src="https://img.shields.io/badge/Project-Rice%20Variety%20Classification-brightgreen" />
  <img src="https://img.shields.io/badge/Domain-Computer%20Vision-blue" />
  <img src="https://img.shields.io/badge/Methods-Supervised%20%2B%20SSL-purple" />
  <img src="https://img.shields.io/badge/Language-Python-orange" />
  <img src="https://img.shields.io/badge/Notebook-Jupyter-yellow" />
</p>

## Overview

**Rice Varieties Bangladesh Classification** is a computer vision project focused on classifying Bangladeshi rice varieties from image data. The project compares supervised transfer learning models with self-supervised learning methods to understand how different deep learning approaches perform on rice variety classification.

The repository includes exploratory data analysis, supervised baseline experiments, self-supervised learning experiments, result summaries, visualizations, and final presentation materials.

---

## Author

**Mahim Katha**  
GitHub: [MahimKatha02](https://github.com/MahimKatha02)

---

## Project Goals

- Classify Bangladeshi rice varieties using image-based deep learning.
- Perform exploratory data analysis on rice image data.
- Build supervised baseline models using transfer learning.
- Evaluate self-supervised learning methods for feature representation.
- Compare model performance using accuracy, precision, recall, F1-score, ROC-AUC, and confusion matrices.
- Organize the full project with code, results, reports, plots, and presentation files.

---

## Dataset Information

| Item | Details |
|---|---|
| Dataset type | Rice variety image dataset |
| Task | Multi-class image classification |
| Domain | Agriculture, food grain analysis, computer vision |
| Data format | Image-based dataset |
| Main objective | Identify the correct rice variety from rice grain images |

---

## Methods Used

The project uses both supervised and self-supervised learning approaches.

### Supervised Learning

The supervised baseline experiments were performed using transfer learning models with different train-test split ratios.

Models used:

| Model |
|---|
| DenseNet121 |
| EfficientNetB0 |
| InceptionV3 |
| MobileNetV2 |
| ResNet50 |

Train-test splits tested:

| Split Type |
|---|
| 10/90 |
| 20/80 |
| 30/70 |
| 40/60 |
| 50/50 |
| 60/40 |
| 70/30 |
| 80/20 |
| 90/10 |

### Self-Supervised Learning

Self-supervised learning methods were used to learn image representations before classification.

| Task | Method |
|---|---|
| Task 4 | SimCLR |
| Task 5 | BYOL |
| Task 6 | DINO |

---

## Workflow

```text
Rice Image Dataset
        │
        ▼
Exploratory Data Analysis
        │
        ▼
Supervised Baseline Experiments
        │
        ├── DenseNet121
        ├── EfficientNetB0
        ├── InceptionV3
        ├── MobileNetV2
        └── ResNet50
        │
        ▼
Self-Supervised Learning Experiments
        │
        ├── SimCLR
        ├── BYOL
        └── DINO
        │
        ▼
Model Evaluation
        │
        ├── Accuracy
        ├── Precision
        ├── Recall
        ├── F1-Score
        ├── ROC-AUC
        └── Confusion Matrix
        │
        ▼
Result Comparison and Final Presentation
