# FishDataProject
# Balık Görüntü Sınıflandırma Modeli

Bu proje, TensorFlow kullanarak bir balık türü sınıflandırma modeli geliştirmeyi amaçlar. Projede, Kaggle üzerindeki **A Large Scale Fish Dataset** veri kümesi kullanılmıştır. Model, balık görüntülerini sınıflandırmak için derin öğrenme teknikleri ve tam bağlantılı yapay sinir ağlarını (Dense Neural Networks) kullanır.

---

## İçindekiler

- [Proje Hakkında](#proje-hakkında)
- [Kullanılan Teknolojiler ve Kütüphaneler](#kullanılan-teknolojiler-ve-kütüphaneler)
- [Veri Kümesi](#veri-kümesi)
- [Model Eğitimi](#model-eğitimi)
- [Sonuçlar](#sonuçlar)
- [Kurulum](#kurulum)
- [Kullanım](#kullanım)
- [Görselleştirmeler](#görselleştirmeler)
- [Lisans](#lisans)

---

## Proje Hakkında

Bu proje, Kaggle üzerinde bulunan **balık görüntü veri kümesini** kullanarak her bir balık türünü doğru şekilde sınıflandırmayı hedefler. Veriler işlendikten sonra, sinir ağı modeli eğitilmiş ve sonuçları değerlendirilmiştir. Eğitim süreci boyunca erken durdurma (early stopping) ve öğrenme hızının azaltılması (ReduceLROnPlateau) gibi yöntemler kullanılmıştır.

---

## Kullanılan Teknolojiler ve Kütüphaneler

- Python
- TensorFlow & Keras
- Pandas
- NumPy
- Matplotlib & Seaborn
- scikit-learn (LabelEncoder, train_test_split)
- OpenCV (Görüntü işleme için)

---

## Veri Kümesi

Veri kümesi, balık görüntülerini içerir ve her görüntü farklı türleri temsil eder. Eğitim seti %80, test seti %20 olarak ayrılmış ve eğitim seti ayrıca %10 oranında doğrulama seti için bölünmüştür.

Veri ön işleme adımları:

1. Yalnızca `.png` formatındaki görüntüler yüklenir.
2. Görüntüler 28x28 boyutuna yeniden boyutlandırılır.
3. Normalizasyon yapılır (0-1 aralığına getirilen piksel değerleri).
4. Etiketler, sayısal değerlere dönüştürülür ve One-Hot Encoding yöntemiyle işlenir.

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
