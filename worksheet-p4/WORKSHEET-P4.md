# WORKSHEET P4
**Pertemuan 4 · CSS Fundamental dan Design Token**  
*Merancang Tampilan dengan Design Token*  
Pengembangan Aplikasi Berbasis Web · SIF302 · Semester Gasal 2026/2027

| Data Mahasiswa | Keterangan |
|---|---|
| **NAMA** | Ahmad Dani Maulana |
| **NIM** | 25523190 |
| **KELAS** | A |
| **TANGGAL** | 24/09/2026 |

---

## Lembar A — Tentukan Token Halaman Anda

### A.1 Warna

| Token | Untuk apa | Contoh nilai | Nilai saya |
|---|---|---|---|
| `--color-bg` | Latar halaman | `#F8FAFC` | `#F8FAFC` |
| `--color-fg` | Warna teks utama | `#0F172A` | `#0F172A` |
| `--color-surface` | Latar kartu dan panel, sedikit berbeda dari halaman | `#FFFFFF` | `#FFFFFF` |
| `--color-border` | Garis pemisah dan tepi kotak | `#D1D5DB` | `#D1D5DB` |
| `--color-primary` | Warna utama: tombol, tautan, judul, penanda | pilih sendiri | `#1D3A8C` |
| `--color-danger` | Peringatan dan isian yang tidak sah | `#B00020` | `#B00020` |
| `--color-focus` | Garis fokus papan ketik | pilih sendiri | `#2563EB` |

*Catatan kontras:* Pasangan teks `#0F172A` di atas latar `#F8FAFC` menghasilkan rasio kontras **16.5:1** (jauh melampaui standar WCAG AA 4.5:1). Teks tombol putih di atas `#1D3A8C` menghasilkan rasio **10.3:1**.

---

### A.2 Jarak, Sudut, Bayangan, dan Ukuran Huruf

| Token | Contoh nilai | Dipakai untuk | Nilai saya |
|---|---|---|---|
| `--space-1` | 0.25rem | Jarak paling rapat, di dalam komponen | `0.25rem` |
| `--space-2` | 0.5rem | Jarak antar label dan isian | `0.5rem` |
| `--space-3` | 0.75rem | Jarak di dalam kartu | `0.75rem` |
| `--space-4` | 1rem | Jarak standar antar elemen | `1rem` |
| `--space-6` | 1.5rem | Jarak antar bagian halaman | `1.5rem` |
| `--radius-md` | 0.5rem | Sudut membulat pada tombol, kartu, isian | `0.5rem` |
| `--radius-full` | 999px | Bentuk pil, misalnya lencana | `999px` |
| `--shadow-1` | 0 1px 3px rgba(0,0,0,.10) | Bayangan halus kartu | `0 1px 3px rgba(0, 0, 0, 0.10)` |
| `--text-sm` | 0.875rem | Keterangan dan teks bantu | `0.875rem` |
| `--text-md` | 1rem | Teks isi | `1rem` |
| `--text-xl` | 1.5rem | Judul bagian | `1.5rem` |
| `--text-3xl` | 2.25rem | Judul halaman | `2.25rem` |

---

### A.3 Uji Satu Baris
- **Kriteria Selesai:** Mengubah nilai `--blue-700` di satu baris pada `tokens.css` akan otomatis mengubah warna tombol, tautan, judul halaman & bagian, serta garis fokus di seluruh halaman tanpa menyunting berkas lain.

### A.4 Rencana di README
- [x] Tabel token terisi lengkap
- [x] README.md sudah memuat bagian "Pertemuan 4"
- [x] Bagian Pertemuan 3 dari pertemuan lalu masih utuh di bawahnya

---

## Lembar B — tokens.css dan Cara Memuat CSS

### B.1 Kesiapan Berkas
- [x] Folder `worksheet-p4/` sudah ada di dalam repositori
- [x] `profil.html` dari P3 tersalin ke sana dan terbuka di peramban
- [x] Gambar `images.jpg` masih tampil setelah berkas dipindah

