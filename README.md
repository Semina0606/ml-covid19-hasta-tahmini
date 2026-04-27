
# COVID-19 Hasta Semptom Analizi ve Teşhis Tahmini

Bu proje, makine öğrenmesi algoritmalarını kullanarak hastaların klinik belirtilerine dayalı olarak COVID-19 test sonuçlarını tahmin etmeyi amaçlayan bir veri bilimi çalışmasıdır.

## Proje Hakkında
Projede, güncel bir hasta semptom veri seti kullanılmıştır. Hastaların yaşı, cinsiyeti, ateş ve öksürük şiddeti gibi temel klinik verileri incelenerek "Covid Pozitif" veya "Negatif" durumları analiz edilmiştir.
* **Veri Kaynağı:** [COVID-19 Patient Symptoms Dataset](https://www.kaggle.com/datasets/shraddha0911/covid19-patient-symptoms-and-diagnosis-dataset)

## Veri Seti Tanıtımı
Bu projede, hastaların temel klinik belirtilerini içeren bir COVID-19 semptom veri seti kullanılmıştır. Veri seti toplamda 6 sütundan oluşmaktadır:
Bağımsız Değişkenler (Öznitelikler):
Age (Yaş): Hastanın yaşı.
Gender (Cinsiyet): Hastanın cinsiyeti (Erkek/Kadın).
Fever (Ateş): Hastanın vücut ısısı ölçümü.
Cough (Öksürük): Öksürük şiddeti (Şiddetli/Hafif).
Hedef Değişken (Etiket):
Has_Covid: Hastanın COVID-19 testi sonucunun pozitif (Yes) veya negatif (No) olma durumu.


## Veri Ön İşleme (EDA) Süreci
- Veri setindeki boş değerler temizlenmiş ve veri bütünlüğü sağlanmıştır.
- Kategorik değişkenler (Cinsiyet, Öksürük Durumu vb.) makine öğrenmesi modelleri için sayısal formatlara dönüştürülmüştür.
- Veri seti, %79 eğitim ve %21 test olacak şekilde randomize edilerek ayrılmıştır.

## Kullanılan Algoritmalar ve Mantığı
Projede sınıflandırma problemi için yaygın olarak kullanılan 4 farklı makine öğrenmesi algoritması test edilmiştir:

Lojistik Regresyon (Logistic Regression): Doğrusal bir modeldir. Hastanın ateş, yaş, cinsiyet gibi değerlerini matematiksel bir denklemde ağırlıklandırarak sonucun "Covid" veya "Covid Değil" olma olasılığını (0 ile 1 arasında) hesaplar.

Karar Ağacı (Decision Tree): Veri setine sorular sorarak ilerler. Örneğin; "Ateş 100'den yüksek mi?", "Evet ise, öksürük şiddetli mi?" şeklinde dallanarak veriyi en iyi bölen kuralları bulmaya ve bir karara varmaya çalışır.

Rastgele Orman (Random Forest): Tek bir karar ağacının ezberleme (overfitting) yapmasını önlemek için geliştirilmiş "Kolektif Akıl" (Ensemble) yöntemidir. Birden fazla farklı karar ağacı oluşturur ve sınıflandırma için ağaçlar arasında oylama yapar.

K-En Yakın Komşu (KNN - K-Nearest Neighbors): Yeni gelen bir hastanın verilerini uzaysal bir düzleme yerleştirir ve ona özellik olarak "en yakın" olan 'K' sayıdaki hastaya bakar. Komşuları genelde COVID pozitifse, yeni hastanın da pozitif olduğunu tahmin eder.


## Model Performans Metrikleri
Aşağıda 4 farklı modelin test verileri üzerinden elde edilen detaylı başarı metrikleri yer almaktadır:

### Model Performans Metrikleri

Aşağıda 4 farklı modelin test verileri üzerinden elde edilen detaylı başarı metrikleri yer almaktadır:

| Algoritma | Accuracy | Precision | Recall | F1-Score |
| :--- | :--- | :--- | :--- | :--- |
| Lojistik Regresyon | % 81 | % 82 | % 85 | % 83 |
| Karar Ağacı | % 75 | % 74 | % 72 | % 73 |
| Rastgele Orman | % 88 | % 89 | % 86 | % 87 |
| KNN Algoritması | % 78 | % 79 | % 81 | % 80 |

## Genel Değerlendirme
Analiz sonuçlarına göre [EN YÜKSEK MODELİ YAZ] algoritması en tutarlı sonuçları vermiştir. Proje, semptom tabanlı ön teşhis süreçlerinde makine öğrenmesinin potansiyelini göstermektedir.

## Kodların Çalıştırılması
1. Depodaki `.ipynb` dosyasını indirin.
2. Gerekli kütüphaneleri (pandas, scikit-learn, seaborn) yükleyin.
3. Google Colab veya Jupyter üzerinden tüm hücreleri çalıştırın.
