# Praktikum Pemrograman Aplikasi Berbasis Web (PABW)
## Pertemuan 3: HTML5 Semantik, Form, Media & Aksesibilitas

**Topik Halaman:** Mengatur Jam Perjalanan  
**Berkas Utama:** `worksheet-p3/profil.html`

---

### Hasil Pemeriksaan & Uji Aksesibilitas (Lembar F)

- **Lighthouse — Accessibility:** **94 / 100**
  - Catatan: Terdapat sorotan minor pada ukuran target sentuh (*target-size*) tautan navigasi karena halaman belum diberi gaya CSS (*padding/margin* area klik), yang akan dipelajari pada Pertemuan 4.
- **Temuan axe DevTools:** 0 pelanggaran kritis (*0 issues*).
- **Uji Navigasi Keyboard (Papan Ketik):** Lancar. Seluruh tautan dan elemen formulir dapat difokuskan berurutan dengan tombol `Tab` tanpa terjebak (*no focus trap*).
- **Uji Tautan Navigasi:** Semua benar. Tautan melompat tepat ke `#bagian-1`, `#bagian-2`, dan `#footer`.
- **Uji Label:** Semua benar. Setiap `<label for>` terhubung langsung ke `<input id>`, sehingga saat teks label diklik kursor langsung aktif di kolom isian.

---

### Pengungkapan Penggunaan AI (AI Disclosure)

Sesuai dengan ketentuan integritas akademik pada Lembar G:

1. **Bagian yang Dikerjakan Mandiri:**
   - Menentukan topik dan ide orisinal halaman (*Mengatur Jam Perjalanan*).
   - Memilih dan menyertakan berkas gambar maskot/ilustrasi perjalanan (`images.jpg`).
   - Menyusun kerangka halaman, tabel data jadwal perjalanan, serta kolom formulir rencana perjalanan.

2. **Bagian yang Dibantu AI:**
   - **Audit Lighthouse Accessibility:** Menjalankan pengujian Lighthouse untuk kategori *Accessibility* serta mencatat skor dan analisis temuannya, dikarenakan tab Lighthouse di peramban Chrome pengguna tidak menampilkan opsi pengujian *Accessibility*.
   - Konsultasi pengecekan mandiri terhadap checklist kelengkapan elemen semantik HTML5 dan rubrik penilaian.
