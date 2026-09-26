# Cyberbullying Detection using Naive Bayes & Text Vectorization

Sistem deteksi cyberbullying pada komentar media sosial (Instagram) menggunakan algoritma **Multinomial Naive Bayes** dengan pendekatan **Bag-of-Words (CountVectorizer)** untuk representasi teks. Project ini dibangun sebagai bagian dari skripsi (S1 Teknik Informatika).

## 📋 Deskripsi

Project ini mengklasifikasikan komentar Instagram ke dalam dua kategori:
- **Bullying**
- **Non-bullying**

Dataset dikumpulkan melalui **web scraping** komentar pada postingan akun Instagram publik figur/selebgram.

## 🗂️ Dataset

- **Jumlah data**: 650 komentar
- **Sumber**: Web scraping komentar Instagram
- **Kolom**: No, Nama Instagram, Komentar, Kategori, Tanggal Posting, Nama Akun IG Artis/Selebgram
- **Label**: Bullying / Non-bullying

## ⚙️ Metodologi

1. **Text Preprocessing**
   - Case folding (lowercase)
   - Custom stopword removal (kata kasar/slang)
   - Stopword removal menggunakan library **Sastrawi**
   - Stemming Bahasa Indonesia menggunakan **Sastrawi**
   - Visualisasi distribusi kata dengan **WordCloud**

2. **Feature Extraction**
   - Representasi teks menggunakan **CountVectorizer (Bag-of-Words)**, `max_features=5000`
   > Catatan: eksperimen awal juga mengeksplorasi pendekatan TF-IDF, namun hasil akhir model menggunakan Bag-of-Words karena performa yang lebih stabil pada dataset ini.

3. **Model**
   - **Multinomial Naive Bayes**
   - Split data: 70% training, 30% testing

## 📈 Hasil Evaluasi

| Metrik | Skor |
|---|---|
| Akurasi Training | 99,12% |
| Akurasi Testing | 83,08% |

Evaluasi tambahan menggunakan confusion matrix untuk data training dan testing.

## 🖥️ Demo Aplikasi

Project ini juga dilengkapi implementasi sederhana menggunakan **Flask** untuk menguji prediksi model secara interaktif melalui web interface.

## 🛠️ Tech Stack

- Python
- Pandas, NumPy
- Scikit-learn (Naive Bayes, CountVectorizer)
- Sastrawi (NLP Bahasa Indonesia)
- Matplotlib, Seaborn, WordCloud
- Flask

## 🚀 Cara Menjalankan

1. Clone repository ini
2. Install dependencies:

## 👤 Author

**Muhammad Farkhan Imfrozin Ferbrian Putra**
📧 imfrozin2000@gmail.com
