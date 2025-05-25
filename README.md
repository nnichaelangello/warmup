# Pendahuluan Kompetisi Tahap Warmup: Sistem Pengelolaan Sampah Cerdas

## Latar Belakang

Dalam lanskap kota cerdas (*smart city*), pengelolaan sampah yang efisien dan berkelanjutan menjadi kebutuhan mendesak untuk mendukung keberlanjutan lingkungan dan kesejahteraan masyarakat. Pertumbuhan populasi urban, ekspansi aktivitas ekonomi, dan pengaruh faktor lingkungan menciptakan tantangan kompleks dalam memprediksi dan mengelola volume sampah. Pendekatan berbasis kecerdasan buatan (AI) menawarkan solusi inovatif untuk memahami pola produksi sampah, memungkinkan optimalisasi proses pengumpulan, pengolahan, dan daur ulang. Dengan memanfaatkan data secara strategis, sistem pengelolaan sampah cerdas dapat meningkatkan efisiensi operasional, mengurangi dampak lingkungan, dan memperkuat fondasi masyarakat cerdas (*smart society*) yang berorientasi pada masa depan.

Kompetisi tahap warmup ini dirancang untuk mengasah kemampuan peserta dalam merancang solusi prediktif berbasis AI menggunakan dataset sintetis yang merefleksikan dinamika pengelolaan sampah di sebuah kota fiktif. Peserta ditantang untuk mengeksplorasi dan menganalisis data yang kompleks dan saling terkait guna menghasilkan prediksi yang akurat serta relevan. Tahap ini bertujuan untuk mengembangkan kompetensi dalam analisis data multivariabel dan pengembangan model machine learning, sekaligus menumbuhkan pemikiran kritis dalam menangani permasalahan dunia nyata. Dengan fokus pada konteks pengelolaan sampah, kompetisi ini mendorong peserta untuk menciptakan solusi berbasis AI yang inovatif, andal, dan mampu memberikan dampak signifikan dalam ekosistem kota cerdas.

## Rumusan Masalah

Kompetisi ini menantang peserta untuk memprediksi jumlah sampah harian yang dihasilkan di berbagai wilayah kota berdasarkan informasi yang tersedia dalam dataset. Tujuan utama adalah merancang model AI yang mampu menghasilkan prediksi akurat melalui analisis data yang kompleks. Peserta diharapkan menjawab pertanyaan berikut:

1. Bagaimana data yang tersedia dapat dimanfaatkan untuk membangun model prediktif yang akurat dan andal?
2. Fitur mana yang memiliki pengaruh dominan terhadap produksi sampah, dan bagaimana hubungan antar fitur dapat dioptimalkan untuk meningkatkan performa model?
3. Bagaimana solusi teknis yang dikembangkan dapat diterjemahkan menjadi strategi praktis untuk mendukung pengelolaan sampah dalam konteks kota cerdas?

Penilaian dilakukan secara otomatis melalui platform Kaggle berdasarkan akurasi prediksi pada data pengujian, menggunakan metrik *Root Mean Squared Error* (RMSE). Peserta diharapkan menunjukkan kemampuan analisis mendalam, kreativitas dalam pengolahan data, dan pemahaman konteks untuk menghasilkan solusi yang kompetitif dan relevan.

## Informasi Dataset

Dataset yang disediakan terdiri dari tiga file CSV yang merepresentasikan skenario pengelolaan sampah di sebuah kota fiktif: `demographic_data.csv`, `commercial_activity_data.csv`, `weather_data.csv`, dan `waste_production.csv` (untuk pelatihan) serta `test.csv` (untuk pengujian). Dataset ini dirancang untuk menantang peserta dalam mengidentifikasi pola, hubungan antar variabel, dan fitur yang relevan secara mandiri. Berikut adalah rincian masing-masing dataset beserta kolomnya:

### 1. Data Demografi (`demographic_data.csv`)

Dataset ini menyediakan informasi demografi untuk setiap wilayah kota, mencerminkan karakteristik penduduk yang dapat memengaruhi produksi sampah.

- **Kolom**:
  - `region_id` (string): Identifikasi unik untuk setiap wilayah.
  - `population` (integer): Jumlah penduduk di wilayah tersebut.
  - `population_density` (float): Kepadatan penduduk per satuan luas.
  - `education_level_avg` (float): Rata-rata tingkat pendidikan penduduk, yang dapat memengaruhi kesadaran lingkungan.
  - `avg_income` (float): Rata-rata pendapatan tahunan per capita, mencerminkan daya beli dan gaya hidup.

### 2. Data Aktivitas Komersial (`commercial_activity_data.csv`)

Dataset ini mencakup informasi aktivitas komersial harian di setiap wilayah, yang merepresentasikan dinamika ekonomi sebagai faktor produksi sampah.

- **Kolom**:
  - `region_id` (string): Identifikasi unik untuk setiap wilayah.
  - `date` (string): Tanggal pengukuran dalam format YYYY-MM-DD.
  - `num_businesses` (integer): Jumlah bisnis aktif di wilayah tersebut.
  - `restaurant_count` (integer): Jumlah restoran, yang sering menghasilkan sampah organik dan non-organik.
  - `retail_count` (integer): Jumlah toko ritel, menunjukkan aktivitas perdagangan konsumen.
  - `industrial_activity_score` (float): Indikator intensitas aktivitas industri.

### 3. Data Cuaca (`weather_data.csv`)

Dataset ini menyediakan informasi cuaca harian untuk setiap wilayah, yang dapat memengaruhi perilaku penduduk dan pola produksi sampah.

- **Kolom**:
  - `region_id` (string): Identifikasi unik untuk setiap wilayah.
  - `date` (string): Tanggal pengukuran.
  - `temperature` (float): Suhu rata-rata harian.
  - `precipitation` (float): Curah hujan harian.
  - `humidity` (float): Tingkat kelembapan udara.

### 4. Data Produksi Sampah (`waste_production.csv`)

Dataset ini berisi informasi produksi sampah harian untuk pelatihan model, termasuk variabel target yang akan diprediksi.

- **Kolom**:
  - `region_id` (string): Identifikasi unik untuk setiap wilayah.
  - `date` (string): Tanggal pengukuran.
  - `waste_tons` (float): Jumlah sampah harian yang dihasilkan (dalam ton).

### 5. Data Pengujian (`test.csv`)

Dataset ini digunakan untuk menghasilkan prediksi yang akan disubmit ke platform Kaggle. Tidak mencakup variabel target.

- **Kolom**:
  - `region_id` (string): Identifikasi unik untuk setiap wilayah.
  - `date` (string): Tanggal pengukuran.

## Panduan untuk Peserta

- **Eksplorasi Dataset**: Peserta diharapkan untuk menganalisis dataset secara mendalam guna mengidentifikasi pola dan hubungan antar variabel yang relevan untuk prediksi.
- **Tujuan Kompetisi**: Merancang model prediktif untuk memprediksi jumlah sampah harian pada data pengujian, dievaluasi menggunakan metrik *Root Mean Squared Error* (RMSE) melalui platform Kaggle.
- **Format Submission**: File CSV dengan kolom `region_id`, `date`, dan `waste_tons`, yang harus diunggah ke platform Kaggle untuk penilaian otomatis.
- **Inovasi dan Kreativitas**: Peserta didorong untuk mengembangkan strategi pengolahan data dan pemodelan yang inovatif, dengan memanfaatkan analisis mendalam untuk menghasilkan solusi yang akurat dan relevan dalam konteks pengelolaan sampah kota cerdas.
