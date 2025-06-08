# 🧱 Surface Crack Detection – ML & DL Hybrid Approach

This project presents a hybrid system for detecting surface cracks in concrete using both traditional machine learning and modern deep learning models. Using a publicly available dataset of 40,000 grayscale images, we compare the performance of hand-crafted feature models like SVM/KNN against CNN and Inception-based architectures.

## 📂 Dataset

- **Source**: [Kaggle - Surface Crack Detection Dataset](https://www.kaggle.com/datasets/arunrk7/surface-crack-detection)
- **Size**: 40,000 grayscale images (227×227 pixels)
  - 20,000 with cracks (positive)
  - 20,000 without cracks (negative)
- **Split**: 80% training, 20% validation

## 🧪 Techniques & Models

### 🔍 Traditional ML Pipeline
- **HOG** (Histogram of Oriented Gradients) for spatial edge feature extraction
- **PCA** to reduce dimensionality from 1764 to 100
- **SVM**:
  - Linear kernel, robust generalization
  - Accuracy: 98.75%
- **KNN**:
  - k = 5, distance-weighted voting
  - Accuracy: 89.5%

### 🧠 Deep Learning Pipeline

#### CNN Architecture
- 3× Convolutional + MaxPooling layers
- Dropout (0.3–0.5) for regularization
- Dense → Sigmoid output
- Accuracy: 99.62%

#### 🕸️ Inception-based CNN
- Multi-scale feature extraction using 1×1, 3×3, and 5×5 filters
- 3 Inception blocks
- L2 Regularization + Dropout
- Accuracy: **99.70%**

## 📈 Results

| Model              | Accuracy | Precision | Recall | F1-Score |
|-------------------|----------|-----------|--------|----------|
| SVM               | 98.75%   | 0.99      | 0.98   | 0.99     |
| KNN               | 89.5%    | 1.00      | 0.80   | 0.89     |
| CNN               | 99.62%   | 0.99–1.00 | 0.99   | 0.99     |
| Inception CNN     | 99.70%   | 0.99–1.00 | 1.00   | 1.00     |

## 📊 Visualizations

- 📉 Learning Curves
- 📊 Confusion Matrices
- 📷 Sample image augmentations (rotations, flips, shears)

## 🔁 Preprocessing Steps

- Resizing to 64×64 (ML) or 128×128×3 (DL)
- Normalization (pixel values [0–1])
- Augmentation: Rotation, Zoom, Shear, Flip

📎 **GitHub Repository**: [https://github.com/call-me-jot/surface-crack-detector](https://github.com/call-me-jot/surface-crack-detector)


---
