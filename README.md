# Proyek Akhir Analisis Big Data

## Pendahuluan
### Pernyataan Masalah
Dalam dunia perhotelan, memahami pola reservasi pelanggan dan faktor yang memengaruhi pembatalan reservasi adalah hal yang sangat penting. Tingkat pembatalan yang tinggi dapat memengaruhi pendapatan dan operasional hotel. Oleh karena itu, hotel perlu menganalisis data reservasi untuk mengidentifikasi tren, pola, dan faktor utama yang memengaruhi pembatalan.

**Mengapa ini penting?**
Proyek ini memberikan wawasan strategis bagi manajemen hotel untuk mengoptimalkan operasional, meningkatkan kepuasan pelanggan, dan meminimalkan kerugian akibat pembatalan reservasi. Selain itu, analisis ini juga dapat membantu dalam segmentasi pelanggan untuk mendukung strategi pemasaran yang lebih efektif.

### Rencana dan Metodologi
Proyek ini dirancang untuk memberikan solusi berbasis data terhadap permasalahan di atas dengan langkah-langkah berikut:
1. **Pengumpulan Data**: Menggunakan dataset "Hotel Bookings" yang mencakup informasi lengkap tentang reservasi, pembatalan, dan perilaku pelanggan.
2. **Pembersihan dan Persiapan Data**: Melakukan pembersihan data seperti mengisi nilai yang hilang, normalisasi teks, dan pembuatan variabel baru.
3. **Eksplorasi Data**: Mengidentifikasi pola dasar melalui statistik deskriptif dan visualisasi.
4. **Analisis Lanjutan**: Menggunakan teknik analisis untuk memahami faktor-faktor kunci yang memengaruhi pembatalan reservasi dan tren reservasi berdasarkan waktu.
5. **Pelaporan**: Menyusun laporan naratif berbasis wawasan yang relevan dengan kebutuhan bisnis.

### Pendekatan dan Teknik Analisis
Untuk mengatasi masalah ini, digunakan beberapa pendekatan berikut:
- **Statistik Deskriptif**: Untuk memberikan gambaran awal tentang dataset, termasuk distribusi variabel utama.
- **Visualisasi Data**: Membantu memetakan pola waktu, tren pembatalan, dan hubungan antar variabel.
- **Pengelompokan dan Segmentasi**: Membagi data pelanggan berdasarkan perilaku dan karakteristik untuk mengidentifikasi subkelompok penting.
- **Analisis Faktor**: Memahami pengaruh variabel tertentu terhadap tingkat pembatalan.

Pendekatan ini dirancang untuk memberikan wawasan yang relevan, praktis, dan dapat langsung diterapkan oleh pengguna hasil analisis.

### Manfaat Analisis
Analisis ini memberikan manfaat berikut bagi konsumen:
1. **Manajemen Hotel**: Memahami tren dan pola reservasi untuk meningkatkan efisiensi operasional dan strategi pemasaran.
2. **Tim Pemasaran**: Segmentasi pelanggan berdasarkan wawasan data untuk mengembangkan kampanye pemasaran yang lebih terarah.
3. **Manajemen Risiko**: Identifikasi faktor-faktor yang memengaruhi pembatalan, memungkinkan penerapan kebijakan pencegahan.
4. **Pengambilan Keputusan**: Data-driven insights yang mendukung keputusan strategis berbasis fakta.

