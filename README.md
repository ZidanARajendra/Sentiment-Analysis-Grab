# **Sentiment Analysis for Grab Reviews**

## **Deskripsi Proyek**

Proyek ini bertujuan untuk menganalisis sentimen ulasan pelanggan terhadap aplikasi Grab yang tersedia di Google Play Store. Dengan menggunakan teknik Natural Language Processing (NLP) dan model machine learning, proyek ini berupaya mengklasifikasikan ulasan pelanggan menjadi kategori **positif** atau **negatif** secara otomatis. Hasil analisis ini dapat digunakan untuk membantu perusahaan seperti Grab memahami persepsi pelanggan terhadap layanan mereka, serta mendukung pengambilan keputusan investasi berdasarkan tren sentimen publik.

---

## **Tujuan Proyek**

1. **Analisis Sentimen Real-Time**  
   - Mengembangkan model yang dapat menganalisis sentimen dari ulasan pelanggan di Google Play Store secara otomatis dan cepat.
   - Memungkinkan investor untuk memantau tren sentimen perusahaan secara berkala, sehingga dapat mendukung pengambilan keputusan yang lebih responsif.

2. **Mengevaluasi Kelayakan Investasi**  
   - Menggunakan hasil analisis sentimen sebagai salah satu faktor dalam menilai apakah suatu perusahaan memiliki citra positif di mata pelanggan.
   - Mengidentifikasi potensi risiko berdasarkan tren sentimen negatif, seperti keluhan berulang terhadap layanan atau produk perusahaan.

3. **Menghasilkan Model yang Cepat, Akurat, dan Efisien**  
   - Mengembangkan model machine learning yang dapat mengklasifikasikan sentimen (positif/negatif) dengan akurasi tinggi.
   - Mengoptimalkan efisiensi model agar dapat berjalan dengan waktu pemrosesan yang minimal, tanpa mengorbankan performa prediksi.
   - Menggunakan teknik **BERT** untuk meningkatkan pemahaman terhadap ulasan pelanggan yang beragam.

---

## **Dataset**

Dataset yang digunakan berasal dari ulasan pengguna di Google Play Store untuk aplikasi Grab. Dataset mencakup informasi berikut:

| **Kolom**         | **Deskripsi**                                                                 |
|--------------------|-----------------------------------------------------------------------------|
| `Time`             | Tanggal ulasan ditulis.                                                       |
| `Comments`         | Isi ulasan dari pengguna.                                                     |

Dataset awalnya berisi 1557 baris data, tetapi setelah pembersihan (seperti menghapus duplikat), jumlah baris menjadi 1551.

---

## **Fitur Utama Analisis**

1. **Pembersihan Data**  
   - Menghapus karakter non-alfanumerik, stopwords, dan melakukan tokenisasi.
   - Melakukan lemmatization untuk menyederhanakan kata-kata menjadi bentuk dasarnya.
   - Koreksi ejaan menggunakan kamus SymSpell untuk memperbaiki kesalahan pengetikan.

2. **Analisis Sentimen**  
   - Menggunakan model **Hugging Face's DistilBERT** untuk mengklasifikasikan ulasan menjadi **positif**, **negatif**, atau **netral**.
   - Menyediakan distribusi sentimen dalam bentuk grafik batang dan pie chart untuk visualisasi yang lebih jelas.

3. **Insight dari Analisis**  
   - Menyediakan wawasan tentang proporsi sentimen positif dan negatif.
   - Mengidentifikasi tren sentimen negatif yang dapat menjadi indikator masalah dalam layanan.

---

## **Cara Menggunakan Program**

### **Prasyarat**
- Pastikan Anda memiliki Python versi 3.x terinstal di sistem Anda.
- Instal modul yang diperlukan dengan menjalankan perintah berikut:
  ```bash
  pip install pandas nltk textblob transformers torch scikit-learn contractions wordcloud symspellpy tensorflow vaderSentiment
  ```

### **Langkah-langkah Penggunaan**

1. **Muat Dataset**  
   Muat dataset `Data_Review_Grab.csv` ke dalam program menggunakan `pandas`:
   ```python
   df = pd.read_csv("Data_Review_Grab.csv")
   ```

2. **Jalankan Program**  
   Jalankan skrip analisis untuk membersihkan data, menganalisis sentimen, dan menghasilkan visualisasi:
   ```python
   python nama_file.py
   ```

3. **Simpan Hasil**  
   Hasil analisis dapat disimpan ke file CSV untuk referensi lebih lanjut:
   ```python
   df.to_csv('Grab_Sentiment_Analysis.csv', index=False)
   ```

---

## **Visualisasi**

1. **Distribusi Sentimen**  
   Grafik batang menunjukkan jumlah ulasan untuk setiap kategori sentimen (positif, negatif).  
   ![Bar Chart](https://via.placeholder.com/600x400?text=Bar+Chart)

2. **Proporsi Sentimen**  
   Pie chart menunjukkan persentase proporsi sentimen positif dan negatif.  
   ![Pie Chart](https://via.placeholder.com/600x400?text=Pie+Chart)

---

## **Keunggulan Program**

- **Otomatisasi**: Mengotomatiskan proses analisis sentimen untuk ribuan ulasan dalam waktu singkat.
- **Akurasi Tinggi**: Menggunakan model **DistilBERT** yang telah dilatih untuk analisis sentimen.
- **Visualisasi Interaktif**: Menggunakan library seperti `matplotlib` dan `seaborn` untuk menghasilkan grafik yang informatif dan mudah dipahami.
- **Rekomendasi Strategis**: Memberikan saran praktis berdasarkan hasil analisis untuk meningkatkan layanan dan pengambilan keputusan investasi.
---

Terima kasih telah menggunakan **Sentiment Analysis for Grab Reviews**! Kami harap proyek ini dapat membantu Anda memahami persepsi pelanggan dan mendukung pengambilan keputusan bisnis yang lebih baik. 😊
