# ✈️ FlyGaruda Sentiment Analysis

Analisis sentimen terhadap ulasan publik mengenai aplikasi **Garuda Indonesia** menggunakan pendekatan berbasis teks bahasa Indonesia.  
Proyek ini terdiri atas beberapa tahap — mulai dari *data scraping*, *cleaning*, *exploratory data analysis (EDA)* hingga *feature engineering* menggunakan *Bag of Words (BoW)*

---

## 📂 Repository Structure

```bash
├── data/
│   ├── cleaned_garuda_reviews.csv         # Hasil akhir data yang sudah dibersihkan
│   ├── colloquial-indonesian-lexicon.csv  # Korpus slang-to-formal untuk normalisasi teks
│   ├── flygaruda_reviews_clean_label.csv  # Dataset akhir dengan label sentimen
│   ├── garuda_reviews.csv                 # Data mentah hasil scraping
│   ├── regex_garuda_reviews.csv           # Data hasil tahap regex cleaning
│
├── notebook/
│   ├── flygaruda_data_scrapping.ipynb     # Tahap pengambilan data dari portal berita
│   ├── flygaruda_regex.ipynb              # Regex cleaning & normalisasi teks
│   ├── flygaruda_preprocess.ipynb         # Pembersihan lanjutan: stopword, slang, dan leksikon
│   ├── flygaruda_eda.ipynb                # Analisis eksploratori dan klasifikasi sentimen
│   ├── flygaruda_bow.ipynb                # Feature engineering menggunakan Bag of Words
│
├── .gitignore
├── README.md
```
---

## 🧭 Project Overview

**🎯 Tujuan:**  
Membangun *pipeline* analisis sentimen terhadap ulasan publik (berita & komentar) mengenai aplikasi **Garuda Indonesia**.

**📈 Cakupan Tahapan:**

### 1. Scraping Data  
- Mengambil data dari Google Play Store, spesifiknya reviews aplikasi FlyGaruda .  

### 2. Cleaning & Preprocessing  
- Pembersihan karakter, emoji, dan angka menggunakan *regex*.  
- Normalisasi kata tidak baku (slang → formal) menggunakan *colloquial lexicon*.  
- Penghapusan stopword Bahasa Indonesia.  
- Stemming & tokenisasi menggunakan `Sastrawi`

### 3. Exploratory Data Analysis (EDA) + Sentiment Analysis  
- Analisis distribusi label sentimen (positif, negatif, netral).  
- *Word frequency*, *wordcloud*, dan *co-occurrence* kata.  
- *Sentiment scoring* menggunakan *rule-based* dan model pembelajaran mesin.  

### 4. Feature Engineering  
- Representasi teks dengan **Bag of Words (BoW)**
- Eksperimen *n-gram* (unigram & bigram).  

---

## 🧩 Tools & Libraries

| Kategori | Tools/Libraries |
|-----------|----------------|
| Scraping | `requests`, `BeautifulSoup`, `newspaper3k`, `google-news` |
| Cleaning | `regex`, `pandas`, `Sastrawi`, `nltk`, `IndoNLP` |
| EDA & Sentiment | `matplotlib`, `seaborn`, `wordcloud`, `plotly`, `textblob`, `scikit-learn` |
| Feature Engineering | `CountVectorizer`, `scikit-learn` |

---