## Dataset
Dataset yang digunakan dalam proyek ini berasal dari data **Hotel Bookings**. Dataset ini dapat diunduh melalui [tautan ini](https://www.kaggle.com/jessemostipak/hotel-booking-demand). Informasi lebih lanjut tersedia di deskripsi dataset tersebut.

- **Tujuan Awal Data**: Dataset ini awalnya dikumpulkan untuk menganalisis tren reservasi di industri perhotelan.
- **Jumlah Observasi**: Terdapat 119,390 observasi.
- **Jumlah Variabel**: Dataset memiliki 32 variabel utama.
- **Fitur Utama**:
  - Contoh variabel: `arrival_date`, `lead_time`, `is_canceled`, `customer_type`, dll.
- **Kekhasan Data**:
  - Terdapat nilai yang hilang dalam beberapa kolom seperti `children`.
  - Variabel seperti `meal` memerlukan normalisasi karena adanya variasi ejaan.
  - Variabel `adr` (average daily rate) memerlukan validasi untuk mengidentifikasi anomali.

### Langkah Pembersihan Data
1. Mengatasi nilai yang hilang:
   - Nilai hilang pada kolom `children` diisi dengan nilai median.
2. Normalisasi teks:
   - Kolom `meal` dinormalisasi untuk konsistensi nilai.
3. Pembuatan variabel baru:
   - Variabel `total_cost` dibuat dengan mengalikan `adr` dengan `stays_in_week_nights` dan `stays_in_weekend_nights`.

Setelah pembersihan, dataset akhir memiliki format yang konsisten dengan jumlah variabel bersih dan data yang siap untuk dianalisis. Berikut adalah gambaran singkat dataset:

| Variabel          | Tipe Data  | Deskripsi                                      |
|-------------------|------------|------------------------------------------------|
| arrival_date      | Date       | Tanggal kedatangan pelanggan                  |
| is_canceled       | Boolean    | Status pembatalan reservasi                   |
| customer_type     | Categorical| Jenis pelanggan                               |
| total_cost        | Numeric    | Total biaya menginap                          |

## Package yang Digunakan
Berikut adalah package Python yang diperlukan untuk mereplikasi analisis:
- `pandas`
- `numpy`
- `matplotlib`
- `seaborn`
- `plotly`
- `scikit-learn` (opsional untuk analisis lanjutan)

Pesan atau peringatan yang muncul saat memuat package telah dihilangkan untuk memastikan pengalaman yang mulus bagi pengguna.

## Metodologi
1. **Persiapan Data**:
   - Pengimporan dan pemeriksaan data mentah.
   - Pembersihan data, termasuk mengatasi nilai yang hilang dan normalisasi.
   - Penambahan variabel baru sesuai kebutuhan analisis.
   
2. **Eksplorasi Data**:
   - Deskriptif statistik pada variabel utama.
   - Visualisasi data untuk mengidentifikasi pola dan anomali.

3. **Analisis Data**:
   - Menggunakan teknik dasar analisis data untuk menjawab pertanyaan yang dirumuskan.
   - Visualisasi data yang informatif dan terstruktur.

4. **Rangkuman**:
   - Menyajikan temuan utama dalam narasi yang koheren.

## Hasil Utama
1. Analisis pola reservasi berdasarkan waktu.
2. Tren pembatalan reservasi dan faktor-faktor yang memengaruhinya.
3. Segmentasi pelanggan berdasarkan karakteristik reservasi.
4. Visualisasi interaktif menggunakan `plotly` untuk memberikan wawasan yang lebih baik.

## Panduan Penggunaan
1. Clone repository ini:
   ```bash
   git clone https://github.com/username/proyek_akhir_big_data.git
   ```
2. Install package yang diperlukan:
   ```bash
   pip install -r requirements.txt
   ```
3. Jalankan notebook:
   ```bash
   jupyter notebook Proyek_Tugas_Akhir_Analisis_big_data_(182_158_276).ipynb
   ```

## Struktur Repository
- `Proyek_Tugas_Akhir_Analisis_big_data_(182_158_276).ipynb`: Notebook utama dengan analisis dan visualisasi.
- `README.md`: Pengantar dan penjelasan proyek.
- `requirements.txt`: Daftar package Python yang diperlukan.

## Kontribusi
Kontribusi terbuka untuk meningkatkan analisis ini. Silakan buat pull request atau buka issue untuk diskusi lebih lanjut.

## Lisensi
Proyek ini dilisensikan di bawah [MIT License](LICENSE).
