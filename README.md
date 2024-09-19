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

- **Doğru Tahmin Oranı:** Test setindeki örneklerin yaklaşık %93.81'i doğru tahmin edildi.
- **Cross-Validation Sonuçları:** Modelin doğruluğu %94'e yükseldi.
- **Churn 0 (Müşteri Kaybı Olmayan) Sınıfı:**
  - **Precision:** 0.95
  - **Recall:** 0.98
- **Churn 1 (Müşteri Kaybı Olan) Sınıfı:**
  - **Precision:** 0.83
  - **Recall:** 0.62
- **Değerlendirme:** Churn 0 sınıfı için yüksek precision ve recall değerleri elde edilmiştir. Ancak, Churn 1 sınıfı için modelin performansı daha düşük olup, bu sınıfın doğru tahmin edilme oranı zayıftır.

### K-Means Kümeleme

- **Silhouette Skoru:** 0.20
- **Değerlendirme:** Elde edilen düşük silhouette skoru, kümeler arasında belirgin bir ayrışma olmadığını ve müşterilerin kümelere düzgün bir şekilde ayrılmadığını gösterdi.

## Modellerin Değerlendirilmesi

- **Genel olarak K-means kümeleme algoritmasını incelediğimizde istediğimiz başarıya ulaşamadık. Müşterilerin kredi skorları, gelirleri ve müşteri hizmet süresi gibi özellikleri baz alarak kümelemeye çalıştık. Ancak, kümeleme sonucunda kümeler arasında çok büyük farklar görülmedi.**

- **KNN Sınıflandırma algoritmasında test setindeki örneklerin yaklaşık %93.81'ini doğru tahmin ettik. Bu modelimizin iyi bir şekilde öğrendiğini gösteriyor. Ayrıca, cross-validation ve hiperparametre optimizasyonu ile bu değer %94'e çıktı. Çok fazla bir artış olmasa da bu, daha iyi bir doğruluk (accuracy) elde etmemize sebep oldu. Fakat Churn 0 için yüksek precision (0.95) ve recall (0.98) değerleri ile bu sınıf için iyi sonuçlar alıyorken, Sınıf 1 için precision (0.83) ve recall (0.62) değerlerini alıyoruz. Bu da bu sınıf üzerinde modelin daha az başarılı olduğunu gösteriyor. Yani, bu durum bize Sınıf 1'deki örneklerin (bankadan ayrılma durumu) doğru tahmin edilme oranının düşük olduğunu gösterir.**

- **K-means Kümeleme algoritmasında ise amacımız benzer özelliklere sahip veri noktalarını bir araya getirmek ve aralarındaki farklılıkları ortaya koymaktı.**

- **Elde edilen 0.20 olan Silhouette skoru, kümelerin ayrışmasının net bir şekilde gerçekleşmediğini gösterdi. Müşteri kümeleri arasında belirgin ayrışmaların olmadığını gösterdi.**

- **Özet olarak, çalıştığım bu veri setinin gözetimli öğrenme için daha uygun olduğunu gördüm. Çünkü veri seti daha çok Churn Flag ve diğer değişkenler arasındaki ilişkiyi göstermekte güçlüydü. Diğer özelliklerin birbiri ile ilişkisi daha zayıftı. Bu da diğer özelliklerin kullanılıp modelin Churn Flag'ı tahmin etmesinde gözetimli öğrenmenin daha etkili olacağını gösteriyor.**


   ## Sonuç

Bu proje, gözetimli öğrenme algoritmalarının (KNN) gözetimsiz öğrenme algoritmalarına (K-Means) göre daha etkili olduğunu göstermiştir. Gözetimli öğrenme, özellikle müşteri kaybını tahmin etmek için daha uygun bir yöntem olarak değerlendirilmiştir.

