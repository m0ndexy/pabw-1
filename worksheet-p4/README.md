## Pertemuan 4 — Design token halaman profil

- Berkas gaya yang dibuat: tokens.css, base.css, layout.css, komponen.css, tema.css
- Warna utama: `#1D3A8C` (biru tua), dipilih karena memberikan kesan andal, tenang, dan kontras tinggi untuk informasi jadwal perjalanan.

### Token yang saya tetapkan

| Token | Nilai | Untuk apa |
|---|---|---|
| `--color-primary` | `#1D3A8C` | tombol, tautan, judul, dan penanda |
| `--color-fg` | `#0F172A` | warna teks utama |
| `--color-bg` | `#F8FAFC` | latar halaman |
| `--color-surface` | `#FFFFFF` | latar kartu dan panel |
| `--color-border` | `#D1D5DB` | garis pemisah tabel dan tepi kartu |
| `--color-danger` | `#B00020` | warna peringatan dan isian tidak sah |
| `--color-focus` | `#2563EB` | garis penanda fokus navigasi keyboard |
| `--radius-md` | `0.5rem` | sudut tombol, kolom isian, dan kartu |
| `--space-4` | `1rem` | jarak standar antar elemen |
| `--section-gap` | `1.5rem` | jarak antar bagian halaman |

**Kriteria selesai saya:** Mengubah `--blue-700` di satu baris pada `tokens.css` mengubah warna tombol, tautan, judul, dan garis fokus di seluruh halaman secara serentak.

## Catatan penggunaan AI

- **Bagian yang dibantu AI:** Penerapan arsitektur CSS 5 berkas berdasar lembar kerja (tokens, base, layout, komponen, tema), pengujian kontras WCAG AA untuk tema terang dan tema gelap, serta pengecekan selektor CSS (:has, :user-invalid).
