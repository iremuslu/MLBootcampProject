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

## Sonuç

Bu proje, gözetimli öğrenme algoritmalarının (KNN) gözetimsiz öğrenme algoritmalarına (K-Means) göre daha etkili olduğunu göstermiştir. Gözetimli öğrenme, özellikle müşteri kaybını tahmin etmek için daha uygun bir yöntem olarak değerlendirilmiştir.

## Kurulum ve Kullanım

1. **Gereksinimler:**
   - Python 3.x
   - Gerekli kütüphaneler: `pandas`, `numpy`, `scikit-learn`, `matplotlib`, `seaborn`

2. **Kurulum:**
   ```bash
   pip install -r requirements.txt
