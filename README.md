# reCAPTCHA Image Classification using CNN (ResNet18)
## Overview
This project implements an image classification model to solve reCAPTCHA-style tasks.

The goal is to classify images into 12 categories (e.g., Bus, Car, Bicycle, Traffic Light), demonstrating that modern machine learning models can outperform traditional CAPTCHA assumptions.

---

## Method

A supervised learning approach was used with a deep convolutional neural network:

- Model: **ResNet18 (pretrained on ImageNet)**
- Framework: **PyTorch**
- Input size: **224 × 224**
- Data augmentation:
  - Horizontal flipping

### Training Setup
- Train/Validation split: **80% / 20%**
- Loss function: **Cross-Entropy Loss**
- Optimizer: **Adam**

To address class imbalance, a higher loss weight was assigned to the **Motorcycle** class.

---

## Dataset
- Training/Validation set: 3000 labeled images
- Test set: 8730 unlabeled images
- Total classes: 12

---

## Results
- Output: **Probability predictions for all classes**
- Format: CSV file (`result.csv`)
- Evaluation metric: Accuracy on test dataset

---

## Usage

### load training dataset and test dataset
```bash
train_val.zip
```
```bash
test.zip
```

### Train the model
```bash
train.ipynb
```

### output
The model generates a CSV file:
```bash
result.csv
```
Each row contains:
-Image name
-Predicted probabilities for all 12 classes
