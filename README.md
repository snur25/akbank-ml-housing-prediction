# California Housing Fiyat Tahmin Projesi

**Akbank Makine Öğrenmesi Bootcamp: Yeni Nesil Proje Kampı**

Bu proje, California'daki ev fiyatlarını makine öğrenmesi algoritmalarıyla tahmin etmeyi amaçlayan supervised learning çalışmasıdır.

## Proje Hakkında

### Veri Seti
- **Kaynak**: Scikit-learn California Housing Dataset
- **Boyut**: 20,640 ev verisi
- **Özellikler**: 8 bağımsız feature (MedInc, HouseAge, AveRooms, AveBedrms, Population, AveOccup, Latitude, Longitude)
- **Hedef**: Median house value (ev fiyatı tahminı)
- **Veri Tipi**: Tamamı sayılardan oluşuyor, eksik değer yok

### Kullanılan Teknolojiler
- **Python**: Ana programlama dili
- **Pandas & NumPy**: Veri manipülasyonu ve analizi
- **Matplotlib & Seaborn**: Veri görselleştirme
- **Scikit-learn**: Makine öğrenmesi algoritmaları
- **Jupyter Notebook**: Geliştirme ortamı

## Çözülen Problem

**Problem Tanımı**: California'daki farklı bölgelerde bulunan evlerin fiyatlarını, demografik ve coğrafi özelliklerine dayanarak tahmin etmek.

**Çözüm Yaklaşımı**: 
- Keşifsel Veri Analizi (Exploratory Data Analysis (EDA)) ile veri desenlerini keşfetme
- Feature scaling ile veri standardizasyonu
- Multiple algoritma karşılaştırması
- En iyi modeli seçerek hiperparametre optimizasyonu

## Kullanılan Algoritmalar

### 1. Linear Regression (Baseline Model)
- **Performans**: %57.6 R² skoru
- **Avantajlar**: Basit, hızlı, yorumlanabilir
- **Dezavantajlar**: Non-linear ilişkileri yakalayamıyor

### 2. Random Forest Regressor (Seçilen Model) 
- **Performans**: %80.5 R² skoru
- **Avantajlar**: 
  - Ensemble learning gücü
  - Non-linear pattern recognition
  - Overfitting'e dayanıklı
- **Hiperparametreler**: n_estimators=100, random_state=42

## Proje Sonuçları

### Model Performans Metrikleri
- **Test R² Skoru**: 0.8053 (%80.5 başarı oranı)
- **Test MSE**: 0.2552
- **Test MAE**: $32,743 (ortalama mutlak hata)
- **Cross Validation**: 5-fold CV ile model stabilitesi onaylandı

### Önemli Bulgular
1. **En Etkili Faktör**: MedInc (Median Income) (%52.5 feature importance)
2. **Konum Faktörü**: Latitude/Longitude kritik rol oynuyor
3. **Model Seçimi**: Ensemble methodu linear modelden %22.9 daha başarılı
4. **Preprocessing**: Feature scaling performansı önemli ölçüde artırdı

## Gerçek Hayat Uygulamaları

### 1. Emlak Sektörü
- **Otomatik Değerleme**: Emlak şirketleri için hızlı fiyat tahmini
- **Piyasa Analizi**: Ev sahipleri için bölgesel fiyat trendlerinin takibi

### 2. Finansal Hizmetler
- **Kredi Risk Değerlendirmesi**: Kredi başvurularında teminat değerleme
- **Sigorta**: Emlak sigortası prim hesaplamaları

### 3. Kamu Politikaları
- **Şehir Planlama**: Konut politikalarının etki analizi
- **Vergi Değerlendirmesi**: Emlak vergisi matrah hesaplamaları
- **Sosyal Politika**: Konut erişilebilirliği analizi

## Gelecek Geliştirmeler

### Teknik İyileştirmeler
1. **Gelişmiş Algoritmalar**
   - Neural Networks (Deep Learning) uygulaması
   - Ensemble voting ve stacking teknikleri

2. **Feature Engineering**
   - Okul kalitesi indeksi eklenmesi
   - Suç oranı ve güvenlik metrikleri
   - Ulaşım erişilebilirlik skorları
   - Ekonomik göstergeler (işsizlik, enflasyon)
   - Haber sentiment analizi ile piyasa psikolojisi skorları
   - Medya trend analizi ve emlak sektörü haber etkisi
   - Evlerin vergi yüzdeleri

### Yayınlama
1. **Web Uygulaması**
2. **API Geliştirme**
3. **Cloud Deployment**
4. **Mobil Uygulama**


## Metodoloji ve Teknik Detaylar

### Veri Ön İşleme
- StandardScaler ile Z-score normalizasyonu
- Train-test split (%80-%20)
- Cross-validation ile model validation

### Model Değerlendirme
- MSE, MAE, R² metrikleri
- Residual analysis ile model diagnostics

### Kod Kalitesi
- Comprehensive documentation
- Reproducible results (random_state)
- Modular code structure

## Öğrenilen Teknolojiler

### Makine Öğrenmesi
- Supervised Learning prensipleri
- Ensemble Learning (Random Forest)
- Cross-validation teknikleri
- Feature selection ve importance

### Veri Bilimi
- Keşifsel Veri Analizi (Exploratory Data Analysis (EDA))
- İstatistiksel analiz ve korelasyon
- Data visualization
- Model interpretation teknikleri

### Yazılım Geliştirme
- Python
- Jupyter Notebook
- Git ve Github
- Doküman yazma

### Kaggle Linki

https://www.kaggle.com/code/nisanur1/california-housing-price-prediction

## Sonuç ve Değerlendirme

Bu proje, gerçek dünya veri seti kullanarak machine learning ile geliştirme deneyimi sağladı.

#Ana Başarılar:

- Veri Analizi Uzmanlığı: Kapsamlı EDA ile gizli veri desenleri ortaya çıkarıldı.

- Algoritma Yetkinliği: Ensemble learning kullanılarak %22.9 oranında performans artışı elde edildi.

- Model Yorumlanabilirliği: Özellik önem analizi sayesinde iş değerine dönüştürülebilecek içgörüler sağlandı.

- Üretime Hazır Yapı: Çapraz doğrulama ile modelin güvenilirliği ve genellenebilirliği test edildi.

- Ölçeklenebilir Mimari: Modüler ve sürdürülebilir kod yapısı ile uzun vadeli kullanım için uygun bir çözüm geliştirildi.

**Gelecek Vizyonu**: Bu proje, kapsamlı bir emlak analiz platformunun temelini oluşturmakta olup; sürekli öğrenme ve geliştirme ile, emlak sektöründe yapay zekâ destekli karar verme süreçlerine değerli katkılar sağlayacaktır.
