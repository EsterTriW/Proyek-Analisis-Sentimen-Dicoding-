# Proyek-Analisis-Sentimen-Dicoding-

# 💬 Sentiment Analysis of App Reviews (Traveloka)

Proyek ini bertujuan untuk melakukan **analisis sentimen** terhadap ulasan pengguna aplikasi, diklasifikasikan menjadi tiga kategori: **positif**, **negatif**, dan **netral**. Proyek ini menggunakan pendekatan **Machine Learning** dan **Deep Learning**.

---

## 📁 Fitur Utama

- **Text Preprocessing** lengkap (cleansing, normalisasi, tokenisasi, stopword removal, stemming)
- **Exploratory Data Analysis (EDA)** visual
- **3 Skema Model**:
  - SVM + TF-IDF (80/20 split)
  - Random Forest + TF-IDF (70/30 split)
  - LSTM + Tokenizer
- **Evaluation Metrics**: Accuracy, Confusion Matrix, Classification Report
- **Model Inference** untuk prediksi sentimen teks baru

---

## 📊 Dataset

Dataset berupa ulasan aplikasi yang dikategorikan dalam tiga label sentimen:
- Positif
- Negatif
- Netral

---

## 🧪 Preprocessing Teks

- Lowercasing
- Penghapusan karakter tidak relevan (`@`, `#`, `RT`, URL, angka, simbol)
- Slang normalization menggunakan kamus slang
- Tokenisasi (`nltk.word_tokenize`)
- Stopword removal (termasuk kata tidak baku seperti "yaa", "loh", "woi")
- Stemming menggunakan Sastrawi

---

## 📈 Modeling

| Skema | Model             | Ekstraksi Fitur | Split   | Train Acc | Test Acc |
|-------|------------------|------------------|---------|-----------|----------|
| 1     | SVM              | TF-IDF           | 80/20   | 0.9986    | 0.9840   |
| 2     | Random Forest    | TF-IDF           | 70/30   | 1.0000    | 0.9815   |
| 3     | LSTM (Bi-LSTM)   | Tokenizer        | Custom  | 0.9961    | 0.9831   |

---

## 🔍Keterangan File
Scrapping -> Notebook ipynb berisi scrapping mandiri dari google app store aplikasi traveloka
Pelatihan Model -> Notebook ipynb berisi load data scrapping, cleaning, text preprocessing, dan pelatihan model ML dan DL
Inference -> Notebook ipynb berisi inference/testing ulasan baru sentimen positif, negatif, netral
Traveloka_reviews -> dataset dalam csv yang digunakan
lstm_model_traveloka.h5 -> Hasil download model lstm yang digunakan dalam membangun model (untuk di load pada notebook Inference)
tokenizer_traveloka -> Hasil download tokenizer yang telah digunakan dalam model (untuk di load pada notebook Inference)
requirements.txt -> library yang digunakan
