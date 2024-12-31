# Proyek Analisis Data Hotel Bookings

## DAFTAR ISI
- [PENDAHULUAN ✅](#Pendahuluan)
- [IMPORT LIBRARY ✅](#Import-Library)
- [DOWNLOAD DATA ✅](#Download-data)
- [LOAD DATASET ✅](#Load-Dataset)
- [HANDLING MISSING VALUE ✅](#HANDLING-MISSING-VALUE)
- [VISUALISASI DEMOGRAFIS TAMU ✅](#VISUALISASI-DEMOGRAFIS-TAMU)
- [VISUALISASI POLA PEMESANAN HOTEL ✅](#VISUALISASI-POLA-PEMESANAN-HOTEL)
- [ANALISIS LANJUTAN UNTUK MENGIDENTIFIKASI KOLOM-KOLOM YANG MEMPENGARUHI TERJADINYA PEMBATALAN PEMESANAN (ExtraTreesClassifier) ✅](#NALISIS-LANJUTAN)
- [ANALISIS DAN VISUALISASI FAKTOR-FAKTOR YANG BERKONTRIBUSI TERHADAP PEMBATALAN PEMESANAN ✅](#ANALISIS-DAN-VISUALISASI)
- [Team](#team)

## **Pendahuluan**
Topik yang kita pilih yaitu: "Permintaan Pemesanan Hotel", dataset ini dapat digunakan untuk menganalisis pola pemesanan, tingkat pembatalan, dan faktor-faktor lain yang mempengaruhi operasional hotel dan banyaknya pemesanan yang dibatalkan.

**Data Dictionary**
- hotel - Jenis hotel (H1 = Resort Hotel, H2 = City Hotel).
- is_canceled - Menunjukkan apakah reservasi dibatalkan (1) atau tidak (0).
- lead_time - Jumlah hari antara tanggal pemesanan masuk dan tanggal kedatangan.
- arrival_date_year - Tahun kedatangan.
- arrival_date_month - Bulan kedatangan.
- arrival_date_week_number - Nomor minggu dalam tahun untuk tanggal kedatangan.
- arrival_date_day_of_month - Tanggal kedatangan dalam bulan.
- stays_in_weekend_nights - Jumlah malam akhir pekan (Sabtu atau Minggu) yang * * dipesan atau diinapi.
- stays_in_week_nights - Jumlah malam kerja (Senin hingga Jumat) yang dipesan atau diinapi.
- adults - Jumlah orang dewasa.
- children - Jumlah anak-anak.
- babies - Jumlah bayi.
- meal - Jenis paket makan yang dipesan: Undefined/SC (tanpa paket makan), BB (Bed & Breakfast), HB (Half board), FB (Full board).
- country - Negara asal, menggunakan format ISO 3155–3:2013.
- market_segment - Segmen pasar: "TA" (Travel Agents), "TO" (Tour Operators).
- distribution_channel - Saluran distribusi pemesanan: "TA" (Travel Agents), "TO" (Tour Operators).
- is_repeated_guest - Menunjukkan apakah tamu merupakan tamu yang sama (1) atau bukan (0).
- previous_cancellations - Jumlah pemesanan sebelumnya yang dibatalkan oleh pelanggan.
- previous_bookings_not_canceled - Jumlah pemesanan sebelumnya yang tidak dibatalkan oleh pelanggan.
- reserved_room_type - Kode jenis kamar yang dipesan (dianonimkan).
- assigned_room_type - Kode jenis kamar yang diberikan, yang mungkin berbeda dengan kamar yang dipesan (dianonimkan).
- booking_changes - Jumlah perubahan yang dilakukan pada pemesanan sebelum check-in atau pembatalan.
- deposit_type - Jenis deposit: No Deposit (tanpa deposit), Non Refund (deposit penuh), Refundable (deposit sebagian).
- agent - ID agen perjalanan yang melakukan pemesanan (dianonimkan).
- company - ID perusahaan/lembaga yang bertanggung jawab atas pemesanan atau pembayaran (dianonimkan).
- days_in_waiting_list - Jumlah hari pemesanan berada di daftar tunggu sebelum dikonfirmasi.
- customer_type - Jenis pemesanan: Contract (terkait kontrak), Group (terkait grup), Transient (tidak terkait grup atau kontrak), Transient-party (terhubung dengan pemesanan transient lainnya).
- adr - Rata-rata tarif harian, dihitung dengan membagi total transaksi penginapan dengan total malam menginap.
- required_car_parking_spaces - Jumlah tempat parkir mobil yang diminta oleh pelanggan.
- total_of_special_requests - Jumlah permintaan khusus (misalnya, tempat tidur twin atau lantai atas).
- reservation_status - Status reservasi: Canceled (dibatalkan), Check-Out (pelanggan sudah check-out), No-Show (pelanggan tidak check-in).
- reservation_status_date - Tanggal saat status terakhir reservasi ditetapkan.

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

## Team
NAMA KELOMPOK
- Rangga Saputra Hari Pratama (202110370311182)
- Muhammad Yusuf Rahmatullah (202110370311158)
- Ardian Ahmad Afifuddin (201910370311276)