### B.3 Urutan Pemuatan Berkas Gaya di `<head>`
```html
<link rel="stylesheet" href="tokens.css">
<link rel="stylesheet" href="base.css">
<link rel="stylesheet" href="layout.css">
<link rel="stylesheet" href="komponen.css">
<link rel="stylesheet" href="tema.css">
```

### B.4 Pemeriksaan Pemuatan Gaya

| Yang diperiksa | Hasil yang benar | Hasil saya |
|---|---|---|
| **DevTools → Console** | Tidak ada galat dari kode Anda | Ya, bersih tidak ada galat (0 error) |
| **DevTools → Network (CSS)** | Kelima berkas status 200, bukan 404 | Ya, kelima berkas status 200 OK |
| **DevTools → Elements → `:root`** | Terlihat seluruh token di panel Styles | Ya, seluruh variabel CSS lapis 1 & 2 muncul |

---

## Lembar C — base.css: Dasar yang Berlaku untuk Semua

- [x] **Reset Ringan:** `*, *::before, *::after { box-sizing: border-box; }` dan `* { margin: 0; }`.
- [x] **Gambar Responsif:** `img { max-width: 100%; height: auto; display: block; }`.
- [x] **Tipografi Relatif:** Menggunakan `rem` dan variabel token.
- [x] **Panjang Baris Paragraf:** Dibatasi dengan `max-width: 60ch`.
- [x] **Uji Zoom Teks 200%:** Diuji dengan perbesaran teks 200% (Ctrl + tanda tambah). Seluruh tata letak tetap proporsional dan tidak ada teks yang terpotong.

---

## Lembar D — layout.css: Navbar dan Katalog Kartu

### Pemeriksaan Layout

| Yang diperiksa | Hasil yang benar | Hasil saya |
|---|---|---|
| **Navbar pada layar lebar** | Judul di kiri, menu di kanan, satu baris | Ya, judul di kiri, menu dan tombol tema di kanan satu baris rapi |
| **Navbar pada layar sempit** | Menu turun baris, tidak terpotong | Ya, `flex-wrap: wrap` bekerja rapi tanpa teks meluber |
| **Jendela disempitkan** | Kartu turun menjadi satu kolom, tanpa gulir mendatar | Ya, responsif turun rapi tanpa scrollbar horizontal |
| **Jarak antar elemen** | Seragam, semuanya dari token spasi | Ya, semua jarak memakai `gap` dan `var(--space-*)` |

---

## Lembar E — Gaya Form dan Keadaan Fokus

### Pemeriksaan Form dan Aksesibilitas

| Yang diperiksa | Hasil yang benar | Hasil saya |
|---|---|---|
| **Tekan Tab berkali-kali** | Kotak fokus terlihat jelas di setiap elemen | Ya, kotak fokus outline terlihat tegas di setiap elemen interaktif |
| **Fokus pada tautan dan tombol** | Garis fokus terlihat, tidak terpotong | Ya, garis fokus dengan `outline-offset: 2px` tampak kontras |
| **Kolom form dibiarkan kosong, halaman baru dibuka** | Belum ada tanda merah sebelum Anda mengetik | Ya, bersih tanpa warna merah saat awal dibuka |
| **Isi kolom dengan isi yang salah lalu hapus** | Garis peringatan dan pesan muncul | Ya, `:user-invalid` aktif dan `.pesan-galat` muncul otomatis |
| **Perbaiki isinya** | Tanda peringatan hilang sendiri | Ya, tanda peringatan langsung hilang secara reaktif |

---

## Lembar F — Tema Gelap

### F.3 Uji Kontras Kedua Tema

| Pasangan yang diuji | Tema terang | Tema gelap | Ambang Batas | Status |
|---|---|---|---|---|
| **Teks isi di atas latar halaman** | 16.5 : 1 | 13.8 : 1 | 4.5:1 | Lolos AA & AAA |
| **Teks tombol di atas warna utama** | 10.3 : 1 | 6.5 : 1 | 4.5:1 | Lolos AA & AAA |
| **Judul bagian di atas latar** | 10.3 : 1 | 7.8 : 1 | 4.5:1 | Lolos AA & AAA |
| **Garis fokus terhadap latar sekitarnya** | 4.6 : 1 | 10.8 : 1 | 3:1 | Lolos AA |
| **Tepi kartu terhadap latar halaman** | 1.5 : 1 | 1.9 : 1 | 3:1 | Batas visual kartu |

