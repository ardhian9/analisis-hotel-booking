# Proyek Analisis Data Hotel Bookings

## Table of Contents
- [Pendahuluan](#pendahuluan)
- [Langkah Analisis](#langkah-analisis)
  - [Persiapan Data](#persiapan-data)
  - [Eksplorasi Data](#eksplorasi-data)
  - [Visualisasi Data](#visualisasi-data)
- [Wawasan Utama](#wawasan-utama)
- [Teknologi yang Digunakan](#teknologi-yang-digunakan)
- [Kesimpulan dan Implikasi](#kesimpulan-dan-implikasi)
- [Saran Pengembangan](#saran-pengembangan)
- [Team](#team)

## Pendahuluan
Proyek ini bertujuan untuk menganalisis dataset "Hotel Bookings" guna memahami pola pembatalan pemesanan berdasarkan jumlah permintaan khusus yang diajukan oleh pelanggan. Proyek ini melibatkan proses pembersihan data, eksplorasi, analisis, dan visualisasi untuk memberikan wawasan yang relevan bagi pemangku kepentingan.

Dataset yang digunakan mencakup variabel seperti:
- **Total of Special Requests**: Jumlah permintaan khusus yang diajukan pelanggan.
- **Is Canceled**: Status pembatalan (0 untuk "Not Canceled" dan 1 untuk "Canceled").

Analisis ini dilakukan menggunakan Python, dengan hasil visualisasi dan laporan yang disusun untuk menggambarkan temuan utama.

## Langkah Analisis
### Persiapan Data
- Dataset diperiksa untuk mengetahui kualitas data seperti nilai hilang dan format yang tidak sesuai.
- Data bersih mencakup dua kolom utama: `total_of_special_requests` dan `is_canceled`.

### Eksplorasi Data
- Distribusi `total_of_special_requests` diperiksa untuk memahami frekuensi dari berbagai jumlah permintaan khusus.
- Hubungan antara `total_of_special_requests` dan `is_canceled` dianalisis untuk menemukan pola pembatalan.

### Visualisasi Data
- **Distribusi Total of Special Requests**: Visualisasi bar chart menggambarkan jumlah pelanggan untuk setiap kategori permintaan khusus.
- **Relasi dengan Pembatalan**: Grouped bar chart menunjukkan pola pembatalan berdasarkan jumlah permintaan khusus.

## Wawasan Utama
1. Pelanggan dengan 0 permintaan khusus memiliki proporsi pembatalan dan non-pembatalan yang seimbang.
2. Dengan meningkatnya jumlah permintaan khusus (1 hingga 3), kecenderungan pembatalan menjadi lebih terfokus, dengan beberapa kategori hanya mencakup kasus pembatalan.
3. Permintaan khusus yang lebih tinggi (3) lebih jarang terjadi dibandingkan dengan permintaan yang lebih rendah.

## Teknologi yang Digunakan
- **Python Libraries**:
  - Pandas: Untuk manipulasi dan pembersihan data.
  - Plotly: Untuk visualisasi data interaktif.

## Kesimpulan dan Implikasi
Analisis ini memberikan wawasan tentang bagaimana jumlah permintaan khusus memengaruhi pembatalan pemesanan. Pemahaman ini dapat membantu hotel dalam mengelola permintaan pelanggan dan memprediksi kemungkinan pembatalan.

## Saran Pengembangan
- Menambah variabel lain dari dataset (misalnya, durasi menginap, jenis kamar) untuk analisis yang lebih komprehensif.
- Menggunakan model prediktif untuk memprediksi pembatalan berdasarkan beberapa fitur utama.
- Mengintegrasikan analisis ini dengan data historis untuk tren waktu yang lebih baik.

