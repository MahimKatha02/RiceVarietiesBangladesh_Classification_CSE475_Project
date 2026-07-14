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
**Akibul Hasan Arman (Project Collaborator)**
GitHub: [abarman079](https://github.com/abarman079)

---

## Project Goals

* Classify Bangladeshi rice varieties using image-based deep learning.
* Perform exploratory data analysis on rice image data.
* Build supervised baseline models using transfer learning.
* Evaluate self-supervised learning methods for feature representation.
* Compare model performance using accuracy, precision, recall, F1-score, ROC-AUC, and confusion matrices.
* Organize the full project with code, results, reports, plots, and presentation files.

---

## Dataset Information

| Item           | Details                                                  |
| -------------- | -------------------------------------------------------- |
| Dataset type   | Rice variety image dataset                               |
| Task           | Multi-class image classification                         |
| Domain         | Agriculture, food grain analysis, computer vision        |
| Data format    | Image-based dataset                                      |
| Main objective | Identify the correct rice variety from rice grain images |

---

## Methods Used

The project uses both supervised and self-supervised learning approaches.

### Supervised Learning

The supervised baseline experiments were performed using transfer learning models with different train-test split ratios.

| Model          |
| -------------- |
| DenseNet121    |
| EfficientNetB0 |
| InceptionV3    |
| MobileNetV2    |
| ResNet50       |

Train-test splits tested:

| Split Type |
| ---------- |
| 10/90      |
| 20/80      |
| 30/70      |
| 40/60      |
| 50/50      |
| 60/40      |
| 70/30      |
| 80/20      |
| 90/10      |

### Self-Supervised Learning

Self-supervised learning methods were used to learn image representations before classification.

| Task   | Method |
| ------ | ------ |
| Task 4 | SimCLR |
| Task 5 | BYOL   |
| Task 6 | DINO   |

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
```

---

## Repository Structure

```text
RiceVarietiesBangladesh_Classification_CSE475_Project/
│
├── Code/
│   ├── Task-2/
│   │   ├── supervised-baseline-10-90.ipynb
│   │   ├── supervised-baseline-20-80.ipynb
│   │   ├── supervised-baseline-30-70.ipynb
│   │   ├── supervised-baseline-40-60.ipynb
│   │   ├── supervised-baseline-50-50.ipynb
│   │   ├── supervised-baseline-60-40.ipynb
│   │   ├── supervised-baseline-70-30.ipynb
│   │   ├── supervised-baseline-80-20.ipynb
│   │   └── supervised-baseline-90-10.ipynb
│   │
│   ├── Task - 4/
│   │   └── task4-simclr-rice-classification.ipynb
│   │
│   ├── Task - 5/
│   │   └── task5-byol-rice-classification.ipynb
│   │
│   └── Task - 6/
│       └── ssl-dino.ipynb
│
├── Results/
│   ├── Task-2 (Baseline)/
│   │   ├── Model_Reports/
│   │   └── Result_Plots/
│   │
│   ├── Task-3(SSL Method)/
│   │   └── Three Main SSL Method.pdf
│   │
│   ├── Task - 4(SimCLR)/
│   │   └── simclr_results_summary.csv
│   │
│   ├── Task - 5 (BYOL)/
│   │   ├── byol_results_summary.csv
│   │   ├── byol_finetuning_curves.png
│   │   ├── byol_training_curves.png
│   │   ├── confusion_matrix_byol.png
│   │   ├── embedding_visualizations_byol.png
│   │   └── learning_curves_byol.png
│   │
│   └── Task - 6(SSL Dino)/
│       ├── classifier_comparison.csv
│       ├── per_class_performance.csv
│       ├── training_loss_by_epoch.csv
│       └── result visualizations
│
├── Rice_Varities_EDA/
│   ├── rice_varities_EDA.ipynb
│   └── Rice_Varities_Related-Work.pdf
│
└── 475 final_slides.pptx
```

---

## Result Summary

### SimCLR Result

| Method           | Accuracy | Precision | Recall | F1-Score | ROC-AUC |
| ---------------- | -------: | --------: | -----: | -------: | ------: |
| Linear Probe     |   50.93% |    0.5285 | 0.5093 |   0.4930 |  0.9644 |
| Fine-Tuned Model |    3.12% |    0.0036 | 0.0312 |   0.0063 |     N/A |

### BYOL Result

| Classifier / Method | Accuracy | Difference from Baseline |
| ------------------- | -------: | -----------------------: |
| Linear Probe        |   64.65% |                  -10.35% |
| MLP                 |   72.75% |                   -2.25% |
| SVM                 |   54.60% |                  -20.40% |
| Decision Tree       |   40.88% |                  -34.12% |
| Random Forest       |   59.96% |                  -15.04% |
| Fine-Tuned Model    |   13.40% |                  -61.60% |

### DINO Result

| Classifier   | Accuracy | Precision | Recall | F1-Score |
| ------------ | -------: | --------: | -----: | -------: |
| Linear Probe |   28.87% |    0.2862 | 0.2862 |   0.2862 |
| MLP          |   35.82% |    0.3598 | 0.3598 |   0.3598 |
| SVM          |   10.79% |    0.1044 | 0.1044 |   0.1044 |

---

## Best Performing Methods

| Approach | Best Method    | Best Accuracy |
| -------- | -------------- | ------------: |
| SimCLR   | Linear Probe   |        50.93% |
| BYOL     | MLP Classifier |        72.75% |
| DINO     | MLP Classifier |        35.82% |

---

## Key Findings

* Supervised transfer learning provides a strong baseline for rice variety image classification.
* BYOL with an MLP classifier achieved the best performance among the tested self-supervised learning methods.
* SimCLR performed better with frozen-feature linear probing than with full fine-tuning in this experiment.
* DINO produced useful image representations, but its classification accuracy was lower than BYOL and SimCLR in this project.
* The results show that self-supervised learning can be useful for agricultural image classification, especially when feature representations are paired with effective downstream classifiers.

---

## Technologies Used

| Category             | Tools / Libraries                      |
| -------------------- | -------------------------------------- |
| Programming Language | Python                                 |
| Notebook Environment | Jupyter Notebook                       |
| Deep Learning        | PyTorch / TensorFlow-based workflows   |
| Machine Learning     | Scikit-learn                           |
| Computer Vision      | Image preprocessing and classification |
| Visualization        | Matplotlib, Seaborn                    |
| Data Handling        | NumPy, Pandas                          |
| SSL Methods          | SimCLR, BYOL, DINO                     |

---

## How to Run This Project

### 1. Clone the Repository

```bash
git clone https://github.com/MahimKatha02/RiceVarietiesBangladesh_Classification_CSE475_Project.git
```

### 2. Navigate to the Project Folder

```bash
cd RiceVarietiesBangladesh_Classification_CSE475_Project
```

### 3. Open Jupyter Notebook

```bash
jupyter notebook
```

### 4. Run the Notebooks

Run the notebooks from the `Code/` folder based on the task:

| Folder           | Purpose                         |
| ---------------- | ------------------------------- |
| `Code/Task-2/`   | Supervised baseline experiments |
| `Code/Task - 4/` | SimCLR experiment               |
| `Code/Task - 5/` | BYOL experiment                 |
| `Code/Task - 6/` | DINO experiment                 |

---

## Evaluation Metrics

The models were evaluated using the following metrics:

| Metric           | Purpose                                               |
| ---------------- | ----------------------------------------------------- |
| Accuracy         | Measures overall correct predictions                  |
| Precision        | Measures correctness among predicted positive classes |
| Recall           | Measures how well actual classes are identified       |
| F1-Score         | Balances precision and recall                         |
| ROC-AUC          | Measures class separation capability                  |
| Confusion Matrix | Shows class-wise prediction performance               |

---

## Project Outputs

| Output                          | Location                                              |
| ------------------------------- | ----------------------------------------------------- |
| Baseline model reports          | `Results/Task-2 (Baseline)/Model_Reports/`            |
| Baseline result plots           | `Results/Task-2 (Baseline)/Result_Plots/`             |
| SSL method document             | `Results/Task-3(SSL Method)/`                         |
| SimCLR summary                  | `Results/Task - 4(SimCLR)/simclr_results_summary.csv` |
| BYOL summary and visualizations | `Results/Task - 5 (BYOL)/`                            |
| DINO classifier results         | `Results/Task - 6(SSL Dino)/`                         |
| Final presentation              | `475 final_slides.pptx`                               |

---

## Future Improvements

* Add a `requirements.txt` file for easier setup.
* Add dataset download and preparation instructions.
* Add a single training script for all experiments.
* Add more detailed class-wise comparison plots.
* Improve SSL fine-tuning strategies.
* Test additional architectures such as Vision Transformer, ConvNeXt, and EfficientNetV2.
* Add experiment tracking using MLflow, TensorBoard, or Weights & Biases.
* Add model checkpoints and reproducible configuration files.

---

## Academic Relevance

This project demonstrates how machine learning and computer vision can be applied to agricultural image classification. It also compares supervised learning and self-supervised representation learning for a practical classification task.

---

## Acknowledgement

This project was completed as part of an academic machine learning / computer vision study on rice variety classification.

If any dataset, code, or reference material is adapted from a third-party source, proper credit and licensing should be maintained.

---

## License

No license file has been added yet. Add an appropriate license before distributing or reusing this project publicly.
