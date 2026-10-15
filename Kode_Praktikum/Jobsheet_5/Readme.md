## 👤 Identitas Mahasiswa

| Keterangan  | Detail |
| :---        | :--- |
| **Nama**    | Galih Maula Mumtaza |
| **Kelas**   | 2F/TI |
| **Absen**   | 16 |

---

## 🎯 Informasi Jobsheet

**Sub-CPMK**: Menerapkan manipulasi DOM & event JavaScript.

### 📂 Isi Tahap Ini
- [`index.html`](./index.html) — Menampilkan halaman beranda utama beserta ringkasan statistik.
- [`buku/list.html`](./buku/list.html) — Menampilkan struktur tabel untuk daftar buku secara statis.
- [`buku/tambah.html`](./buku/tambah.html) — Menyediakan form input untuk menambahkan data buku baru.
- [`anggota/list.html`](./anggota/list.html) — Menampilkan struktur tabel untuk daftar anggota secara statis.
- [`anggota/tambah.html`](./anggota/tambah.html) — Menyediakan form input untuk mendaftarkan anggota baru.
- [`assets/css/style.css`](./Assets/css/style.css) — Baju buat HTML agar syntax atau halaman website menjadi lebih bagus.
- [`docs/wireframe.md`](./docs/wireframe.md) — Acuan struktur HTML 

## Perubahan dari Jobsheet 4
- Tambah `assets/js/app.js`.
- Hamburger menu: checkbox hack (CSS) diganti tombol + JS (`nav.classList.toggle("nav-open")`).
- Form Tambah Buku & Tambah Anggota: validasi client-side (`initValidasiForm`) — field wajib, rentang tahun, stok non-negatif — pesan error tampil inline via manipulasi DOM (`insertAdjacentElement`).
- Tabel Daftar Buku & Daftar Anggota: kolom pencarian real-time (`initTableFilter`) yang menyaring baris via `keyup`.
- Tombol Hapus (`.btn-hapus`): menampilkan `confirm()` lalu menghapus baris dari tampilan (masih front-end saja, belum ke server).

## Cara menjalankan
Buka `index.html` di browser. Coba: submit form kosong (muncul error), ketik di kolom cari (tabel tersaring), klik Hapus (muncul konfirmasi).

## Catatan
- Validasi di sini murni client-side dan bisa dilewati (nonaktifkan JS). Validasi server-side ditambahkan di Jobsheet 7 sebagai lapisan kedua yang wajib.
- Hapus baris di jobsheet ini hanya menghilangkan dari tampilan (belum persisten) — akan diganti proses hapus sungguhan ke database mulai Jobsheet 9.