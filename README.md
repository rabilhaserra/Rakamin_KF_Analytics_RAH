# Rakamin_KF_Analytics_RAH

# Big Data Analytics: Kimia Farma Business Performance Analysis (2020-2023)

Proyek ini bertujuan untuk menganalisis performa bisnis Kimia Farma melalui pengolahan data transaksi, produk, dan operasional cabang menggunakan **Google BigQuery** dan visualisasi data di **Looker Studio**.

## 📊 Dashboard Link
[Lihat Dashboard Interaktif di Looker Studio](https://lookerstudio.google.com/s/vn0tgsP6iL8)

---

## 🛠️ Metodologi Analisis (Framework OSEMN)

Proses analisis ini dilakukan secara sistematis menggunakan framework **OSEMN**:

### 1. Obtain
Mengunduh 4 dataset utama (Tabel Transaksi, Produk, Kantor Cabang, dan Inventori) dan mengunggahnya ke **Google BigQuery** sebagai Data Warehouse.

### 2. Scrub (Data Cleaning)
Melakukan pembersihan data untuk menjamin validitas hasil analisis. Proses ini mencakup:
* **Cek Duplikat:** Memastikan tidak ada data transaksi ganda.
* **Missing Values:** Identifikasi dan penanganan baris dengan nilai kosong (NULL).
* **Deteksi Anomali:** Validasi data yang tidak wajar seperti harga ≤ 0, diskon > 100%, dan rating di luar skala 1-5.

### 3. Explore
Tahap eksplorasi dilakukan dengan membuat **Tabel Analisa** menggunakan teknik `LEFT JOIN` untuk menggabungkan informasi dari tabel transaksi, cabang, dan produk. 

**Logika Bisnis yang Diterapkan:**
* Perhitungan **Persentase Gross Laba** dinamis (10% - 30%) berdasarkan kategori harga produk.
* Kalkulasi **Nett Sales** (Harga setelah diskon).
* Kalkulasi **Nett Profit** (Laba bersih per transaksi).

### 4. Model (Visualization)
Data dari BigQuery dihubungkan ke **Looker Studio** untuk divisualisasikan dalam bentuk dashboard interaktif. Fokus utama visualisasi meliputi:
* Tren Pendapatan & Profitabilitas bulanan/tahunan.
* Performa Cabang berdasarkan Rating.
* Analisis Top Produk dan Customers.

### 5. iNterpretation
* **Profitabilitas:** Perusahaan mencatatkan rata-rata Gross Margin sebesar **28.40%**, yang menunjukkan efisiensi pengadaan produk yang sehat.
* **Customer Insights:**: Terlihat ada customer yang loyal.
* **Strategi Cabang:** Identifikasi cabang dengan rating tinggi namun transaksi rendah sebagai bahan evaluasi operasional.

---

## 💻 Tech Stack
* **Storage & Processing:** Google BigQuery (SQL)
* **Visualization:** Looker Studio
* **Documentation:** Markdown & Pseudocode

---

## 📂 Struktur File
* `sql_queries/`: Berisi query SQL untuk cleaning data dan pembuatan tabel analisa.
* `pseudocode/`: Dokumentasi alur logika program dalam bahasa manusia.
*  Sisanya berisi syntax untuk analisa.
---

## 📧 Kontak
Dibuat oleh: [Rabiyatul Adawiyah Haserra]  
LinkedIn: [https://www.linkedin.com/in/rabil-haserra/]
