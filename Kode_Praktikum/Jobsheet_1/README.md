## 👤 Identitas Mahasiswa

| Keterangan  | Detail |
| :---        | :--- |
| **Nama**    | Galih Maula Mumtaza |
| **Kelas**   | 2F/TI |
| **Absen**   | 16 |

---

## 🎯 Informasi Jobsheet

**Sub-CPMK:** Menyusun struktur halaman web dengan HTML5 semantic.

### 📂 Isi Tahap Ini
- [`index.html`](./index.html) — Menampilkan halaman beranda utama beserta ringkasan statistik.
- [`buku/list.html`](./buku/list.html) — Menampilkan struktur tabel untuk daftar buku secara statis.
- [`buku/tambah.html`](./buku/tambah.html) — Menyediakan form input untuk menambahkan data buku baru.
- [`anggota/list.html`](./anggota/list.html) — Menampilkan struktur tabel untuk daftar anggota secara statis.
- [`anggota/tambah.html`](./anggota/tambah.html) — Menyediakan form input untuk mendaftarkan anggota baru.

### 🚀 Cara Menjalankan
Buka `index.html` langsung di browser (belum butuh server).

### 📌 Catatan
> Belum ada CSS/JS — fokus murni pada struktur semantic (`<header>`, `<nav>`, `<main>`, `<section>`, `<article>`, `<footer>`) dan penamaan atribut `name`/`id` yang akan dipakai kembali di jobsheet berikutnya.

---

## 6.5 Latihan Reflektif

Sebagai latihan mandiri, coba bandingkan sendiri form ini dengan form
buku dan jawab pertanyaan berikut untuk menguji pemahaman:

**1. Kenapa field "Alamat" dan "No. HP" tidak diberi `required`, sedangkan "Nama" dan "No. Anggota" diberi?**

Field Nama dan No. Anggota diberi atribut required karena kedua data tersebut merupakan informasi utama yang diperlukan untuk mengidentifikasi anggota. Data tersebut harus diisi agar data anggota dapat dianggap lengkap.
Sementara itu, Alamat dan No. HP tidak diberi required karena kedua data tersebut bersifat opsional. Artinya, pengguna tetap dapat menyimpan data anggota meskipun alamat atau nomor HP belum tersedia.

**2. Apa yang akan terjadi (di browser) kalau kamu klik tombol "Simpan" tanpa mengisi field "Nama"? Coba buka filenya di browser dan praktikkan.**

Jika tombol Simpan diklik ketika field Nama masih kosong, browser akan melakukan validasi HTML karena field tersebut memiliki atribut required.
Browser akan menampilkan pesan bahwa field tersebut harus diisi dan proses pengiriman form tidak akan dilanjutkan sampai field Nama diisi.
Hal yang sama juga berlaku pada field No. Anggota karena field tersebut juga menggunakan atribut required.

**3. Form ini juga **belum punya `action`** pada tag `<form>`-nya — apa dampaknya saat tombol "Simpan" ditekan?**

Jika tag <form> tidak memiliki atribut action, browser secara default akan mengirimkan data form ke URL halaman yang sedang dibuka.

Lanjut ke: [Rangkuman & Latihan Lanjutan](07-rangkuman-latihan.md)