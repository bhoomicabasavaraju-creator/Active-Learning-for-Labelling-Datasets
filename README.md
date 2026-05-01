 🧠 Active Learning Methods for Labeling Datasets

This repository contains the implementation of **Active Learning** techniques that help minimize manual labeling effort while achieving high model accuracy. The project applies **Least Confidence**, **Margin Sampling**, and **Entropy Sampling** strategies on popular datasets such as **CIFAR-10**, **EuroSAT**, and **Fashion MNIST**.

---

## 🚀 Overview

In supervised machine learning, model performance heavily depends on the availability of labeled data. However, labeling is time-consuming and expensive.  
**Active Learning** addresses this by iteratively selecting the most informative data samples for labeling, thereby reducing the overall labeling effort.

This project implements three popular active learning query strategies:
- **Least Confidence Sampling**
- **Margin Sampling**
- **Entropy-Based Sampling**

A **Convolutional Neural Network (CNN)** is used for training, and results are compared across datasets to demonstrate efficiency and accuracy improvements.

---

## 🎯 Objectives

- Reduce the number of labeled samples required for training.
- Improve model accuracy using actively selected data points.
- Compare and analyze multiple active learning strategies.

---

## ⚙️ Methodology

1. **Dataset Preparation**
   - Begin with a small labeled subset and a large unlabeled pool.
   - Datasets used: CIFAR-10, EuroSAT, Fashion MNIST.

2. **Model Training**
   - Train a CNN model on the initial labeled dataset.

3. **Active Learning Iteration**
   - Predict on unlabeled data.
   - Rank samples using one of the active learning strategies.
   - Add the most uncertain samples to the labeled pool.
   - Retrain the model.

4. **Repeat**
   - Iterate until optimal accuracy or stopping condition is reached.

---

## 🧩 Datasets Used

| Dataset | Description | Classes |
|----------|--------------|----------|
| **CIFAR-10** | 60,000 32×32 color images | 10 |
| **EuroSAT** | 27,000 Sentinel-2 satellite images | 10 |
| **Fashion MNIST** | 60,000 grayscale images | 10 |

---

## 🧠 Active Learning Techniques

### 1. Least Confidence
Selects samples for which the model has the **lowest prediction confidence**.

### 2. Margin Sampling
Selects samples where the difference between the two most probable classes is **smallest**, indicating uncertainty.

### 3. Entropy Sampling
Uses **entropy** of prediction probabilities to quantify uncertainty; higher entropy = more uncertainty.

---

## 🧰 Tools & Technologies

- **Language:** Python  
- **Libraries:** TensorFlow / Keras, NumPy, Pandas, Matplotlib, OpenCV  
- **Environment:** Google Colab / Jupyter Notebook  

---

## 📊 Results Summary

| Dataset | All Data Accuracy | Active Learning Accuracy | Reduction in Data |
|----------|-------------------|--------------------------|-------------------|
| CIFAR-10 | 70.49% | 71.5% (40,000 samples) | 33% less data |
| EuroSAT | 85.94% | 86.09% (20,000 samples) | 25% less data |
| Fashion MNIST | 86.11% | 87.2% (20,000 samples) | 33% less data |

Active learning methods significantly reduced the labeling effort while maintaining or improving accuracy.


   git clone https://github.com/your-username/active-learning-labeling.git
   cd active-learning-labeling
