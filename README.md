# MLBootcampProject

# Proje Adı

## Proje Hakkında

Bu proje, bir banka müşteri veri seti kullanarak müşteri kaybını tahmin etmeyi amaçlamaktadır. Veri setinde müşterilerin kredi skorları, gelirleri, eğitim seviyeleri gibi çeşitli özellikler bulunmaktadır. Proje, gözetimli ve gözetimsiz öğrenme algoritmalarını kullanarak müşteri kaybını analiz etmeyi ve modellemeyi hedefler.

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

Aşağıda KNN Sınıflandırma algoritmasının sonuçlarını ve hiperparametre optimizasyonunu gösteren görseller bulunmaktadır.

1. **KNN Sınıflandırma Sonuçları:**
   <img src="https://github.com/user-attachments/assets/1566acc7-3c5c-44cd-9029-b5a1e4a2dc9d" alt="KNN Class Rep" width="400"/>
   Bu görsel, KNN sınıflandırma algoritmasının test setindeki sonuçlarını göstermektedir.

2. **KNN Hiperparametre Optimizasyonu Sonuçları:**
   <img src="https://github.com/user-attachments/assets/a2b69efa-793d-42e7-92c8-99721023db95" alt="KNN Class Rep Opt" width="400"/>
   Bu görsel, hiperparametre optimizasyonu sonrası elde edilen sonuçları göstermektedir.

### K-Means Kümeleme

Aşağıda K-Means kümeleme algoritmasının sonuçlarını ve Silhouette skorunu gösteren görseller bulunmaktadır.

1. **K-Means Kümeleme Sonuçları:**
   <img src="https://github.com/user-attachments/assets/19e4da3e-6ac9-48f7-a05c-79fc43c3a626" alt="KMeans Clustering" width="400"/>
   Bu görsel, K-Means kümeleme algoritması ile elde edilen kümeleri göstermektedir.

2. **Silhouette Skoru:**
   <img src="https://github.com/user-attachments/assets/7bf3ba0f-9121-427f-9659-62736ac9761b" alt="Silhouette Score" width="400"/>
   Bu görsel, kümelerin ne kadar ayrıştığını gösteren Silhouette skorunu içermektedir.


## Modellerin Değerlendirilmesi

- **Genel olarak K-means kümeleme algoritmasını incelediğimizde istediğimiz başarıya ulaşamadık. Müşterilerin kredi skorları, gelirleri ve müşteri hizmet süresi gibi özellikleri baz alarak kümelemeye çalıştık. Ancak, kümeleme sonucunda kümeler arasında çok büyük farklar görülmedi.**

- **KNN Sınıflandırma algoritmasında test setindeki örneklerin yaklaşık %93.81'ini doğru tahmin ettik. Bu modelimizin iyi bir şekilde öğrendiğini gösteriyor. Ayrıca, cross-validation ve hiperparametre optimizasyonu ile bu değer %94'e çıktı. Çok fazla bir artış olmasa da bu, daha iyi bir doğruluk (accuracy) elde etmemize sebep oldu. Fakat Churn 0 için yüksek precision (0.95) ve recall (0.98) değerleri ile bu sınıf için iyi sonuçlar alıyorken, Sınıf 1 için precision (0.83) ve recall (0.62) değerlerini alıyoruz. Bu da bu sınıf üzerinde modelin daha az başarılı olduğunu gösteriyor. Yani, bu durum bize Sınıf 1'deki örneklerin (bankadan ayrılma durumu) doğru tahmin edilme oranının düşük olduğunu gösterir.**

- **K-means Kümeleme algoritmasında ise amacımız benzer özelliklere sahip veri noktalarını bir araya getirmek ve aralarındaki farklılıkları ortaya koymaktı.**

- **Elde edilen 0.20 olan Silhouette skoru, kümelerin ayrışmasının net bir şekilde gerçekleşmediğini gösterdi. Müşteri kümeleri arasında belirgin ayrışmaların olmadığını gösterdi.**

- **Özet olarak, çalıştığım bu veri setinin gözetimli öğrenme için daha uygun olduğunu gördüm. Çünkü veri seti daha çok Churn Flag ve diğer değişkenler arasındaki ilişkiyi göstermekte güçlüydü. Diğer özelliklerin birbiri ile ilişkisi daha zayıftı. Bu da diğer özelliklerin kullanılıp modelin Churn Flag'ı tahmin etmesinde gözetimli öğrenmenin daha etkili olacağını gösteriyor.**


   ## Sonuç

Bu proje, gözetimli öğrenme algoritmalarının (KNN) gözetimsiz öğrenme algoritmalarına (K-Means) göre daha etkili olduğunu göstermiştir. Gözetimli öğrenme, özellikle müşteri kaybını tahmin etmek için daha uygun bir yöntem olarak değerlendirilmiştir.

