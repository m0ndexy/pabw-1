# Praktikum Pemrograman Aplikasi Berbasis Web (PABW)
## Pertemuan 3: HTML5 Semantik, Form, Media & Aksesibilitas

- **Nama Mahasiswa:** m0ndexy
- **NIM:** 25523190
- **Topik Halaman:** Mengatur Jam Perjalanan
- **Berkas Utama:** [`worksheet-p3/profil.html`](worksheet-p3/profil.html)

---

### Deskripsi Halaman
Halaman profil ini dibangun menggunakan standar **HTML5 Semantik murni** tanpa CSS (sesuai ruang lingkup Pertemuan 3). Halaman ini berfungsi untuk menampilkan dan mengatur perencanaan waktu perjalanan antarkota secara terstruktur, informatif, dan ramah aksesibilitas.

### Struktur & Komponen Halaman
1. **Kepala Dokumen:**
   - Menyertakan atribut `lang="id"` pada elemen `<html>`.
   - Konfigurasi metadata standar: `<meta charset="UTF-8">`, `<meta name="viewport" content="width=device-width, initial-scale=1.0">`, dan `<title>Mengatur Jam Perjalanan - Profil Saya</title>`.
2. **Landmark Semantik & Hierarki Heading:**
   - Landmark lengkap: `<header>`, `<nav>`, `<main>`, dua `<section>`, dan `<footer>`.
   - Heading berurutan tanpa lompatan: satu `<h1>` utama di `<header>`, dilanjutkan dengan `<h2>` pada masing-masing `<section>`.
   - Navigasi internal menghubungkan tautan `#bagian-1`, `#bagian-2`, dan `#footer`.
3. **Tabel Data Terstruktur:**
   - Memuat `<caption>`, `<thead>`, dan `<tbody>`.
   - Memanfaatkan `<th scope="col">` untuk kepala kolom dan `<th scope="row">` untuk kepala baris.
   - Menyajikan 4 baris data perjalanan yang realistis dan bermakna.
4. **Media & Aksesibilitas Gambar:**
   - Menggunakan elemen semantik `<figure>` dan `<figcaption>`.
   - Gambar dilengkapi atribut `alt` deskriptif dalam Bahasa Indonesia serta dimensi eksplisit `width="640"` dan `height="360"` untuk mencegah layout shift, ditambah `loading="lazy"`.
5. **Formulir & Validasi Input:**
   - Semua input terhubung secara tepat dengan pasangannya melalui `<label for="...">` dan `id="..."`.
   - Menggunakan tipe data input yang tepat: `type="text"`, `type="date"`, dan `type="time"`.
   - Dilengkapi atribut validasi seperti `required` dan `minlength`.

---

### Hasil Pemeriksaan Mandiri & Audit Aksesibilitas
- **Lighthouse Accessibility Score:** **94 / 100**
- **Temuan Uji Otomatis:** 1 catatan minor WCAG `target-size` pada tautan daftar navigasi karena halaman belum menggunakan styling CSS (margin/padding sentuh akan diimplementasikan pada Pertemuan 4).
- **Uji Navigasi Keyboard (Tab):** Lancar, seluruh tautan dan kontrol formulir dapat difokuskan dan dioperasikan tanpa tetikus.
- **Uji Klik Label:** Seluruh teks label ketika diklik langsung memindahkan fokus kursor ke elemen input pasangannya.
- **Uji Loncat Navigasi:** Semua tautan navigasi melompat tepat ke elemen target yang dituju.

---

### Pengungkapan Penggunaan AI (AI Disclosure)
Sesuai dengan ketentuan integritas akademik pada Lembar G:
- **Bagian yang Dikerjakan Mandiri:**
  - Penentuan topik orisinal halaman ("Mengatur Jam Perjalanan").
  - Pengambilan dan penyiapan berkas gambar maskot perjalanan (`images.jpg`).
  - Penyusunan kerangka awal profil, data tabel rute perjalanan, dan rancangan isian formulir.
- **Bagian yang Dibantu AI:**
  - Audit kepatuhan standar semantik HTML5 dan rubrik penilaian (menemukan bahwa tag `<h1>` sebelumnya belum ada di `<header>` dan memperbaikinya).
  - Perbaikan kesalahan sintaks kecil (penghapusan karakter backtick tidak sengaja pada penutup tag `</form>` dan duplikasi tag penutup `</body>`).
  - Pemilihan tipe input waktu standar HTML5 (`type="time"`) untuk menggantikan `type="text"`.
  - Pelaksanaan pengujian aksesibilitas menggunakan audit Lighthouse.
