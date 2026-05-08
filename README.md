# 🐦 Bird Species Classification using Deep Learning

A deep learning project focused on **multi-class bird species classification** across **525 bird species** using Convolutional Neural Networks (CNNs) and Transfer Learning techniques in TensorFlow/Keras.

This project explores and compares multiple architectures ranging from a custom CNN model to a pre-trained MobileNetV2 network, with a focus on improving generalization and reducing overfitting.

---

# 📌 Project Overview

The objective of this project is to classify bird images into one of **525 species** using deep learning models trained on a large-scale bird image dataset.

The dataset contains approximately:

- **84,632 training images**
- **2,625 validation images**
- **2,625 test images**

Total dataset size is roughly **90,000 images**.

The project investigates:

- Custom CNN architectures
- Transfer learning
- Overfitting mitigation using Dropout regularization
- Model comparison and performance analysis

---

# 🧠 Models Implemented

## 1️⃣ Custom CNN Architecture

A custom Convolutional Neural Network built from scratch using:

- Conv2D layers
- MaxPooling
- Batch Normalization
- GlobalAveragePooling
- Dense layers

### Results

| Metric | Value |
|---|---|
| Training Accuracy | 56.29% |
| Training Loss | 1.8379 |
| Validation Accuracy | 61.71% |
| Validation Loss | 1.7174 |
| Epochs | 20 |

### Observations

- The model achieved reasonable performance despite being trained from scratch.
- Validation accuracy exceeded training accuracy, indicating good regularization and generalization behavior.

---

## 2️⃣ Transfer Learning with MobileNetV2

The second approach utilized **MobileNetV2** with pre-trained ImageNet weights.

### Results

| Metric | Value |
|---|---|
| Training Accuracy | 97.67% |
| Training Loss | 0.0706 |
| Validation Accuracy | 86.17% |
| Validation Loss | 0.9547 |
| Epochs | 20 |

### Observations

- Transfer learning dramatically improved classification performance.
- The model learned highly discriminative image features.
- However, the gap between training and validation accuracy suggested signs of overfitting.

---

## 3️⃣ MobileNetV2 + Dropout Regularization

To reduce overfitting observed in the previous model, Dropout regularization (`Dropout = 0.2`) was added during training.

### Results

| Metric | Value |
|---|---|
| Training Accuracy | 89.45% |
| Training Loss | 0.3720 |
| Validation Accuracy | 86.32% |
| Validation Loss | 0.6994 |
| Epochs | 20 |

### Observations

- Adding Dropout improved generalization.
- Validation loss decreased significantly.
- The model became more robust while maintaining high validation accuracy.

---

# 📊 Model Comparison

| Model | Train Acc | Val Acc | Train Loss | Val Loss |
|---|---|---|---|---|
| Custom CNN | 56.29% | 61.71% | 1.8379 | 1.7174 |
| MobileNetV2 | 97.67% | 86.17% | 0.0706 | 0.9547 |
| MobileNetV2 + Dropout | 89.45% | **86.32%** | 0.3720 | **0.6994** |

---

# 🛠️ Technologies Used

- Python
- TensorFlow / Keras
- Matplotlib

---

# 🧪 Training Techniques

The following techniques were explored throughout experimentation:

- Transfer Learning
- Data Augmentation (Due to poor performance, not included in the code.)
- Dropout Regularization
- Batch Normalization

---

# 📂 Dataset

The dataset is publicly available on Kaggle and contains images from **525 bird species**.

Due to current connectivity limitations, the dataset link is not included in this repository.
