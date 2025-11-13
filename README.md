# 🧠 Handwritten Digit Recognition (MNIST)

A **Pattern Recognition Mini Project** that implements a **Convolutional Neural Network (CNN)** to recognize handwritten digits (0–9) using the **MNIST dataset**.  
This project demonstrates the use of modern deep learning techniques for **pattern recognition** tasks.

---

## 📘 Project Overview
This project aims to:
- Develop a machine learning model to classify handwritten digits.
- Apply pattern recognition concepts using convolutional neural networks.
- Understand preprocessing, feature extraction, and model evaluation.

---

## 📊 Dataset Description
**Dataset:** [MNIST Handwritten Digit Dataset](http://yann.lecun.com/exdb/mnist/)  
- **Training samples:** 60,000  
- **Test samples:** 10,000  
- **Image size:** 28×28 pixels (grayscale)  
- **Classes:** Digits 0–9  

Each image is labeled with its corresponding digit, providing data for supervised learning.

---

## ⚙️ Methodology

### 1. Data Loading & Visualization
- Load MNIST data using TensorFlow.
- Visualize random samples for inspection.

### 2. Preprocessing
- Normalize pixel values between 0 and 1.
- Reshape images to `(28, 28, 1)` for CNN input.
- Convert labels to one-hot encoded vectors.

### 3. Model Development
- Sequential CNN architecture with convolutional, pooling, batch normalization, dropout, and dense layers.
- Uses **ReLU** activation and **Softmax** for output.

### 4. Training
- Optimizer: **Adam (lr = 0.001)**
- Loss: **Categorical Crossentropy**
- Early stopping & checkpointing enabled.
- Data augmentation applied for better generalization.

### 5. Evaluation
- Accuracy and loss plots.
- Confusion matrix and classification report.
- Visualization of random test predictions.

---

## 🧩 Model Architecture
| Layer | Output Shape | Parameters |
|:------|:--------------|-----------:|
| Conv2D (32 filters, 3×3) | (26, 26, 32) | 320 |
| BatchNormalization | (26, 26, 32) | 128 |
| MaxPooling2D | (13, 13, 32) | 0 |
| Conv2D (64 filters, 3×3) | (11, 11, 64) | 18,496 |
| BatchNormalization | (11, 11, 64) | 256 |
| MaxPooling2D | (5, 5, 64) | 0 |
| Conv2D (128 filters, 3×3) | (3, 3, 128) | 73,856 |
| BatchNormalization | (3, 3, 128) | 512 |
| Flatten + Dropout(0.4) | (1152) | 0 |
| Dense (128, ReLU) + Dropout(0.3) | (128) | 147,584 |
| Output Dense (Softmax) | (10) | 1,290 |

**Total Parameters:** 242,954  
**Trainable Parameters:** 242,250  

---

## 📈 Results

| Metric | Value |
|:--------|:-------|
| **Training Accuracy** | 98.7% |
| **Validation Accuracy** | 99.2% |
| **Test Accuracy** | 99.4% |

The confusion matrix showed only minor misclassifications, proving strong generalization capability.

---


