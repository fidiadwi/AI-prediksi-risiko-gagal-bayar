Implementasi Data Analytics dan Machine Learning untuk Prediksi Risiko Gagal Bayar Pembayaran Kredit
Ringkasan
Proyek ini menganalisis data nasabah kartu kredit dan membangun model machine learning untuk memprediksi risiko gagal bayar pada bulan berikutnya.
Batasan: dataset yang digunakan adalah dataset gagal bayar kartu kredit, bukan dataset invoice. Dataset ini tidak memiliki tanggal jatuh tempo dan tanggal pembayaran invoice. Karena itu, proyek ini tidak dapat diklaim sebagai prediksi keterlambatan invoice.

Dataset
- Nama: Default of Credit Card Clients
- Sumber resmi: UCI Machine Learning Repository
- Halaman dataset: https://archive.ics.uci.edu/dataset/350/default
- ID UCI: 350
- Jumlah observasi: 30.000
- Lisensi: CC BY 4.0
- Referensi: Yeh, I.-C. (2009). Default of Credit Card Clients. UCI Machine Learning Repository. https://doi.org/10.24432/C55S3H
Notebook mengambil dataset langsung dari UCI menggunakan package ucimlrepo.

Tujuan
1. Memeriksa struktur dan kualitas data.
2. Menganalisis distribusi target dan hubungan status pembayaran dengan default.
3. Melakukan preprocessing fitur.
4. Membandingkan Logistic Regression dan Random Forest.
5. Memilih model berdasarkan F1-score pada validation set.
6. Mengevaluasi model terpilih pada test set.
7. Menyimpan model dan hasil evaluasi.

Cara menjalankan di Google Colab
1. Buka https://colab.research.google.com/
2. Pilih File → Upload notebook.
3. Unggah Prediksi_Risiko_Gagal_Bayar.ipynb.
4. Jalankan code cell dari atas ke bawah. Pastikan koneksi internet aktif saat dataset diunduh.
5. Setelah CELL 22 selesai, buka panel Files di Colab.
6. Klik kanan hasil_project.zip, lalu pilih Download.

Metode dan metrik
- Pemeriksaan data dan statistik deskriptif
- Analisis distribusi target
- Analisis tingkat default berdasarkan PAY_0
- Korelasi fitur terpilih
- Pembagian data: 60% train, 20% validation, 20% test
- One-Hot Encoding untuk fitur kategorikal
- StandardScaler untuk fitur numerik
- Logistic Regression dan Random Forest
- Accuracy, precision, recall, F1-score, ROC-AUC
- Confusion matrix dan ROC curve

Batasan dan penggunaan yang bertanggung jawab
- Model ini merupakan proyek pembelajaran, bukan sistem keputusan kredit otomatis.
- Data berasal dari konteks nasabah kartu kredit di Taiwan; performa model tidak dijamin berlaku pada populasi atau wilayah lain.
- Evaluasi pada dataset historis tidak menjamin performa pada data baru.
- Keputusan penting terhadap individu tidak boleh didasarkan hanya pada prediksi model.