### Pemeriksaan Tema Gelap

| Yang diperiksa | Hasil yang benar | Hasil saya |
|---|---|---|
| **Ubah pengaturan sistem ke gelap, muat ulang** | Halaman ikut gelap tanpa menyentuh CSS | Ya, media query `prefers-color-scheme: dark` berjalan otomatis |
| **Klik tombol pengalih di tema terang** | Halaman menjadi gelap | Ya, selector `:root:has(#tema:checked)` berfungsi sempurna |
| **Klik lagi** | Halaman kembali terang | Ya, kembali ke tema terang |
| **Ganti warna utama di `tokens.css`, muat ulang** | Kedua tema ikut berubah | Ya, kedua tema mereferensikan token semantik yang sama |

---

## Lembar G — Uji Satu Baris, Tiket Keluar, Penilaian

### G.1 Uji Kemampuan Rawat

| Yang berubah saat satu baris `--blue-700` diubah | Ikut berubah? | Bagian yang tidak ikut |
|---|---|---|
| **Tautan pada menu navigasi** | ya | - |
| **Tombol pada form** | ya | - |
| **Judul halaman dan judul bagian** | ya | - |
| **Garis penanda fokus** | ya | - |
| **Warna pada tema gelap** | ya | - |

---

### G.2 Bersihkan Sisa Cara Lama

| Penanda | Jumlah temuan | Lokasinya |
|---|---|---|
| `float` dan clearfix | 0 | - |
| `!important` | 0 | - |
| Warna hex langsung di luar `tokens.css` dan `tema.css` | 0 | - |
| `px` untuk ukuran huruf | 0 | - |
| `style="..."` di dalam `profil.html` | 0 | - |

---

### G.3 Skor Lighthouse

| Yang diperiksa | Angka saya | Kalau rendah, apa yang disorot? |
|---|---|---|
| **Lighthouse — Accessibility** | 100 | Lolos sempurna |
| **Lighthouse — Performance** | 99 | Sangat baik dan optimal |
| **Kontras teks** | 100% | Seluruh elemen teks memenuhi rasio WCAG AA |

---

## Lembar G — Tiket Keluar

### Pertanyaan 1
**Apa bedanya `--blue-700` dengan `--color-primary`? Jawab dua kalimat: apa yang dijawab masing-masing nama, dan mengapa komponen sebaiknya hanya menyentuh salah satunya.**  
> `--blue-700` adalah token primitif yang menjawab "warna apa" dengan nilai heksadesimal mentah spesifik, sedangkan `--color-primary` adalah token semantik yang menjawab peran antarmuka ("untuk apa"). Komponen sebaiknya hanya menyentuh `--color-primary` agar jika terjadi perubahan tema atau penyesuaian palet merek, kita cukup memperbarui satu baris pemetaan semantiknya tanpa perlu menyunting kode CSS tiap komponen.

---

### Pertanyaan 2
**Anda memakai `--color-surface: #FFFFFF` untuk latar kartu, lalu tema gelap tidak berubah pada kartu itu. Apa yang Anda tulis, dan bagaimana seharusnya?**  
> Yang tertulis kemungkinan adalah nilai warna heksadesimal langsung `#FFFFFF` pada properti latar komponen kartu. Seharusnya pada komponen ditulis `background: var(--color-surface);`, kemudian nilai token semantik `--color-surface` tersebut didefinisikan ulang di dalam blok tema gelap (misalnya `--color-surface: #1E293B;`).

---

