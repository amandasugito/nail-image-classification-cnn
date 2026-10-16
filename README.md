# 💅 Nail Image Classification Using CNN and MobileNetV2

## 📌 Project Overview

This project explores the use of deep learning for nail image classification using Convolutional Neural Networks (CNNs). It focuses on identifying nail conditions from images and comparing different model architectures, including a baseline CNN, a modified CNN, and MobileNetV2 transfer learning.

The project also addresses class imbalance in the dataset through class weighting during model training.

## 🎯 Project Objectives

- Build a baseline CNN for nail image classification.
- Explore modifications to the CNN architecture.
- Apply transfer learning using MobileNetV2 pretrained on ImageNet.
- Identify and address class imbalance in the dataset.
- Explore model performance using training and validation data.

## 📂 Dataset

The dataset contains **2,205 nail images** across five classes:

| Class | Number of Images |
|---|---:|
| Acral Lentiginous Melanoma | 21 |
| Pitting | 629 |
| Onychogryphosis | 600 |
| Healthy Nail | 343 |
| Blue Finger | 612 |
| **Total** | **2,205** |

The dataset has a significant class imbalance, particularly in the *Acral Lentiginous Melanoma* category, which contains only 21 images.

## ⚙️ Data Preprocessing

The notebook includes the following preprocessing steps and configurations:

- Image resizing to 224 × 224 pixels.
- Image normalization using rescaling by 1/255.
- Dataset splitting into training and validation subsets using `validation_split=0.2`.
- Integer labels for multiclass classification.
- Class weight calculation to address class imbalance.

## 🧠 Model Development

Three model approaches are explored in the notebook:

### 1. 🔹 Baseline CNN

A CNN architecture consisting of convolutional layers, max-pooling layers, a fully connected layer, and an output layer for five classes.

### 2. 🔹 Modified CNN

An alternative architecture incorporating batch normalization and dropout layers to explore changes in model performance.

### 3. 🔹 MobileNetV2 Transfer Learning

A pretrained MobileNetV2 model using ImageNet weights as a feature extractor, followed by additional layers for the classification task.

## ⚖️ Class Imbalance Handling

The project identifies class imbalance as a challenge because the number of images varies substantially between categories.

The notebook calculates balanced class weights using `compute_class_weight` and applies them during baseline model training to help reduce the influence of majority classes.

## 🛠️ Tools and Technologies

- Python
- TensorFlow / Keras
- NumPy
- Matplotlib
- Scikit-learn
- Convolutional Neural Networks (CNN)
- MobileNetV2
- Transfer Learning

## 📈 Evaluation Approach

The notebook uses training and validation datasets to monitor model learning. It also contains a separate test-set evaluation section; however, the test dataset creation and the final evaluation pipeline require further verification.

Numerical performance results are therefore not reported in this README.

## 📁 Project Files

- `UTS_DeepLearning_No_3_Amanda_2702388433(1).ipynb` — notebook containing the project workflow, preprocessing, model development, and evaluation code.
- `3B.zip` — original dataset archive, if included in the repository.

## 👩‍💻 Author
**Amanda Sugito**

Deep Learning academic project at BINUS University.

## 🔗 Connect with Me
- LinkedIn: Amanda Sugito | www.linkedin.com/in/amanda-sugito
- GitHub: amandasugito | https://github.com/amandasugito
Amanda Sugito

## ⚠️ Disclaimer

This project is an academic deep learning exercise for image classification. The models are experimental and are not intended for medical diagnosis. Further validation is required before any real-world medical application.
