<p align="center">
  <img src="https://www.ntua.gr/images/logo/pyrforos.png" alt="NTUA Logo" width="100"/>
</p>

<h1 align="center">🤖 Machine Learning — NTUA</h1>
<h3 align="center">School of Electrical & Computer Engineering — Academic Year 2025-26</h3>

<p align="center">
  <img src="https://img.shields.io/badge/Course-Machine%20Learning-blueviolet?style=for-the-badge" alt="Course"/>
  <img src="https://img.shields.io/badge/University-NTUA-orange?style=for-the-badge" alt="NTUA"/>
  <img src="https://img.shields.io/badge/Language-Python-blue?style=for-the-badge&logo=python&logoColor=white" alt="Python"/>
  <img src="https://img.shields.io/badge/Platform-Google%20Colab-F9AB00?style=for-the-badge&logo=googlecolab&logoColor=white" alt="Colab"/>
</p>

---

## 📖 Overview

This repository contains the two individual lab projects for the **Machine Learning** course (Μηχανική Μάθηση) at the National Technical University of Athens (NTUA), School of Electrical & Computer Engineering (ΣΗΜΜΥ). Both projects are implemented as Jupyter Notebooks designed to run on Google Colab.

> **Student:** Ζωή Τσουρούφλη (Zoe Tsouroufli)
> **Student ID:** 03122062

---

## 📁 Repository Structure

```
.
├── ML2025_labproject1__03122062_TsouroufliZoi.ipynb    # Lab Project 1
├── ML25_labproject2_03122062_TsouroufliZoi.ipynb.ipynb # Lab Project 2
├── train-val (1).csv                                   # Dataset for Project 1
├── indian_pines_corrected.npy                          # Hyperspectral data for Project 2
├── indian_pines_gt.npy                                 # Ground truth labels for Project 2
└── README.md
```

---

## 🔬 Lab Project 1 — Weather Prediction (Classification)

### 📋 Description

A complete **supervised classification** pipeline on an Australian weather dataset. The goal is to predict whether it will **rain tomorrow** (`RainTomorrow`) based on meteorological features such as temperature, humidity, pressure, wind, and cloud cover.

### 📊 Dataset

- **Source:** `train-val.csv` — Australian weather observations
- **Samples:** 10,000 records
- **Features:** 23 columns including `MinTemp`, `MaxTemp`, `Rainfall`, `Humidity`, `Pressure`, `WindSpeed`, etc.
- **Target:** `RainTomorrow` (binary classification: Yes / No)

### 🔧 Pipeline

| Step | Description |
|------|-------------|
| **1. Data Loading** | Load and inspect the CSV dataset |
| **2. EDA** | Exploratory Data Analysis — sample counts, feature types, class distribution, correlation heatmap |
| **3. Preprocessing** | Handle missing values, encode categorical features, normalize numerical features |
| **4. Classification** | Train and evaluate multiple ML classifiers |
| **5. Evaluation** | Compare models using accuracy, precision, recall, F1-score |

### 🧠 Models Used

- K-Nearest Neighbors (KNN)
- Support Vector Machines (SVM)
- Decision Trees
- And more classical ML algorithms

### 📦 Dependencies

```python
pandas, numpy, scikit-learn, seaborn, matplotlib
```

---

## 🛰️ Lab Project 2 — Hyperspectral Image Classification (Deep Learning)

### 📋 Description

A **deep learning approach** to hyperspectral image classification using the **Indian Pines** dataset. The project uses **transfer learning** with **EfficientNetB0** to classify land cover types from hyperspectral satellite imagery.

### 📊 Dataset

- **Name:** Indian Pines
- **Data:** `indian_pines_corrected.npy` — Corrected hyperspectral image data
- **Labels:** `indian_pines_gt.npy` — Ground truth pixel-wise land cover classification
- **Type:** Hyperspectral remote sensing data with multiple spectral bands

### 🧠 Model Architecture

| Component | Details |
|-----------|---------|
| **Base Model** | EfficientNetB0 (pre-trained, transfer learning) |
| **Total Parameters** | ~4.05M (15.45 MB) |
| **Trainable Parameters** | ~4.01M (15.29 MB) |
| **Framework** | TensorFlow / Keras |

### 🔧 Key Techniques

- **Transfer Learning** from EfficientNetB0 pre-trained weights
- **Data Preprocessing** with rescaling and normalization layers
- **Batch Normalization** throughout the network
- **Squeeze-and-Excitation (SE) blocks** for channel attention
- **Depthwise Separable Convolutions** for efficient computation

### 📦 Dependencies

```python
tensorflow, keras, numpy, matplotlib
```

---

## ⚙️ How to Run

Both notebooks are designed to run on **Google Colab**:

1. Open the desired `.ipynb` file
2. Upload it to [Google Colab](https://colab.research.google.com/)
3. Upload the required data files to the Colab environment
4. Run all cells sequentially

### Local Setup (Alternative)

```bash
# Clone the repository
git clone https://github.com/zoetsouroufli/ml-25-26.git
cd ml-25-26

# Install dependencies
pip install pandas numpy scikit-learn seaborn matplotlib tensorflow keras

# Launch Jupyter
jupyter notebook
```

---