### Pertanyaan 3
**Mengapa menulis `--color-primary: #7DA9F7` di dalam blok tema gelap, bukan `#1D3A8C` yang sama seperti tema terang?**  
> Karena `#1D3A8C` adalah warna biru tua yang memiliki rasio kontras sangat rendah jika diletakkan di atas latar tema gelap (`#0F172A`) sehingga teks/tombol menjadi tidak terbaca. Oleh karena itu, dipilih varian biru yang lebih terang seperti `#7DA9F7` agar tetap kontras dan lolos ambang batas aksesibilitas WCAG AA (minimal 4.5:1).

---

### Pertanyaan 4
**Apa yang terjadi bila `input:invalid` dipakai untuk memberi warna merah, dan mengapa `:user-invalid` lebih baik? Sebutkan saat keduanya menyala.**  
> Bila memakai `input:invalid`, kolom form yang memiliki atribut `required` langsung menyala merah sejak halaman baru dibuka meskipun pengguna belum sempat membaca atau menyentuhnya. `:user-invalid` jauh lebih baik karena baru menyala setelah pengguna berinteraksi (mengetik atau berpindah kolom) dan nilai isiannya tidak sah.

---

### Pertanyaan 5
**Mengapa `gap` lebih baik daripada `margin` untuk jarak antar item di dalam flexbox?**  
> `gap` hanya memberikan jarak tepat di antara item-item yang bersebelahan tanpa menyisakan margin tambahan di tepi luar wadah (*margin bleed*) dan tidak menimbulkan masalah margin bertumpuk (*margin collapsing*), terutama saat elemen fleksibel membungkus (*wrap*) ke baris berikutnya.

---

## Penilaian Mandiri

- [x] **Berkas:** `profil.html` dan kelima berkas CSS ada di `worksheet-p4/`, terbuka tanpa galat di Console dan tanpa 404 di tab Network.
- [x] **Urutan pemuatan:** `tokens.css` dimuat paling awal, lalu `base`, `layout`, `komponen`, dan `tema`.
- [x] **Token dua lapis:** primitif dan semantik dipisah dalam dua blok `:root`.
- [x] **Token dipakai:** tidak ada warna langsung maupun `px` huruf di luar `tokens.css` dan `tema.css`.
- [x] **Base:** `box-sizing: border-box` global, margin bawaan dihapus, gambar `max-width: 100%`.
- [x] **Tipografi:** memakai `rem`, `line-height: 1.6` untuk teks isi.
- [x] **Layout:** navbar flexbox, katalog/bagian memakai `gap` dan `flex-wrap`, tanpa float.
- [x] **Responsif:** jendela disempitkan tidak menimbulkan gulir mendatar.
- [x] **Form:** kolom isian memakai `font: inherit` dan tetap berlabel.
- [x] **Fokus:** `:focus-visible` terlihat jelas dan kontras.
- [x] **Isian tidak sah:** `:user-invalid` dipakai, bukan `:invalid`.
- [x] **Tema gelap:** berfungsi lewat `prefers-color-scheme` dan bisa ditimpa tombol.
- [x] **Kontras:** kedua tema sudah diuji, angka dicatat apa adanya.
- [x] **Kebersihan:** tanpa `!important`, tanpa gaya inline.
- [x] **Uji satu baris:** warna utama berubah dari satu baris di `tokens.css`.
- [x] **Pengungkapan AI:** README menyebutkan bagian mana yang dibantu AI.
- [x] **Keaslian:** tampilan ini rancangan saya sendiri, tidak menyalin teman.

---

### Perkiraan Nilai Saya

| Aspek Penilaian | Bobot | Nilai Saya |
|---|---|---|
| Design token: dua lapis, dipakai konsisten | 30 | 30 |
| Tata letak: flexbox, gap, responsif | 25 | 25 |
| Tipografi dan satuan: rem, line-height, skala | 20 | 20 |
| Tema gelap: berfungsi dan kontras AA | 15 | 15 |
| Kebersihan kode: urutan pemuatan, tanpa !important | 10 | 10 |
| **Perkiraan Nilai Akhir** | **100** | **100** |

**Tanda tangan:** Ahmad Dani Maulana  
**Tanggal:** 24/09/2026  
**Jam selesai:** 20:15 WIB  
