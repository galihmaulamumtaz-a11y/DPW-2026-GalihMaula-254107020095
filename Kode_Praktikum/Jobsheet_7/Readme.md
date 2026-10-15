## 👤 Identitas Mahasiswa

| Keterangan  | Detail |
| :---        | :--- |
| **Nama**    | Galih Maula Mumtaza |
| **Kelas**   | 2F/TI |
| **Absen**   | 16 |

---

## 🎯 Informasi Jobsheet

**Sub-CPMK**: Mengimplementasikan dasar PHP & pengolahan form.

### 📂 Isi Tahap Ini
- [`index.html`](./index.html) — Menampilkan halaman beranda utama beserta ringkasan statistik.
- [`buku/list.html`](./buku/list.html) — Menampilkan struktur tabel untuk daftar buku secara statis.
- [`buku/tambah.html`](./buku/tambah.html) — Menyediakan form input untuk menambahkan data buku baru.
- [`anggota/list.html`](./anggota/list.html) — Menampilkan struktur tabel untuk daftar anggota secara statis.
- [`anggota/tambah.html`](./anggota/tambah.html) — Menyediakan form input untuk mendaftarkan anggota baru.
- [`assets/css/style.css`](./Assets/css/style.css) — Baju buat HTML agar syntax atau halaman website menjadi lebih bagus.
- [`docs/wireframe.md`](./docs/wireframe.md) — Acuan struktur HTML 

## Perubahan dari Jobsheet 6
- Semua halaman `.html` diubah menjadi `.php`.
- Diperkenalkan `includes/header.php` & `includes/footer.php` untuk menghindari duplikasi navbar/footer di setiap halaman (dipakai lewat `include`).
- Path CSS/JS/menu memakai path **relatif** (`assets/css/style.css`, `index.php`, dst, tanpa awalan `/`), dihitung otomatis di `includes/header.php` berdasarkan kedalaman folder halaman yang sedang diakses (`$base` = `""` di root, `"../"` untuk halaman satu level ke dalam seperti `buku/`, `anggota/`). Jadi proyek ini tetap berjalan benar walau diakses dari root server (`php -S`) **maupun** lewat subfolder (mis. Laragon dengan document root di folder induk).
- `buku/tambah.php` & `anggota/tambah.php`: form kini `method="post"` mengarah ke `proses_tambah.php` masing-masing.
- `buku/proses_tambah.php` & `anggota/proses_tambah.php`: memvalidasi `$_POST` di server (validasi ini **terpisah** dari validasi JS di Jobsheet 5 — bisa berjalan sendiri walau JS dimatikan), lalu menyimpan sementara ke `$_SESSION['buku']` / `$_SESSION['anggota']` (array), redirect ke `list.php`.
- `buku/list.php` & `anggota/list.php`: tabel dirender dari `$_SESSION` via `foreach` (menggantikan pendekatan fetch/JSON di Jobsheet 6 — rendering utama sekarang di server).
- Flash message sukses/gagal ditampilkan lewat `$_SESSION['flash']`.
- File `assets/js/buku.js`, `assets/js/anggota.js`, dan folder `data/` dari Jobsheet 6 **dihapus** karena rendering sudah dipindah ke server-side PHP.

## Cara menjalankan
**Opsi 1 — PHP built-in server**, jalankan dari dalam folder `jobsheet-07/`:
```bash
php -S localhost:8000
```
Buka `http://localhost:8000/index.php`.

**Opsi 2 — Laragon (Apache)**: bisa lewat virtual host yang document root-nya langsung ke folder `jobsheet-07/` (mis. `http://jobsheet07.test/`), atau diakses bersarang di bawah domain proyek (mis. `http://dp2026.test/kode-praktikum/jobsheet-07/`) — dua-duanya jalan karena path CSS/JS/link sudah relatif otomatis (lihat catatan di atas).

## Catatan
- Data yang disimpan di `$_SESSION` akan hilang saat sesi browser berakhir — ini jembatan sementara. Mulai Jobsheet 8, penyimpanan dipindah ke PostgreSQL agar persisten.
- Coba nonaktifkan JavaScript di browser lalu submit form kosong: validasi server tetap mencegah data invalid tersimpan.