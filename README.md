# 🖼️ AI Image Classifier using CNN

A Convolutional Neural Network (CNN) built with PyTorch to classify **AI-generated** and **real** images using the CIFAKE dataset.

## 🚀 Features

- Custom CNN architecture
- Image preprocessing with torchvision
- PyTorch DataLoader pipeline
- Training and evaluation loops
- Visualize misclassified predictions
- Visualize feature maps learned by convolutional filters

## 🛠 Tech Stack

- Python
- PyTorch
- Torchvision
- Matplotlib
- Google Colab

## 📂 Dataset

- CIFAKE Dataset (Kaggle)

## 🧠 Model Architecture

Input Image (3×32×32)

↓

Conv2D (3 → 16)

↓

ReLU

↓

MaxPool

↓

Conv2D (16 → 32)

↓

ReLU

↓

MaxPool

↓

Flatten

↓

Fully Connected (2048 → 64)

↓

Output Layer (64 → 2)

## 📈 Results

- Successfully classifies AI-generated and real images.
- Includes visualization of learned feature maps.
- Displays correctly classified and misclassified examples.

## 🔮 Future Improvements

- Transfer Learning (ResNet18)
- Data Augmentation
- Batch Normalization
- Dropout
- Early Stopping