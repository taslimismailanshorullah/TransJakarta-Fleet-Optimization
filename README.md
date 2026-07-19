# Optimizing TransJakarta Fleet Allocation using Route Density Clustering

Repositori ini berisi analisis data penumpang TransJakarta untuk mensegmentasi prioritas rute menggunakan algoritma *Machine Learning*. Proyek ini mengusulkan transisi dari penjadwalan statis menuju model *Dynamic Fleet Allocation* (DFA) guna mengatasi inefisiensi operasional.

## Latar Belakang & Objektif
TransJakarta menghadapi ketidakseimbangan rute yang parah, di mana penjadwalan statis menyebabkan penumpukan penumpang di rute utama sementara bus di rute lain berjalan kosong. Analisis Pareto menunjukkan bahwa Top 10 rute saja menanggung 43,9% dari total beban penumpang (52,8 Juta penumpang). 

Proyek ini bertujuan untuk:
1. Mengidentifikasi rute-rute kritis menggunakan Analisis Pareto.
2. Menganalisis fluktuasi permintaan musiman (*seasonality*).
3. Mengelompokkan rute ke dalam klaster prioritas menggunakan K-Means untuk alokasi sumber daya yang lebih tepat sasaran.

## Data & Metodologi
- **Sumber Data:** Data Penumpang TransJakarta 2021 (Jakarta Open Data).
- **Pendekatan Analisis:** *Exploratory Data Analysis* (EDA) & *Unsupervised Learning*.
- **Metode Clustering:** K-Means Clustering (pemilihan *k* optimal menggunakan *Elbow Method* setelah normalisasi data).

## Temuan & Rekomendasi Utama
Berdasarkan hasil K-Means Clustering, rute disegmentasi menjadi tiga kategori untuk rekomendasi *Dynamic Fleet Allocation* (DFA):
1. **High Priority (50%):** Didominasi oleh koridor utama BRT dan Mikrotrans. **Rekomendasi:** Peningkatan frekuensi, penggunaan bus gandeng (*articulated buses*), dan layanan ekspres pada jam sibuk (terutama rute super-demand seperti Blok M - Kota).
2. **Medium Priority (25%):** Berfungsi utamanya sebagai armada *feeder*. **Rekomendasi:** Pertahankan tingkat layanan standar dengan pemantauan performa berbasis data secara rutin.
3. **Low Priority (25%):** Didominasi oleh Angkutan Umum Integrasi yang menunjukkan redundansi dan efisiensi rendah. **Rekomendasi:** Evaluasi ulang untuk efisiensi, penggabungan/penghapusan rute yang kurang berkinerja, dan realokasi armada ke koridor dengan dampak yang lebih tinggi.

*(Letakkan screenshot poster infografis TransJakarta kamu di sini dengan cara men-drag and drop file gambarnya)*

## Struktur Repositori
- `data/` : Folder berisi dataset historis penumpang TransJakarta.
- `notebooks/` : *Source code* lengkap (Jupyter Notebook) untuk EDA, Pareto Analysis, dan K-Means Clustering.
- `Optimizing TransJakarta Fleet Allocation using Route Density Clustering.png` : Poster infografis rangkuman eksekutif proyek.
