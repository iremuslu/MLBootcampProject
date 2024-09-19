## Proje Hakkında

Bu proje, bir banka müşteri veri seti kullanarak müşteri kaybını tahmin etmeyi amaçlamaktadır. Veri setinde müşterilerin kredi skorları, gelirleri, eğitim seviyeleri gibi çeşitli özellikler bulunmaktadır. Proje, gözetimli ve gözetimsiz öğrenme algoritmalarını kullanarak müşteri kaybını analiz etmeyi ve modellemeyi hedefler.

**Proje Linki:**
[https://www.kaggle.com/code/iremuslu1/bankcustomerchurn-ml](https://www.kaggle.com/code/iremuslu1/bankcustomerchurn-ml) 


## Amaç ve Hedef
- **Amaç:** Müşterilerin bankadan ayrılma olasılıklarını tahmin etmek ve bu tahminlere dayanarak stratejik kararlar almak.
- **Hedef:** Müşteri kaybını etkili bir şekilde tahmin edebilmek ve bankanın müşteri ilişkilerini iyileştirmek için önerilerde bulunmak.

## Kullanılan Algoritmalar

1. **K-Nearest Neighbors (KNN) Sınıflandırma:**
   - Müşterilerin bankadan ayrılma durumlarını sınıflandırmak için kullanıldı.

2. **K-Means Kümeleme:**
   - Müşterileri benzer özelliklere sahip gruplara ayırarak veri setindeki yapıların anlaşılmasına yardımcı oldu.

## Modellerin Değerlendirilmesi

### KNN Sınıflandırma

**KNN Sınıflandırma Sonuçları:**

<img src="https://github.com/user-attachments/assets/1566acc7-3c5c-44cd-9029-b5a1e4a2dc9d" width="400" />

*Bu görsel, KNN sınıflandırma algoritmasının test setindeki sonuçlarını göstermektedir.*

**KNN Hiperparametre Optimizasyonu Sonuçları:**

<img src="https://github.com/user-attachments/assets/a2b69efa-793d-42e7-92c8-99721023db95" width="400" />

*Bu görsel, hiperparametre optimizasyonu sonrası elde edilen sonuçları göstermektedir.*

### K-Means Kümeleme

**K-Means Kümeleme Sonuçları:**

<img src="https://github.com/user-attachments/assets/19e4da3e-6ac9-48f7-a05c-79fc43c3a626" width="400" />

*Bu görsel, K-Means kümeleme algoritması ile elde edilen kümeleri göstermektedir.*

**Silhouette Skoru:**

<img src="https://github.com/user-attachments/assets/7bf3ba0f-9121-427f-9659-62736ac9761b" width="400" />

*Bu görsel, kümelerin ne kadar ayrıştığını gösteren Silhouette skorunu içermektedir.*

   ## Sonuç
 **Bu proje, gözetimli öğrenme algoritmalarının (KNN) gözetimsiz öğrenme algoritmalarına (K-Means) göre daha etkili olduğunu göstermiştir. Gözetimli öğrenme, özellikle müşteri kaybını tahmin etmek için daha uygun bir yöntem olarak değerlendirilmiştir.**

