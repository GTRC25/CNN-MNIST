# MNIST CNN Classifier

A Convolutional Neural Network (CNN) built using TensorFlow/Keras to classify handwritten digits (0–9) from the MNIST dataset.

---

## 🚀 Project Overview

This project demonstrates:
- Convolutional layers for feature extraction  
- Pooling layers for downsampling  
- Fully connected layers for classification  
- Regularization using Dropout  
- Early Stopping to prevent overfitting  
- Training visualization for performance analysis  

---

## Dataset

- Dataset: MNIST  
- Description: 28x28 grayscale images of handwritten digits (0–9)  
- Size:
  - Training: 60,000 images  
  - Testing: 10,000 images  

Loaded using:
from tensorflow.keras.datasets import mnist

---

## Model Architecture

Input (28x28x1)
↓
Conv2D (32 filters, 3x3) + ReLU
↓
MaxPooling (2x2)
↓
Conv2D (64 filters, 3x3) + ReLU
↓
MaxPooling (2x2)
↓
Flatten
↓
Dropout (0.3)
↓
Dense (64) + ReLU
↓
Dropout (0.3)
↓
Dense (10) + Softmax

---

## Training Details

- Optimizer: Adam  
- Loss Function: Sparse Categorical Crossentropy  
- Metrics: Accuracy  
- Epochs: Up to 20 (with Early Stopping)  

Early Stopping:
- Monitor: val_loss  
- Patience: 2  
- Restore best weights: Enabled  

---

## Results

- Training Accuracy: ~99%  
- Validation Accuracy: ~99%+  
- Minimal gap → good generalization  

---

## Training Visualization

Tracks:
- Training Accuracy  
- Validation Accuracy  

Helps detect:
- Overfitting  
- Underfitting  
- Stability  

---

## Key Learnings

- CNN learns hierarchy:
  edges → patterns → structures  
- Dropout reduces overfitting  
- Early Stopping prevents overtraining  
- Normalization + reshaping are critical  

---

## Tech Stack

- Python  
- TensorFlow / Keras  
- NumPy  
- Matplotlib  

---

## How to Run

1. Clone:
git clone https://github.com/your-username/mnist-cnn.git  
cd mnist-cnn  

2. Install:
pip install tensorflow matplotlib numpy  

3. Run:
python main.py  

---

## Future Improvements

- Visualize filters  
- Move to CIFAR-10  
- Add Batch Normalization  
- Hyperparameter tuning  
- Deploy app  

---

## Contributing

Open to contributions via issues or PRs.

---
