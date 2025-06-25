# ARL-Based Service Recommendation System

This repository presents a real-world implementation of a service recommendation engine powered by Association Rule Learning (ARL). Inspired by platforms like Armut, where users frequently request categorized services (e.g., cleaning, transportation, renovation), this system is designed to surface relevant and actionable cross-sell suggestions.

## 🔍 Project Scope

The objective is to generate interpretable recommendations by leveraging user-service interaction data. Each user's monthly service usage is treated as a transaction (basket), and Apriori algorithm is applied to uncover frequent itemsets and association rules.

## 🧩 Key Features

- **Transactional Modeling**: Baskets are dynamically constructed by aggregating services on a monthly basis per user.
- **Service Representation**: Each service is encoded as a `ServiceId_CategoryId` string to ensure uniqueness.
- **Rule Extraction**: Frequent itemsets and association rules are generated with adjustable support and lift thresholds.
- **Recommendation Engine**: A modular function identifies and ranks service recommendations for any given service.

## 🗂 Project Structure

```
arl-service-recommender/
├── src/
│   └── arl_service_recommender.py  # ARL pipeline
├── requirements.txt                # Dependencies
├── README.md                       # Project overview
```

## 🚀 Getting Started

```bash
pip install -r requirements.txt
python src/arl_service_recommender.py
```

## 📤 Example Output

```
Last taken service: 2_0
Recommended services: ['3_0', '4_1', '2_2']
```

## 🔒 Data Privacy Notice

This repository is built on proprietary user-service interaction data and thus cannot share the original dataset. The implementation, however, is fully reproducible with your own transactional data.

---

# ARL Tabanlı Hizmet Öneri Sistemi

Bu proje, Armut gibi platformlardaki hizmet geçmişine dayalı olarak çalışan bir öneri motorunun Association Rule Learning (ARL) kullanılarak nasıl geliştirilebileceğini gösterir. Temizlik, nakliyat, tadilat gibi kategorize hizmetler için çapraz satış önerileri sunmayı hedefler.

## 🔍 Proje Kapsamı

Her kullanıcının hizmet alma davranışı aylık bazda bir 'sepet' olarak modellenir. Bu sepetler üzerinden Apriori algoritması ile sık çıkan hizmet kombinasyonları ve birliktelik kuralları belirlenir.

## 🧩 Temel Özellikler

- **İşlemsel Modelleme**: Kullanıcı bazında aylık sepetler oluşturulur.
- **Hizmet Kodlama**: Her hizmet `ServiceId_CategoryId` şeklinde tanımlanır.
- **Kural Çıkarımı**: Destek ve lift eşiklerine göre birliktelik kuralları üretilir.
- **Öneri Fonksiyonu**: Belirli bir hizmete karşılık gelen en anlamlı önerileri sunar.

## 🗂 Proje Yapısı

```
arl-service-recommender/
├── src/
│   └── arl_service_recommender.py  # ARL iş akışı
├── requirements.txt                # Gereksinimler
├── README.md                       # Proje özeti
```

## 🚀 Kurulum

```bash
pip install -r requirements.txt
python src/arl_service_recommender.py
```

## 📤 Örnek Çıktı

```
Son alınan hizmet: 2_0
Önerilen hizmetler: ['3_0', '4_1', '2_2']
```

## 🔒 Veri Gizliliği

Bu proje, özel kullanıcı verileri üzerine inşa edilmiştir. Veri paylaşımı yapılamamaktadır, ancak aynı yapıyı kendi verinizle tekrar edebilirsiniz.
