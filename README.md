# 🖼️ AI Image Classifier using CNN

<p align="center">
  <img src="screenshots/Feature maps.png" width="500">
</p>

A Convolutional Neural Network (CNN) built with PyTorch to classify **AI-generated** and **real** images using the CIFAKE dataset.

## 📦 How to Run

1. Clone this repository.
2. Open `AI_Image_Classifier_CNN.ipynb` in **Google Colab**.
3. Set the runtime to **GPU** (`Runtime → Change runtime type → T4 GPU`).
4. Download the **CIFAKE** dataset from Kaggle.
5. Place the dataset in the expected directory structure (`cifake_data/train` and `cifake_data/test`).
6. Run all notebook cells from top to bottom.

## 🚀 Features

- Custom CNN architecture built with PyTorch
- Image preprocessing using torchvision
- Efficient DataLoader pipeline
- Training and evaluation loops
- Visualization of correctly classified and misclassified images
- Feature map visualization from convolutional layers

## 🛠 Tech Stack

- Python
- PyTorch
- Torchvision
- Matplotlib
- Google Colab

## 📂 Dataset

- **Dataset:** CIFAKE (Kaggle)
- **Training Images:** 100,000
- **Test Images:** 20,000

## 🧠 Model Architecture

```text
Input (3×32×32)
      │
      ▼
Conv2D (3 → 16)
      │
ReLU
      │
MaxPool
      │
Conv2D (16 → 32)
      │
ReLU
      │
MaxPool
      │
Flatten (2048)
      │
Linear (2048 → 64)
      │
Linear (64 → 2)
```

## ⚙️ Training Configuration

- Optimizer: Adam
- Loss Function: CrossEntropyLoss
- Epochs: 5
- Batch Size: 64
- Input Size: 32×32

## 📈 Results

- **Test Accuracy:** **93.58%** on the CIFAKE test set.
- Significantly outperforms random guessing (50% baseline).
- Successfully classifies AI-generated and real images.
- Visualizes learned feature maps.
- Displays correctly classified and misclassified predictions.

## 🔍 Findings

- Early convolutional filters learned meaningful visual features such as edges and gradients.
- Some filters produced similar activation patterns, suggesting a degree of redundancy, while others specialized in detecting different image characteristics.
- At a resolution of **32×32**, many misclassified images appeared visually similar to correctly classified ones, highlighting the difficulty of distinguishing AI-generated and real images at such a low resolution.

## ⚠️ Limitations

- The model was trained only on **32×32** images.
- Performance on higher-resolution, real-world images is not guaranteed because resizing images to **32×32** removes substantial visual detail.
- The model has only been evaluated on the CIFAKE dataset and may not generalize to other image distributions.

## 🔮 Future Improvements

- Transfer Learning (ResNet18)
- Data Augmentation
- Batch Normalization
- Dropout
- Early Stopping
- Learning Rate Scheduling
