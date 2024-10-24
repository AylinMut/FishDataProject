# FishDataProject
# General Introduction

This project was developed as part of the **Akbank Deep Learning Bootcamp** using the **A Large Scale Fish Dataset** dataset available on Kaggle. It aims to develop a fish species classification model using TensorFlow. The model uses deep learning techniques and an artificial neural network (ANN) model to classify fish images.

---

## Contents

- [PurposeOfTheProject](#purpose-of-the-project)
- [Technologies and Libraries Used](#technologies-and-libraries-used)
- [Dataset](#dataset)
- [Model Training](#model-training)
- [Results](#results)
- [Installation](#installation)
- [Usage](#usage)
- [Visualizations](#visualizations)
- [License](#license)

---

## Purpose of the Project

The purpose of this project is to build a deep learning model capable of accurately classifying different fish species based on their images. Through this project, participants aim to gain hands-on experience in critical steps of deep learning, including data preprocessing, model development, training, and evaluation. This work focuses on:

Developing a practical deep learning classification model using artificial neural networks (ANN).
Enhancing skills in data preprocessing, especially dealing with image datasets.
Implementing optimization techniques such as early stopping and learning rate adjustments to prevent overfitting and improve model performance.
Evaluating model performance using metrics like accuracy, loss curves, and confusion matrices.
Gaining familiarity with Kaggle as a development and deployment environment, leveraging it for collaborative coding and sharing results.
This project not only helps participants apply theoretical concepts in real-world scenarios but also prepares them for future challenges in computer vision and deep learning domains.

---

## Technologies and Libraries Used

- Python
- TensorFlow & Keras
- Pandas
- NumPy
- Matplotlib & Seaborn
- scikit-learn (LabelEncoder, train_test_split)
- OpenCV (Görüntü işleme için)

---

## Dataset

The dataset contains fish images and each image represents different species. The training set is divided into 80%, the test set is divided into 20% and the training set is further divided into 10% for the validation set.

Data preprocessing steps:

1. Only images in `.png` format are uploaded.

2. Images are resized to 28x28.

3. Normalization is performed (pixel values ​​are brought to the range of 0-1).

4. Labels are converted to numerical values ​​and processed using the One-Hot Encoding method.

---

## Model Eğitimi

Model, **Dense Neural Network** mimarisi kullanılarak oluşturulmuştur. Yapısı şu şekildedir:

- **Giriş Katmanı**: 28x28x3 (RGB görüntüler için)
- **Gizli Katmanlar**: 512, 256, 128, ve 64 nöronlu katmanlar. 
  - Her katmandan sonra **Batch Normalization** ve **Dropout (0.3)** uygulanır.
- **Çıkış Katmanı**: 9 sınıf için `softmax` aktivasyon fonksiyonu.

### Model Derleme

- **Optimizasyon**: Adam Optimizer (öğrenme oranı = 0.0001)
- **Kayıp Fonksiyonu**: Categorical Crossentropy
- **Başarı Ölçütü**: Accuracy (Doğruluk)

---

## Sonuçlar

Model, eğitim ve test setleri üzerinde doğruluk oranları ile değerlendirilmiştir:

- **Eğitim Verisi**:
  - Kayıp: `Train Loss`
  - Doğruluk: `Train Accuracy`

- **Test Verisi**:
  - Kayıp: `Test Loss`
  - Doğruluk: `Test Accuracy`

### Eğitim Sonuçlarının Grafikleri

1. Eğitim ve doğrulama doğruluğu grafiği.
2. Eğitim ve doğrulama kaybı grafiği.

### Karışıklık Matrisi (Confusion Matrix)

Test verisi üzerindeki tahminlerin doğruluğunu gösteren bir karışıklık matrisi görselleştirilmiştir.

---

## Kurulum

Bu projeyi çalıştırmak için aşağıdaki adımları izleyebilirsiniz:

1. Bu projeyi klonlayın:
   ```bash
   git clone https://github.com/kullanici_adi/proje_adi.git
   cd proje_adi
