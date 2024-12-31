# analisis-hotel-booking

# Analisis Data Reservasi Hotel

## Pendahuluan
Proyek ini bertujuan untuk menganalisis data reservasi hotel, mengidentifikasi pola pembatalan reservasi, dan faktor-faktor yang memengaruhi keputusan pelanggan. Dataset berisi informasi tentang reservasi hotel dari tahun 2015 hingga 2017.

---

## Data yang Digunakan
- **Dataset:** [Hotel Bookings](#) *(Tautkan ke dataset)*
- **Jumlah Kolom:** X
- **Jumlah Baris:** Y

---

## Langkah-Langkah Analisis
1. **Eksplorasi Awal Data**
   - Melihat struktur data.
   - Memeriksa nilai hilang dan duplikasi.
2. **Pembersihan Data**
   - Menangani nilai hilang.
   - Normalisasi tipe data.
3. **Analisis Data**
   - Analisis distribusi pembatalan.
   - Mengidentifikasi hubungan antara fitur, seperti jumlah permintaan khusus dan tingkat pembatalan.
4. **Visualisasi**
   - Membuat visualisasi interaktif dan statistik deskriptif.

---

## Temuan
1. Sebagian besar pembatalan berasal dari pelanggan dengan kategori X.
2. Pelanggan dengan lebih banyak permintaan khusus cenderung memiliki tingkat pembatalan lebih rendah.
3. [Masukkan temuan lainnya di sini.]

---

## Kesimpulan
Hasil analisis ini memberikan wawasan bagi manajemen hotel untuk meningkatkan pengalaman pelanggan dan mengurangi tingkat pembatalan.

---

## Cara Menjalankan Proyek
1. Pastikan Anda memiliki Python dan library yang diperlukan:
   - pandas
   - numpy
   - seaborn
   - matplotlib
   - plotly
2. Jalankan file notebook Jupyter `Proyek_Tugas_Akhir.ipynb`.

---

## Instruksi Notebook
Berikut adalah langkah-langkah yang diikuti dalam notebook:

### 1. Eksplorasi Awal Data
```python
# Melihat struktur data
print(df.head())
print(df.info())
print(df.describe())
```

### 2. Pembersihan Data
```python
# Menangani nilai hilang
df = df.dropna()
# Normalisasi tipe data
df['reservation_status_date'] = pd.to_datetime(df['reservation_status_date'])
```

### 3. Analisis Data dan Visualisasi
```python
# Analisis distribusi pembatalan
import seaborn as sns
import matplotlib.pyplot as plt
sns.countplot(data=df, x='is_canceled')
plt.show()

# Visualisasi hubungan special requests dan pembatalan
import plotly.express as px
fig = px.bar(df, x='total_of_special_requests', y='is_canceled', color='is_canceled', barmode='group')
fig.show()
```

