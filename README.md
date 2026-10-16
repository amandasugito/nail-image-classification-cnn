# 💅 Nail Image Classification Using CNN and MobileNetV2

## 📌 Project Overview

This project explores deep learning for nail image classification using Convolutional Neural Networks (CNNs). It explores three model approaches: a baseline CNN, a modified CNN, and MobileNetV2 transfer learning.

The project also investigates class imbalance and uses class weighting during baseline model training.

## 🎯 Project Objectives

- Build a baseline CNN for nail image classification.
- Explore modifications to the CNN architecture.
- Apply transfer learning using MobileNetV2 pretrained on ImageNet.
- Identify and address class imbalance in the dataset.
- Monitor model performance using training and validation data.

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

The original dataset is provided in `3B.zip`. Due to its file size and distribution considerations, it is not included in this repository.

## ⚙️ Data Preprocessing

The notebook includes the following preprocessing steps and configurations:

- Image resizing to 224 × 224 pixels.
- Image normalization using rescaling by 1/255.
- Splitting the dataset into training and validation subsets using `validation_split=0.2`.
- Integer labels for multiclass classification.
- Calculating class weights to address class imbalance.

## 🧠 Model Development

### 1. 🔹 Baseline CNN

A convolutional neural network consisting of convolutional layers, max-pooling layers, a fully connected layer, and an output layer for five classes.

### 2. 🔹 Modified CNN

An alternative CNN architecture incorporating batch normalization and dropout layers to explore their effects on model performance.

### 3. 🔹 MobileNetV2 Transfer Learning

A pretrained MobileNetV2 model using ImageNet weights as a feature extractor, followed by additional layers for the classification task.

## ⚖️ Class Imbalance Handling

The dataset has a substantial class imbalance, particularly in the *Acral Lentiginous Melanoma* category, which contains only 21 images.

The notebook calculates balanced class weights using `compute_class_weight` and applies them during baseline model training to help reduce the influence of majority classes.

## 📊 Evaluation Approach

The notebook uses training and validation datasets to monitor model learning.

It also contains a separate test-set evaluation section. However, the test dataset creation and final evaluation pipeline require further verification. Therefore, numerical performance results are not reported in this README.

## 🛠️ Tools and Technologies

- Python
- TensorFlow / Keras
- NumPy
- Matplotlib
- Scikit-learn
- Convolutional Neural Networks (CNN)
- MobileNetV2
- Transfer Learning

## 🚀 How to Run

1. Clone or download this repository.
2. Open `UTS_DeepLearning_No_3_Amanda_2702388433(1).ipynb` in Google Colab or Jupyter Notebook.
3. Obtain the original `3B.zip` dataset from the source provided for the academic assignment.
4. Extract the dataset and update the `data_dir` variable in the notebook to match the extracted dataset directory.
5. Install the required Python libraries if they are not already available:
   - TensorFlow
   - NumPy
   - Matplotlib
   - Scikit-learn
6. Run the notebook cells sequentially to perform image preprocessing, calculate class weights, train the models, and review the results.

**Note:** Parts of the model architecture and evaluation pipeline may require adjustment before the experiments can be reproduced end to end.

## 📁 Project Files

- `Nail Image Classification.ipynb` — Notebook containing preprocessing, model development, training, and evaluation code.
- `3B.zip` — Original dataset archive, not included in this repository.

## 👩‍💻 Author

**Amanda Sugito**

Deep Learning academic project at BINUS University.

## 🔗 Connect with Me

- LinkedIn: Amanda Sugito | www.linkedin.com/in/amanda-sugito
- GitHub: amandasugito | https://github.com/amandasugito

## ⚠️ Disclaimer

This project is an academic deep learning exercise for image classification. The models are experimental and are not intended for medical diagnosis. Further validation is required before any real-world medical application.
