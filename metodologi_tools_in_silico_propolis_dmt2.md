# Panduan Metodologi & Tools In-Silico (Hulu ke Hilir) - Uji Docking Propolis DMT2

Dokumen ini merangkum secara komprehensif alur kerja komputasi (molecular docking & ADMET), perangkat lunak (tools), basis data resmi, serta pranala web valid internasional untuk riset in-silico propolis terhadap target Diabetes Melitus Tipe 2 (DMT2) berbasis korelasi patologi klinik (ATLM).

---

## 1. Alur Kerja Hulu: Pengambilan Data & Preparasi Struktur

### A. Penyiapan Ligan (Senyawa Aktif Propolis)
Metabolit sekunder propolis (seperti CAPE, Pinocembrin, Chrysin, Galangin) disiapkan struktur 3 dimensi (3D)-nya dan dioptimasi energi geometrinya.

* **PubChem (NCBI)**
  * **Link Web:** https://pubchem.ncbi.nlm.nih.gov
  * **Fungsi:** Pencarian dan pengunduhan file struktur 3D molekul senyawa aktif dalam format SDF / MOL2.
* **Avogadro (Local Software)**
  * **Link Web:** https://avogadro.cc
  * **Fungsi:** Optimasi geometri 3D, minimisasi energi molekul (forcefield MMFF94/UFF), serta penambahan parsial muatan (Gasteiger charges).
* **MarvinSketch / ChemDraw (Optional)**
  * **Link Web:** https://chemaxon.com/marvin
  * **Fungsi:** Penataan gambar struktur 2D/3D senyawa alami jika diperlukan modifikasi gugus fungsi.

### B. Penyiapan Reseptor (Protein Target DMT2)
Struktur kristal 3D reseptor enzim target diunduh dan dibersihkan dari molekul pengganggu (air dan ligan alami).

* **RCSB Protein Data Bank (PDB)**
  * **Link Web:** https://www.rcsb.org
  * **Fungsi:** Unduh file koordinat 3D protein target dalam format `.pdb`:
    * Alpha-Glucosidase (PDB ID: **3W37**)
    * PPAR-Gamma (PDB ID: **2P4Y**)
* **UCSF Chimera**
  * **Link Web:** https://www.cgl.ucsf.edu/chimera/
  * **Fungsi:** Pembersihan molekul air (H2O), pemisahan ligan alami (native ligand), dan penambahan atom hidrogen polar pada struktur protein.

---

## 2. Alur Kerja Proses: Penambatan Molekuler (Molecular Docking)

### A. Validasi Metode (Redocking Native Ligand)
Sebelum simulasi ligan uji dilakukan, posisi Grid Box dipastikan valid melalui prosedur redocking ligan alami dengan kriteria RMSD < 2.0 Angstrom.

* **AutoDock Tools (ADT / MGLTools)**
  * **Link Web:** https://ccsb.scripps.edu/mgltools/
  * **Fungsi:** Menentukan posisi pusat koordinat (center X, Y, Z) dan ukuran dimensi (size X, Y, Z) dari Grid Box pada kantong aktif reseptor.

### B. Eksekusi Penambatan Molekuler
* **AutoDock Vina**
  * **Link Web:** https://vina.scripps.edu
  * **Fungsi:** Engine utama simulasi penambatan molekuler (molecular docking) untuk menghitung afinitas ikatan (Binding Affinity / Delta G dalam kcal/mol).
* **PyRx (Virtual Screening Tool)**
  * **Link Web:** https://pyrx.sourceforge.io
  * **Fungsi:** Antarmuka (GUI) pengganti eksekusi AutoDock Vina secara massal (*batch docking*) untuk banyak ligan propolis sekaligus.

---

## 3. Alur Kerja Hilir: Visualisasi & Profil ADMET

### A. Visualisasi & Analisis Interaksi Residu
* **BIOVIA Discovery Studio Visualizer**
  * **Link Web:** https://www.3ds.com/products/biovia/discovery-studio/visualization
  * **Fungsi:** Analisis diagram 2D dan 3D interaksi molekuler (ikatan hidrogen, interaksi hidrofobik, kontak Van der Waals) serta identifikasi residu asam amino kantong aktif.
* **PyMOL Molecular Graphics System**
  * **Link Web:** https://pymol.org
  * **Fungsi:** Pembuatan visualisasi 3D kualitas tinggi (publication-ready figure) posisi penempelan ligan pada struktur 3D reseptor.

### B. Prediksi Farmakokinetik & Toksisitas (ADMET)
* **SwissADME (SIB Swiss Institute of Bioinformatics)**
  * **Link Web:** http://www.swissadme.ch
  * **Fungsi:** Evaluasi Lipinski Rule of Five (bobot molekul, logP, donor/akseptor hidrogen), penyerapan gastrointestinal (GI absorption), dan permeabilitas membran.
* **pkCSM (University of Cambridge / Melbourne)**
  * **Link Web:** http://structure.bioc.cam.ac.uk/pkcsm
  * **Fungsi:** Prediksi profil ADMET kuantitatif (volume distribusi, klirens, toksisitas organ/hepatotoksisitas, dan uji AMES mutagenisitas).
* **ProTox 3.0 (Charité - Universitätsmedizin Berlin)**
  * **Link Web:** https://tox.charite.de/protox3/
  * **Fungsi:** Prediksi tingkat toksisitas oral (LD50), kelas toksisitas, serta analisis fragmen kimia beracun secara in-silico.

---

## 4. Tahap Translasi Klinis ATLM (Intepretasi Biomarker)

* **Inhibisi Alpha-Glucosidase** -> Parameter Glukosa Darah Postprandial (GD2PP).
* **Aktivasi PPAR-Gamma** -> Parameter Glukosa Darah Puasa (GDP), Indeks HOMA-IR, dan HbA1c.
* **Organ Protection Endpoint** -> Parameter Fungsi Ginjal (Ureum, Kreatinin, eGFR) dan Fungsi Hati (SGOT, SGPT).