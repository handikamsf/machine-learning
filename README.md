Segmentasi Kualitas Hidup dan Aksesibilitas Digital Kabupaten/Kota di Sumatera (2024)
Repositori ini memuat source code dan analisis komparatif dari proyek segmentasi kewilayahan menggunakan algoritma K-Means dan DBSCAN. Analisis ini memetakan 154 kabupaten dan kota di Pulau Sumatera berdasarkan enam indikator makroekonomi dan infrastruktur digital dari Badan Pusat Statistik (BPS) tahun 2024.

Author: Muhammad Handika Maulana Sifa (Mahasiswa Sains Data, Semester 4)

📌 Latar Belakang
Ketimpangan kualitas hidup dan aksesibilitas digital yang persisten antarwilayah di Sumatera menuntut adanya pendekatan berbasis data (data-driven) untuk mendukung perumusan kebijakan makroekonomi yang lebih terarah. Proyek ini mengevaluasi kinerja algoritma partisional (K-Means) dan algoritma berbasis kepadatan spasial (DBSCAN) dalam melakukan segmentasi wilayah serta mendeteksi daerah dengan karakteristik anomali ekstrem.

📊 Dataset
Data yang digunakan mencakup 154 observasi dengan enam variabel prediktor:

X1: Banyaknya Desa/Kelurahan Menerima Sinyal Internet Telepon Seluler

X2: Indeks Pembangunan Manusia (IPM)

X3: PDRB Per Kapita Atas Dasar Harga Berlaku

X4: Persentase Penduduk Miskin

X5: Tingkat Pengangguran Terbuka (TPT)

X6: Rata-rata Pengeluaran per Kapita Sebulan Makanan

🛠️ Teknologi yang Digunakan
Bahasa Pemrograman: Python 3.x

Prapemrosesan & Manipulasi Data: Pandas, NumPy

Machine Learning (Clustering & PCA): Scikit-Learn (sklearn)

Visualisasi Data: Matplotlib, Seaborn

⚙️ Alur Metodologi
Prapemrosesan Data: Penanganan missing values dan normalisasi variabel menggunakan Z-Score Standardization agar penghitungan jarak spasial (Euclidean) tidak bias.

Pemodelan K-Means: Penentuan jumlah klaster optimal menggunakan Elbow Method dan Silhouette Score (menghasilkan parameter K=2).

Pemodelan DBSCAN: Penentuan radius spasial dan batas kepadatan minimum menggunakan K-Distance Graph (menghasilkan parameter Epsilon=2.1 dan MinPts=12).

Reduksi Dimensi (PCA): Mengompresi 6 dimensi variabel menjadi 2 sumbu utama (Principal Components) untuk keperluan visualisasi sebaran distribusi klaster.

Analisis Silang (Cross-Analysis): Mengekstraksi 10 daerah noise dari DBSCAN dan memprofiling ulang daerah tersebut menggunakan label biner dari K-Means untuk memecahnya menjadi "Anomali Maju" dan "Anomali Tertinggal".

🚀 Hasil dan Temuan Utama
Kinerja Algoritma: DBSCAN terbukti secara statistik lebih robust dan superior dengan Silhouette Score sebesar 0.3142 (berbanding 0.2676 milik K-Means). DBSCAN tidak memaksakan data masuk ke dalam klaster rata-rata, melainkan berhasil mengisolasi 10 daerah outlier.

Anomali Maju: Wilayah episentrum industri dan lumbung migas (seperti Kepulauan Anambas dan Kota Batam) yang mengalami ledakan PDRB ekstrem jauh di atas kewajaran daerah maju lainnya, namun mengindikasikan adanya resource curse (kutukan sumber daya alam). Membutuhkan kebijakan hilirisasi digital dan evaluasi rasio Dana Bagi Hasil (DBH).

Anomali Tertinggal: Wilayah dengan krisis fundamental (seperti Pidie dan Nias Selatan) yang mengalami degradasi aksesibilitas fisik dan telekomunikasi secara parah. Membutuhkan kebijakan afirmatif super-prioritas untuk injeksi infrastruktur dasar.
