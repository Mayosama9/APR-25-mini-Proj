# APR-25-mini-Proj

This project builds and trains a **Convolutional Neural Network (CNN)** to recognize handwritten digits (0–9) from images.  
It uses the **MNIST dataset (CSV format)** stored in Google Drive and runs in **Google Colab**.

---

## 📁 Project Structure
MyDrive/
└── APR/
├── train.csv
├── test.csv
├── digit_recognition.ipynb
├── digit_recognition_model.h5
└── sample_digit.png


---

## 🚀 Features

- CNN model for handwritten digit recognition (0–9)  
- Trains on MNIST dataset (CSV format)  
- >98% accuracy on test data  
- Can predict digits from custom images  
- Saves trained model to Google Drive  

---

## 🧩 Model Architecture

| Layer | Type | Parameters |
|-------|------|-------------|
| 1 | Conv2D | 32 filters, 3×3 kernel, ReLU |
| 2 | MaxPooling2D | 2×2 pool size |
| 3 | Conv2D | 64 filters, 3×3 kernel, ReLU |
| 4 | MaxPooling2D | 2×2 pool size |
| 5 | Flatten | — |
| 6 | Dense | 64 units, ReLU |
| 7 | Output | 10 units, Softmax |

---

## 🧠 How to Run (Google Colab)

1. **Upload Dataset to Google Drive**
   - Create a folder named `APR` and upload `minst_train.csv` and `minst_test.csv`.

2. **Open in Google Colab**
   - open the APR.ipynb in google colab

3. **Mount Drive**
   ```python
   from google.colab import drive
   drive.mount('/content/drive')
4. Run the Notebook
  -The model will train and save to your Drive:/content/drive/MyDrive/APR/digit_recognition_model.h5
5. Predict Custom Images
   -predict_digit("/content/drive/MyDrive/APR/sample_digit.png")
   -Image Requirements: Contains one digit (0–9),Any size (auto-resized to 28×28)
