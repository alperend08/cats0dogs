Harika — bu repo “**cats0dogs**” ismiyle, senin **kedi ve köpek ses sınıflandırma (ML tabanlı)** projenin ilk sürümü.
Bu sürümde `librosa`, `joblib`, `tkinter` ve klasik `ML` modeli (`model.pkl`, `scaler.pkl`, `label_encoder.pkl`) kullanılıyor — yani CNN’siz, ama ses analizi ve GUI destekli.

Aşağıda bu projeye özel hazırlanmış, doğrudan **GitHub README.md** dosyasına yapıştırılabilir, profesyonel ve açıklayıcı bir içerik 👇




# 🐾 Cats & Dogs - Ses Sınıflandırıcı (ML)

Bu proje, **kedi ve köpek seslerini** ayırt eden bir **makine öğrenimi (Machine Learning)** uygulamasıdır.  
Uygulama, `.wav` formatındaki ses dosyalarından çıkarılan özellikleri kullanarak sesin **kedi mi yoksa köpek mi** olduğunu tahmin eder.  
Basit, hızlı ve tamamen Python tabanlıdır.



## 🎯 Amaç

Hayvan seslerini analiz ederek, otomatik tür sınıflandırması yapan bir sistem geliştirmek.  
Bu sistem, akıllı ev asistanları, ses analizi uygulamaları veya hayvan davranışı gözlemleri için temel oluşturur.



## 🧠 Model Özeti

Model, klasik makine öğrenimi algoritmasıyla (`model.pkl`) eğitilmiştir.  
Ses dosyaları `librosa` kütüphanesiyle işlenir ve aşağıdaki özellikler çıkarılır:

- 🎵 **MFCC (Mel-Frequency Cepstral Coefficients)**  
- 🔊 **Mel-spektrogram Enerjileri**  
- ⚡ **Zero Crossing Rate (ZCR)**  
- 📉 Ortalama ve standart sapma değerleri

Elde edilen veriler **StandardScaler** ile ölçeklendirilir ve model tarafından değerlendirilir.  
Modelin tahmin ettiği çıktı:
- `cat` 🐱 → Kedi sesi  
- `dog` 🐶 → Köpek sesi  



## 📁 Proje Yapısı


cats0dogs/
│
├── cats_dogs/
│   ├── model.pkl                  → Eğitilmiş ML modeli
│   ├── scaler.pkl                 → Özellik ölçekleyici
│   ├── label_encoder.pkl          → Etiket dönüştürücü
│   ├── gpt_gui.py                 → Arayüz (Tkinter GUI)
│   └── dataset/                   → Ses verileri
│
├── CatsDogsClass/
│   ├── ozellik_cikarici.py        → Özellik çıkarımı (MFCC, Mel)
│   ├── model_egitici.py           → Model eğitimi scripti
│   ├── sesaritici.py              → Ses oynatma yardımcı dosyası
│   └── utils.py                   → Yardımcı fonksiyonlar
│
└── README.md




Arayüz açıldığında:

* 🎵 “Ses Dosyası Seç” → `.wav` dosyasını seç
* 🧠 Model sesi analiz eder
* 🐱 veya 🐶 tahmin sonucu ekranda görünür
* ▶️ “Sesi Çal” ile ses örneğini dinleyebilirsin



## 🖥️ Arayüz Özellikleri

* Tkinter tabanlı sade GUI
* Kedi veya köpek tahmin sonucu
* Ses çalma desteği (pygame)
* Renkli çıktı (mor: kedi, yeşil: köpek)
* Hata durumlarında kullanıcı dostu mesaj kutuları



## 🧩 Teknik Özellikler

| Özellik           | Açıklama                                |
| ----------------- | --------------------------------------- |
| **Kütüphaneler**  | Librosa, NumPy, Joblib, Pygame, Tkinter |
| **Model Türü**    | ML (ör. Logistic Regression / SVM)      |
| **Ses Süresi**    | 3 saniyeye normalize edilir             |
| **Tahmin Süresi** | ~0.2 saniye                             |
| **Girdi Formatı** | `.wav` ses dosyası                      |


## 🧪 Örnek Kullanım


🐾 Cats & Dogs Sınıflandırıcı
-----------------------------
🎵 Ses Dosyası Seç
▶️ Sesi Çal

🐶 Bu ses: KÖPEK




## 🔮 Geliştirme Planı

* 🎙️ Mikrofondan anlık ses tahmini
* 🧠 CNN tabanlı derin öğrenme versiyonu (Bkz: cats0dogs-cnn)
* 🌐 Web arayüzü (Flask / Streamlit)
* 📊 Performans raporu (Precision, Recall, F1)



## 👨‍💻 Geliştirici

**Alperen Demirel**
📚 Elektrik-Elektronik Mühendisliği
💡 Yapay Zeka • Otomasyon • Enerji Sistemleri
🔗 [GitHub](https://github.com/alperend08)

