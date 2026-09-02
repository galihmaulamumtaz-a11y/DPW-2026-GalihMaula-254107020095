## 👤 Identitas Mahasiswa

| Keterangan  | Detail |
| :---        | :--- |
| **Nama**    | Galih Maula Mumtaza |
| **Kelas**   | 2F/TI |
| **Absen**   | 16 |

---

## 🎯 Informasi Jobsheet

**Sub-CPMK**: Mengimplementasikan styling dasar dengan CSS3.

### 📂 Isi Tahap Ini
- [`index.html`](./index.html) — Menampilkan halaman beranda utama beserta ringkasan statistik.
- [`buku/list.html`](./buku/list.html) — Menampilkan struktur tabel untuk daftar buku secara statis.
- [`buku/tambah.html`](./buku/tambah.html) — Menyediakan form input untuk menambahkan data buku baru.
- [`anggota/list.html`](./anggota/list.html) — Menampilkan struktur tabel untuk daftar anggota secara statis.
- [`anggota/tambah.html`](./anggota/tambah.html) — Menyediakan form input untuk mendaftarkan anggota baru.
- [`assets/css/style.css`](./Assets/css/style.css) — Baju buat HTML agar syntax atau halaman website menjadi lebih bagus.

## Perubahan dari Jobsheet 1
- Tambah `assets/css/style.css` (box model, Flexbox untuk navbar, CSS Grid untuk kartu statistik Beranda).
- Semua halaman `.html` ditambahkan `<link rel="stylesheet">` ke `style.css` (path relatif menyesuaikan kedalaman folder).
- Struktur HTML **tidak diubah** — hanya tampilan.

## Cara menjalankan
Buka `index.html` langsung di browser.

## Catatan
- Kartu statistik di Beranda memakai `main section:nth-of-type(2)` sebagai grid 3 kolom.
- Class CSS bersifat generik (berbasis tag semantic + `nth-child`) agar bisa dipakai ulang di halaman Anggota tanpa duplikasi class.