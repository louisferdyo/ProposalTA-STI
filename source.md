# Rangkuman Riset: Neural Behaviour Sense System (NBSS) untuk Kukang Sunda (Nycticebus coucang)

[cite_start]**Judul Penelitian:** Model Pengenalan Ekspresi Wajah Primata Dilindungi Berbasis Artificial Intelligence [cite: 7, 24]
[cite_start]**Institusi Pengusul:** Institut Teknologi Bandung (ITB) [cite: 11]
[cite_start]**Mitra Riset:** IPB University & Universitas Padjadjaran (UNPAD) [cite: 35]

---

## 1. Latar Belakang & Masalah
[cite_start]Konservasi primata endemik seperti Kukang Sunda (*Nycticebus coucang*) menghadapi tantangan besar karena sifat nokturnal dan pergerakannya yang lambat[cite: 51]. [cite_start]Metode observasi manual saat ini rentan human error dan tidak efisien[cite: 52]. [cite_start]Kesalahan dalam perawatan (pakan, penanganan) dapat menyebabkan stres, sakit, hingga kematian[cite: 71].

**Solusi yang Diajukan:**
[cite_start]Pengembangan sistem *Video Analytics* berbasis AI untuk mendeteksi ekspresi wajah kukang secara *real-time* (santai, stres, sakit) guna membantu petugas konservasi[cite: 53, 79]. namun untuk sementara, sampai tugas akhir ini berakhir hanya perlu dibuat berbasis video belum sampai realtime

---

## 2. Metodologi Penelitian & Kolaborasi
[cite_start]Penelitian menggunakan metode *Systems Development Life Cycle* (SDLC) [cite: 143] dengan pembagian tugas sebagai berikut:

### A. Tim ITB (Teknologi & AI)
* [cite_start]**Fokus:** Digitalisasi dataset, pengembangan model *Computer Vision*, dan sistem deteksi otomatis[cite: 112, 113, 114].
* [cite_start]**Target Teknis:** Mendeteksi perilaku pergerakan telinga, mulut, dan mata[cite: 116].
* [cite_start]**Luaran:** Dataset terlabeli dan model deteksi ekspresi wajah[cite: 202].

### B. Tim IPB (Perilaku & Ground Truth)
* [cite_start]**Fokus:** Meneliti hubungan pancaran warna cahaya mata, posisi mata, telinga, dan mulut dengan ekspresi perilaku kukang[cite: 209].
* [cite_start]**Validasi:** Menyediakan validasi anotasi label berdasarkan perilaku hewan[cite: 117].

### C. Tim UNPAD (Hormonal & Fisiologis)
* [cite_start]**Fokus:** Validasi respons lingkungan melalui analisis hormon[cite: 121].
* [cite_start]**Metode:** Ekstraksi feses untuk menghitung konsentrasi hormon kortisol (stres) dan dopamin (senang/nyaman) menggunakan metode ELISA[cite: 206].
* [cite_start]**Tambahan:** Identifikasi mikrobiota saluran cerna[cite: 207].

---

## 3. Indikator Ekspresi & Perilaku (Temuan Wawancara & Proposal)
Berdasarkan proposal dan wawancara dengan drh. Dwi Wahyudha, indikator utama yang diamati adalah:

1.  [cite_start]**Fitur Wajah:** Fokus utama pada perubahan bentuk dan gerak **Mulut, Mata, dan Telinga**[cite: 75, 209].
2.  [cite_start]**Mata:** Ada potensi indikator dari "pancaran cahaya mata" atau perubahan warna mata saat terkena cahaya, namun riset spesifik pada kukang masih minim (mengacu pada primata lain)[cite: 209].
3.  [cite_start]**Hormonal (Ground Truth):** Tingkat stres atau kenyamanan divalidasi melalui kadar **Kortisol** dan **Dopamin** pada feses[cite: 206].

---

## 4. Kendala Teknis & Lapangan (Hasil Wawancara)
Implementasi di lapangan (Pusat Rehabilitasi IPB/IARI & Cikamurang) menghadapi tantangan fisik yang signifikan yang belum terakomodasi sepenuhnya dalam desain awal:

### A. Isu Kandang vs. Kamera
* **Masalah:** Kandang habituasi yang digunakan saat ini memiliki tinggi **4 meter**.
* **Dampak:** Jarak antara kamera CCTV (yang biasanya dipasang di atas/sudut) dan kukang menjadi terlalu jauh.
* **Akibat:** Detail fitur wajah mikro (telinga, mata, mulut) **sulit atau tidak mungkin diamati** dengan jelas menggunakan kamera standar.

### B. Isu Resolusi & Pencahayaan
* [cite_start]**Masalah:** Kukang adalah hewan nokturnal, sehingga pengamatan dilakukan dalam kondisi gelap/minim cahaya[cite: 95].
* **Dampak:** Kamera CCTV standar seringkali menghasilkan *noise* tinggi pada kondisi *low-light*, menghilangkan detail ekspresi wajah.

### C. Isu Stres vs. Validitas Data
* **Opsi Solusi:** Memindahkan kukang ke kandang kecil (tinggi 50cm x p 100 cm x l 100 cm) agar dekat dengan kamera.
* **Risiko:** Kandang sempit akan **meningkatkan tingkat stres** secara drastis.
* **Dampak pada AI:** Data yang terekam hanya akan berisi ekspresi "Stres", sehingga model AI menjadi bias (tidak bisa mengenali ekspresi "Santai" atau "Normal" karena sampelnya tidak ada).

---

## 5. Solusi & Rekomendasi Mitigasi
Berdasarkan diskusi masalah di atas, berikut adalah langkah mitigasi yang disepakati/diusulkan:

1.  **Spesifikasi Kamera:**
    * CCTV standar tidak memadai. Dibutuhkan kamera dengan resolusi tinggi (4K/High MP) yang memiliki kemampuan *Night Vision/Infrared* superior untuk menangkap detail dari jarak jauh atau dalam kondisi gelap total.
    * Posisi kamera harus *multi-angle* untuk mengantisipasi pergerakan kukang yang bersembunyi.

2.  **Strategi Kandang (Adaptasi):**
    * Jika menggunakan kandang kecil (50x100 cm) untuk pengambilan data jarak dekat, kukang **wajib** melalui proses adaptasi/habituasi terlebih dahulu.
    * Tujuannya untuk memastikan kukang kembali ke kondisi emosi "netral" sebelum pengambilan data dimulai, agar hormon kortisol turun.

3.  **Faktor Lingkungan:**
    * Variabel intensitas cahaya, suara, suhu, dan kelembaban harus dikontrol karena sangat mempengaruhi perilaku kukang.
    * Faktor usia (bayi vs dewasa) dinilai kurang berpengaruh dibandingkan "durasi adaptasi di habitat baru".

---

## 6. Rencana Kerja Selanjutnya (Roadmap 2025-2026)
1.  [cite_start]**Tahap Inisiasi:** Digitalisasi dataset (pengambilan video & foto) serta pelabelan ekspresi wajah[cite: 234, 235].
2.  [cite_start]**Pengadaan Alat:** Pembelian/Penyewaan CCTV spesifikasi khusus dan *harddisk* penyimpanan data besar (4TB/2TB)[cite: 258].
3.  [cite_start]**Pengumpulan Data Lapangan:** Perekaman video 24 jam di lokasi mitra (IPB/UNPAD)[cite: 171].
4.  [cite_start]**Analisis Lab:** Ekstraksi feses untuk data ground truth hormonal[cite: 206].