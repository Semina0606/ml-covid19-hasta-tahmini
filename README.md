
# COVID-19 Hasta Semptom Analizi ve Teşhis Tahmini

Bu proje, makine öğrenmesi algoritmalarını kullanarak hastaların klinik belirtilerine dayalı olarak COVID-19 test sonuçlarını tahmin etmeyi amaçlayan bir veri bilimi çalışmasıdır.

## Proje Hakkında
Projede, güncel bir hasta semptom veri seti kullanılmıştır. Hastaların yaşı, cinsiyeti, ateş ve öksürük şiddeti gibi temel klinik verileri incelenerek "Covid Pozitif" veya "Negatif" durumları analiz edilmiştir.
* **Veri Kaynağı:** [COVID-19 Patient Symptoms Dataset](https://www.kaggle.com/datasets/shraddha0911/covid19-patient-symptoms-and-diagnosis-dataset)

## Veri Ön İşleme (EDA) Süreci
- Veri setindeki boş değerler temizlenmiş ve veri bütünlüğü sağlanmıştır.
- Kategorik değişkenler (Cinsiyet, Öksürük Durumu vb.) makine öğrenmesi modelleri için sayısal formatlara dönüştürülmüştür.
- Veri seti, %79 eğitim ve %21 test olacak şekilde randomize edilerek ayrılmıştır.

## Model Performans Metrikleri
Aşağıda 4 farklı modelin test verileri üzerinden elde edilen detaylı başarı metrikleri yer almaktadır:

Algoritma,Kesinlik (Precision),Duyarlılık (Recall),F1 Puanı,Doğruluk (Accuracy)
Lojistik Regresyon,% 82,% 85,% 83,% 81
Karar Ağacı,% 74,% 72,% 73,% 75
Rastgele Orman,% 89,% 86,% 87,% 88
KNN Algoritması,% 79,% 81,% 80,% 78

## Genel Değerlendirme
Analiz sonuçlarına göre [EN YÜKSEK MODELİ YAZ] algoritması en tutarlı sonuçları vermiştir. Proje, semptom tabanlı ön teşhis süreçlerinde makine öğrenmesinin potansiyelini göstermektedir.

## Kodların Çalıştırılması
1. Depodaki `.ipynb` dosyasını indirin.
2. Gerekli kütüphaneleri (pandas, scikit-learn, seaborn) yükleyin.
3. Google Colab veya Jupyter üzerinden tüm hücreleri çalıştırın.
