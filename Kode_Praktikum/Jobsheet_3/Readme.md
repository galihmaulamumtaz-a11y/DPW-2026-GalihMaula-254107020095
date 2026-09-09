## 👤 Identitas Mahasiswa

| Keterangan  | Detail |
| :---        | :--- |
| **Nama**    | Galih Maula Mumtaza |
| **Kelas**   | 2F/TI |
| **Absen**   | 16 |

---

## 🎯 Informasi Jobsheet

**Sub-CPMK**: Membangun tampilan responsif.

### 📂 Isi Tahap Ini
- [`index.html`](./index.html) — Menampilkan halaman beranda utama beserta ringkasan statistik.
- [`buku/list.html`](./buku/list.html) — Menampilkan struktur tabel untuk daftar buku secara statis.
- [`buku/tambah.html`](./buku/tambah.html) — Menyediakan form input untuk menambahkan data buku baru.
- [`anggota/list.html`](./anggota/list.html) — Menampilkan struktur tabel untuk daftar anggota secara statis.
- [`anggota/tambah.html`](./anggota/tambah.html) — Menyediakan form input untuk mendaftarkan anggota baru.
- [`assets/css/style.css`](./Assets/css/style.css) — Baju buat HTML agar syntax atau halaman website menjadi lebih bagus.

## Perubahan dari Jobsheet 2
- Tambah `<meta name="viewport">` di semua halaman.
- Navbar: hamburger menu memakai teknik **checkbox hack** murni CSS (`input[type=checkbox] + label`), aktif di layar ≤480px.
- Tabel dibungkus `<div class="table-responsive">` agar bisa di-scroll horizontal di layar sempit.
- Tambah media query di `style.css`: grid kartu statistik 3 → 2 → 1 kolom mengikuti breakpoint tablet/mobile.

## Cara menjalankan
Buka `index.html` di browser, uji dengan DevTools responsive mode pada 3 breakpoint (mobile ≤480px, tablet ~768px, desktop ≥1024px).

## Catatan
- Hamburger di jobsheet ini masih murni CSS (checkbox hack). Di Jobsheet 5 akan diganti dengan toggle berbasis JavaScript.