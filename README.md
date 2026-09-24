# Breast Cancer Detection Using CNN

A deep learning project for classifying breast histopathology images into **Invasive Ductal Carcinoma (IDC)** and **Non-IDC** using a Convolutional Neural Network (CNN).

## 📌 Project Overview

Breast cancer is one of the most common cancers worldwide. Histopathology images can contain important visual patterns that help identify cancerous tissue.

In this project, I developed a CNN-based image classification model to distinguish between:

* **IDC** — Invasive Ductal Carcinoma
* **Non-IDC** — Tissue without IDC

The project uses TensorFlow and Keras for model development and evaluation.

## 📊 Dataset

The dataset was obtained from **Kaggle**.

The original dataset contained approximately **277,524 images**:

| Class     | Number of Images | Percentage |
| --------- | ---------------: | ---------: |
| Non-IDC   |          198,738 |     71.61% |
| IDC       |           78,786 |     28.39% |
| **Total** |      **277,524** |   **100%** |

For this project, a smaller balanced subset of **2,000 images** was used to make training practical.

### Dataset Split

| Dataset    |    Images |
| ---------- | --------: |
| Training   |     1,400 |
| Validation |       300 |
| Testing    |       300 |
| **Total**  | **2,000** |

Images were resized to **50 × 50 pixels** with **3 RGB channels**.

> The original dataset is not included in this repository because of its large size.

## 🛠️ Technologies

* Python
* TensorFlow
* Keras
* NumPy
* Pandas
* Matplotlib
* Scikit-learn
* Jupyter Notebook

## 🔄 Project Workflow

Dataset
   ↓
Image Selection
   ↓
Image Quality Checking
   ↓
Image Resizing
   ↓
Normalization
   ↓
Train / Validation / Test Split
   ↓
CNN Model
   ↓
Training
   ↓
Evaluation
   ↓
Prediction

## 🧠 Model

A Convolutional Neural Network was used for binary image classification.

The model learns visual features from the histopathology images and predicts whether an image belongs to the IDC or Non-IDC class.

### Training Configuration

* Image size: **50 × 50 × 3**
* Batch size: **32**
* Epochs: **15**
* Number of classes: **2**
* Framework: **TensorFlow / Keras**

## 📈 Results

The final model achieved:

| Metric        |     Result |
| ------------- | ---------: |
| Test Accuracy | **76.67%** |
| ROC-AUC       | **0.8669** |

### Confusion Matrix

[[96, 54],
 [16, 134]]

The classification results show that the model was able to distinguish between the two classes, while also producing some false positive and false negative predictions.

## 📊 Classification Performance

For the IDC class:

* Precision: **71.28%**
* Recall: **89.33%**
* F1-score: **79.29%**

The ROC-AUC of **0.8669** indicates that the model demonstrated useful discrimination between the two classes on the test set.

## 📁 Repository Structure

breast-cancer-detection-cnn/
│
├── README.md
│
├── notebooks/
│   └── breast_cancer_detection.ipynb
│
└── results/

## 🚀 How to Run

### 1. Clone the repository

git clone https://github.com/mintesnotbekele26-collab/breast-cancer-detection-cnn.git


### 2. Install the required libraries

bash
pip install tensorflow numpy pandas matplotlib scikit-learn

### 3. Open the notebook

jupyter notebook

Then open:

notebooks/breast_cancer_detection.ipynb

### 4. Dataset

Download the dataset from Kaggle and place the required image files in the appropriate dataset directory before running the notebook.

## ⚠️ Limitations

* The project uses a subset of the original dataset rather than all available images.
* The model is a research/educational project and is **not intended for clinical diagnosis**.
* Further validation on larger and independent datasets would be required before considering real-world medical use.

## 🔮 Future Improvements

* Train using a larger portion of the dataset.
* Apply transfer learning with architectures such as ResNet or EfficientNet.
* Improve class balancing and augmentation strategies.
* Perform more extensive hyperparameter tuning.
* Evaluate the model on an independent external dataset.
* Develop a simple deployment interface for demonstration.

## 👨‍💻 Author

**Mintesnot Bekele**

This project was developed as part of my learning and practical work in **Computer Vision and Deep Learning**.
