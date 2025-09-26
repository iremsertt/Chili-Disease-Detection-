# 🌶️ Chili-Disease-Detection-
Global AI Hub bootcamp projesi
Bu proje, Global AI Hub bootcamp kapsamında gerçekleştirilmiştir. Amaç, biber bitkilerinde hastalıklı ve sağlıklı yaprakları sınıflandırmak için CNN tabanlı bir derin öğrenme modeli geliştirmektir.
Çalışma Kaggle üzerinde gerçekleştirilmiş ve hem "Temel CNN" hem de "Transfer Learning (VGG16)" modelleri karşılaştırılmıştır.

#📂 Veri Seti
- Toplam **200 görsel**:  
  - 140 eğitim (%70)  
  - 60 doğrulama (%30)  
- Sınıflar: `healthy`, `unhealthy`

##  Modeller
### 1️-Temel CNN
- 2 adet Conv2D + MaxPooling katmanı  
- Flatten + Dense(128) + Dropout  
- Çıkış katmanı: Dense(2, softmax)

### 2️-Transfer Learning (VGG16)
- Önceden eğitilmiş VGG16 (`imagenet` ağırlıkları, `include_top=False`)  
- GlobalAveragePooling2D + Dense(256) + Dropout + Dense(2, softmax)
- 
## 📊 Sonuçlar
- **Temel CNN doğruluk**: **%95.00**  
- **Transfer Learning doğruluk**: **%93.33**  
- En iyi optimizer: **Adam**

| Model              | Doğruluk | En İyi Optimizer |
|--------------------|----------|------------------|
| Temel CNN          | %95.00   | Adam (%91.67)    |
| Transfer Learning  | %93.33   | Adam (%91.67)    |

Yorum: Küçük bir veri setinde **Temel CNN**, Transfer Learning’den biraz daha iyi performans göstermiştir. Bunun nedeni, VGG16’nın daha karmaşık bir yapı olması ve küçük veri setinde aşırı uyum sağlamamasıdır.

## ⚙️ Kullanılan Kütüphaneler
- tensorflow
- keras
- numpy
- matplotlib
- seaborn
- scikit-learn

## 🔗 Linkler
-  **GitHub Repository**: [Chili Disease Detection](https://github.com/iremsertt/Chili-Disease-Detection-) 
-  **Kaggle Notebook**  : [CNN & Transfer Learning - Chili Plant Disease](https://www.kaggle.com/code/remsert/cnn-transfer-learning-chili-plant#Transfer-Learning)
-  **Dataset (Kaggle)** :  [Chili Plant Disease Dataset](https://www.kaggle.com/datasets/shuvokumarbasak4004/chili-plant-disease-detection)  



 



