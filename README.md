# 📌 Gelişmiş Metin Madenciliği Teknikleri ile Optimum Konu Sayısının Araştırılması

Bu proje, **Latent Dirichlet Allocation (LDA) ve BERTopic algoritmalarını kullanarak metin madenciliği ile optimum konu sayısını belirlemeyi amaçlamaktadır**. Çalışma, **bilimsel makalelerin başlık ve özetlerinden oluşan bir veri kümesi üzerinde** gerçekleştirilmiştir.

## 📖 Proje Açıklaması

- **Metin verileri işlenerek ve temizlenerek** konuların belirlenmesine uygun hale getirilmiştir.  
- **LDA ve BERTopic algoritmaları kullanılarak konu modelleme işlemi** gerçekleştirilmiştir.  
- **Karışıklık (perplexity) ve tutarlılık (coherence) metrikleri kullanılarak optimum konu sayısı belirlenmiştir.**  
- **LDA ve BERTopic sonuçları görselleştirilmiş ve karşılaştırılmıştır.**  

## 📊 Kullanılan Veri Kümesi

- **8989 satır ve 3 sütun (id, başlık, özet)** içeren veri seti kullanılmıştır.  
- ID sütunu kaldırılarak **başlık ve özet sütunları birleştirilmiştir.**  
- **Ön işleme adımları:**  
  - Noktalama işaretlerinin kaldırılması  
  - Metnin küçük harfe çevrilmesi  
  - Kelime köklerine indirgenmesi (stemming)  
  - Durdurma kelimelerinin çıkarılması  

## 🔍 Kullanılan Konu Modelleme Yöntemleri

### **1. Latent Dirichlet Allocation (LDA)**
- **Olasılıklı bir model** olup, her belgeyi bir konu karışımı ve her konuyu kelime dağılımı olarak ele alır.  
- **Optimum konu sayısını belirlemek için karışıklık ve tutarlılık skorları kullanılmıştır.**  

### **2. BERTopic**
- **Transformer tabanlı bir model olup, kelimelerin bağlamsal anlamını kullanarak konuları belirler.**  
- **Konuların daha ayrıntılı ayrıştırılmasını sağlar.**  

## 🏆 Optimum Konu Sayısı Belirleme Süreci

**Optimum konu sayısını belirlemek için şu metrikler kullanılmıştır:**  
- **Karışıklık (Perplexity):** Modelin metin verisini ne kadar iyi tahmin ettiğini gösterir.  
- **Tutarlılık (Coherence):** Konu içerisindeki kelimelerin anlamsal bağlılığını ölçer:  
  - UCI Coherence  
  - UMass Coherence  
  - CV Coherence  

**Normalizasyon Yöntemleri:**  
- Min-Max Normalizasyon  
- Ortalama Normalizasyon  
- T-Skor Normalizasyon  

Bu metrikler **lambda değerleri ile ağırlıklandırılarak birleşik skor oluşturulmuş ve optimum konu sayısı 16 olarak belirlenmiştir.**  

## 📊 Deneysel Sonuçlar

- **LDA modeli için 16 konulu dağılım en iyi sonucu vermiştir.**  
- **BERTopic, konuları daha iyi ayrıştırırken, bazı konuların örtüştüğü gözlemlenmiştir.**  
- **Her iki model için konuların mesafe haritaları ve anahtar kelimeler analiz edilmiştir.**  

Detaylı sonuçlar için **[📄 Proje Raporu](Rapor/Veri Madenciliği Rapor.pdf)** dosyasını inceleyebilirsiniz.

