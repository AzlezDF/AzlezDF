# Panduan Setup GitHub Profile

## 1. Siapkan repository profil

1. Pastikan repository ini **publik** dan namanya persis `AzlezDF` (sama dengan username GitHub).
2. Push `README.md`, `.github/workflows/snake.yml`, dan `SETUP.md` ke branch `main`.
3. Buka halaman profil GitHub untuk melihat README. Perubahan biasanya tampil dalam beberapa saat.

## 2. Aktifkan contribution snake

1. Buka tab **Actions** pada repository `AzlezDF/AzlezDF`.
2. Jika GitHub meminta persetujuan, aktifkan workflow.
3. Pilih workflow **Generate contribution snake**, lalu klik **Run workflow** dan jalankan pada branch `main`.
4. Setelah proses sukses, workflow membuat atau memperbarui branch `output` yang berisi `github-snake.svg` dan `github-snake-dark.svg`.
5. Muat ulang halaman profil. Animasi akan muncul setelah file di branch `output` tersedia.

Workflow juga berjalan otomatis setiap 12 jam dan setiap ada push ke `main`. Ia memakai `GITHUB_TOKEN` bawaan GitHub Actions, sehingga Anda tidak perlu membuat atau menyimpan personal access token.

## 3. Personalisasi README

- Ganti bagian **About Me** agar sesuai dengan cerita dan target belajar Anda.
- Pada bagian **Featured Projects**, ganti nama/link/deskripsi/stack/status placeholder dengan repository nyata.
- Di bagian **Connect With Me**, hilangkan komentar HTML hanya untuk tautan yang benar-benar dipakai, kemudian ganti `USERNAME`, `EMAIL`, atau URL contoh. Jangan tampilkan tautan kosong.
- Hapus platform latihan yang tidak digunakan dan tambahkan yang memang digunakan.

## Catatan GitHub Stats

Gambar statistik menggunakan instance publik `github-readme-stats.vercel.app`. Instance publik dapat terkena rate limit, lambat, atau sementara tidak tampil karena dipakai banyak orang. Jika ingin lebih stabil, fork proyek [github-readme-stats](https://github.com/anuraghazra/github-readme-stats), deploy fork tersebut di Vercel, lalu ganti domain `github-readme-stats.vercel.app` pada `README.md` dengan domain deployment Vercel Anda.

Untuk konfigurasi Vercel, ikuti petunjuk deployment pada repository proyek tersebut. Hindari menaruh token, kredensial, IP, atau data sensitif apa pun di README maupun repository publik.
