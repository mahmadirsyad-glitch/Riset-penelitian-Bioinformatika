# Dasar Teori, Urgensi, dan Batasan Penelitian (Scope & Limitations)

## 1. Latar Belakang & Urgensi Penelitian (Research Urgency)

### A. Beban Klinis Diabetes Melitus Tipe 2 (DMT2) & Keterbatasan Terapi Konvensional
* **Krisis Global dan Nasional:** Diabetes Melitus Tipe 2 (DMT2) merupakan salah satu beban kesehatan terbesar dengan angka prevalensi yang terus meningkat, memicu komplikasi sistemik serius seperti nefropati, retinopati, dan gangguan vaskular.
* **Kelemahan Agen Farmakologis Saat Ini:** Penggunaan obat antidiabetik oral konvensional (seperti Metformin atau Acarbose) sering kali menimbulkan efek samping gastrointestinal jangka panjang, risiko hipoglikemia, atau resistensi sekunder. Hal ini mendorong urgensi eksplorasi agen fitoterapi alternatif yang lebih spesifik dan aman.

### B. Problemmatika Ekstrak Propolis Mentah & Kesenjangan Geografis (*Research Gap*)
* **Variabilitas Fitokimia Ekstrak Mentah:** Sebagian besar riset *wet lab* menggunakan ekstrak propolis mentah tanpa standardisasi senyawa aktif yang jelas. Padahal, komposisi kimia propolis sangat dipengaruhi oleh vegetasi tumbuhan dan iklim wilayah lebah dalam mencari getah.
* **Komparasi Subtropis vs Tropis:** Literatur menunjukkan bahwa lebah di wilayah iklim empat musim (Subtropis, *poplar-type*) menghasilkan kadar ester fenolik tinggi seperti CAPE (*Caffeic Acid Phenethyl Ester*) dan aglikon flavonoid (*Pinocembrin*, *Galangin*) sebagai mekanisme pertahanan suhu. Di sisi lain, propolis tropis Indonesia kaya akan senyawa prenilasi dan terpenoid. 
* **Celah Penelitian:** Belum banyak studi komparatif *in-silico* yang secara presisi membedah afinitas ikatan molekuler antara senyawa khas propolis subtropis melawan propolis tropis Indonesia terhadap target protein multi-enzim diabetes secara bersamaan, atau bisa juga menjadi peluang riset ilmiah membahas masalah komprehensif lainnya secara bioinformatika untuk landasan awal sebelum transisi ke wet lab.

### C. Efisiensi Metodologis (Pendekatan Komputasi / Dry Lab)
* **Kendala Uji Langsung:** Menguji ratusan kandidat senyawa secara acak langsung melalui laboratorium basah (*wet lab*) membutuhkan biaya besar, waktu yang lama, dan kendala etika hewan coba.
* **Solusi Bioinformatika:** Penapisan awal (*screening*) melalui *Molecular Docking* dan analisis farmakokinetik *ADMET* menjadi langkah mutlak untuk menyaring *lead compound* paling potensial sebelum dilanjutkan ke tahap validasi klinis.

---

## 2. Relevansi dengan Kompetensi Inti ATLM (Analis Kesehatan)
* **Korelasi Biomarker Klinik:** Target makromolekul dalam studi komputasi ini ($\alpha$-Glucosidase dan PPAR-$\gamma$) berkaitan langsung dengan regulasi kontrol glukosa darah postprandial dan sensitivitas insulin. 
* **Parameter Laboratorium Medik:** Hasil akhir riset ini bermuara pada pemahaman dasar molekuler yang memengaruhi parameter pemeriksaan rutin laboratorium klinik, seperti **Glukosa Darah Puasa (GDP)**, **HbA1c**, serta profil keamanan fungsi organ (Ureum/Kreatinin dan SGOT/SGPT).
* **Peran ATLM Modern:** Memperkuat kapasitas analis kesehatan tidak hanya sebagai pelaksana uji sampel pasif, tetapi juga memahami landasan biokimiawi molekuler dari patofisiologi penyakit dan agen pencegahannya.

---

## 3. Ruang Lingkup dan Batasan Penelitian (Scope & Limitations)

* **Metodologi Utama:** Penelitian ini murni berbasis komputasi kering (*dry lab / in-silico*), mencakup:
  1. *Molecular Docking* (penambatan molekul ligan ke reseptor target).
  2. Visualisasi interaksi 3D (ikatan hidrogen dan hidrofobik).
  3. Evaluasi profil farmakokinetik dan toksisitas (*ADMET* via SwissADME dan pkCSM).
* **Batasan Eksperimental:** Penelitian tidak mencakup uji laboratorium basah (*wet lab*) seperti kultur sel (*in-vitro*) maupun hewan coba (*in-vivo*), melainkan berfokus pada perumusan rekomendasi *lead compound* terbaik berdasarkan skor energi ikatan komputasi.
* **Variabel Batasan Target (PDB ID):** 
  * Enzim $\alpha$-Glucosidase (PDB ID: `3W37`)
  * Reseptor PPAR-$\gamma$ (PDB ID: `2P4Y`)
  * dan reseptor lainnya jika ditemukan lebih efektif
