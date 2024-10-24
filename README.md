# FishDataProject
# General Introduction

This project was developed as part of the **Akbank Deep Learning Bootcamp** using the **A Large Scale Fish Dataset** dataset available on Kaggle. It aims to develop a fish species classification model using TensorFlow. The model uses deep learning techniques and an artificial neural network (ANN) model to classify fish images.

---

## Contents

- [PurposeOfTheProject](#purpose-of-the-project)
- [Technologies and Libraries Used](#technologies-and-libraries-used)
- [DatasetDescription](#dataset-description)
- [ModelTraining](#model-training)
- [ModelCompilation](#model-complation)
- [Results](#results)
- [KaggleNotebookLink](#kaggle-notebook-link)


---

## Purpose of the Project

The purpose of this project is to build a deep learning model capable of accurately classifying different fish species based on their images. Through this project, participants aim to gain hands-on experience in critical steps of deep learning, including data preprocessing, model development, training, and evaluation. This work focuses on:

- Developing a practical deep learning classification model using artificial neural networks (ANN).

- Enhancing skills in data preprocessing, especially dealing with image datasets.

- Implementing optimization techniques such as early stopping and learning rate adjustments to prevent overfitting and improve model performance.

- Evaluating model performance using metrics like accuracy, loss curves, and confusion matrices.

- Gaining familiarity with Kaggle as a development and deployment environment, leveraging it for collaborative coding and sharing results.

- This project not only helps participants apply theoretical concepts in real-world scenarios but also prepares them for future challenges in computer vision and deep learning domains.

---

## Technologies and Libraries Used

- Python
- TensorFlow & Keras
- Pandas
- NumPy
- Matplotlib & Seaborn
- scikit-learn (LabelEncoder, train_test_split)
- OpenCV

---

## Dataset Description

The dataset contains fish images and each image represents different species. The training set is divided into 80%, the test set is divided into 20% and the training set is further divided into 10% for the validation set.

Data preprocessing steps:

1. Only images in `.png` format are uploaded.

2. Images are resized to 28x28.

3. Normalization is performed (pixel values ​​are brought to the range of 0-1).

4. Labels are converted to numerical values ​​and processed using the One-Hot Encoding method.

---

## Model Training

The model is built using the **Dense Neural Network** architecture. Its structure is as follows:

- **Input Layer**: 28x28x3 (for RGB images)
- **Hidden Layers**: Layers with 512, 256, 128, and 64 neurons.
- **Batch Normalization** and **Dropout** are applied after each layer.
- **Output Layer**: `softmax` activation function for 9 classes.

### Model Compilation

- **Optimization**: Adam Optimizer
- **Loss Function**: Categorical Crossentropy
- **Success Measure**: Accuracy

---

## Results

The model was evaluated with accuracy rates on training and test sets:

- **Train Data**:
- Loss: `Train Loss`
- Accuracy: `Train Accuracy`

- **Test Data**:
- Loss: `Test Loss`
- Accuracy: `Test Accuracy`

- **Confusion Matrix**:
- A confusion matrix is ​​visualized showing the accuracy of the predictions on the test data.

---

## Kaggle Notebook Link
