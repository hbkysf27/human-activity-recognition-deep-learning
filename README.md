# 🧠 Human Activity Recognition (Deep Learning)

A deep learning project focused on **classifying human activities from multivariate time-series sensor data** using sequential and convolutional neural networks.

This project was developed as part of an MSc in Artificial Intelligence & Robotics coursework, exploring model design, training, and evaluation for real-world activity recognition.

---

## 🚀 Overview

The goal of this project is to automatically classify human activities such as:

* Walking
* Walking Upstairs
* Walking Downstairs
* Sitting
* Standing
* Laying

using **accelerometer and gyroscope sensor data**.

---

## 🗂 Dataset

* Multivariate time-series data (x, y, z axes)
* Sensor types:

  * Accelerometer
  * Gyroscope
* Preprocessing:

  * Standardization (zero mean, unit variance)
  * Label encoding (0–5 classes)
  * Sequence window segmentation

---

## 🧱 Models Implemented

The following deep learning models were designed and evaluated:

### 🔹 RNN

* Captures sequential dependencies
* Limited by vanishing gradients

### 🔹 LSTM

* Uses gating mechanisms for long-term dependencies
* Strong baseline performance

### 🔹 BiLSTM ⭐ (Best Model)

* Processes sequences forward & backward
* Captures full temporal context
* Achieved highest accuracy

### 🔹 CNN1D

* Extracts temporal features using convolution
* Faster training and efficient inference

---

## ⚙️ Training Configuration

* Optimizer: Adam (lr = 1e-3)
* Loss Function: CrossEntropyLoss
* Epochs: 15
* Regularization:

  * Dropout (0.2–0.3)
  * Gradient Clipping (max_norm=1.0)
* Scheduler:

  * Cosine learning rate with warm-up
* Mixed Precision Training (AMP) enabled

---

## 📊 Results

| Model  | Accuracy  | AUROC     | Notes                            |
| ------ | --------- | --------- | -------------------------------- |
| RNN    | ~0.89     | ~0.94     | Struggles with long dependencies |
| LSTM   | ~0.92     | ~0.96     | Strong generalisation            |
| BiLSTM | **~0.94** | **~0.97** | ⭐ Best performance               |
| CNN1D  | ~0.93     | ~0.96     | Fast & efficient                 |

---

## 📈 Evaluation

* Metrics:

  * Accuracy
  * Precision / Recall / F1-score
  * AUROC (One-vs-Rest)
* Confusion Matrix analysis
* Error analysis for misclassified activities

---

## 🔍 Key Insights

* **BiLSTM performed best** due to bidirectional temporal learning
* CNN1D achieved similar performance with lower computational cost
* RNN showed limitations in capturing long-range dependencies
* Temporal context is critical for accurate activity recognition

---

## 🛠 Tech Stack

* PyTorch
* Deep Learning (RNN, LSTM, CNN)
* Time-Series Analysis
* DataLoader & GPU Training

---

## 📸 Project Highlights

* End-to-end deep learning pipeline
* Multiple model comparisons
* Real-world dataset handling
* Performance visualization & analysis

---

## 📂 Project Structure

```
├── data/
├── notebooks/
├── models/
├── results/
├── utils/
└── README.md
```

---

## 📌 Future Improvements

* Hyperparameter tuning (Optuna / Grid Search)
* Transformer-based models (e.g., Time Series Transformers)
* Real-time deployment (Edge / IoT systems)
* Model compression for mobile inference

---

## 🤝 Acknowledgements

University of Aberdeen
MSc Artificial Intelligence & Robotics
CS5062 – Machine Learning

---

## 📬 Contact

If you’d like to collaborate or discuss this project, feel free to connect!
