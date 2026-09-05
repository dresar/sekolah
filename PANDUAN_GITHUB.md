# Panduan Menyimpan Kode Aplikasi di GitHub

Panduan ini akan membantu Anda menyimpan kode aplikasi website sekolah dan PPDB online di GitHub.

## Persiapan Awal

### 1. Instal Git

- **Windows**: Download dan instal Git dari [git-scm.com](https://git-scm.com/download/win)
- **Linux**: Gunakan perintah `sudo apt-get install git` (Ubuntu/Debian) atau `sudo yum install git` (Fedora/CentOS)
- **Mac**: Instal menggunakan Homebrew dengan perintah `brew install git`

### 2. Buat Akun GitHub

- Kunjungi [github.com](https://github.com) dan daftar untuk membuat akun baru
- Verifikasi email Anda setelah pendaftaran

## Langkah-Langkah Menyimpan Kode di GitHub

### 1. Buat Repository Baru di GitHub

1. Login ke akun GitHub Anda
2. Klik tombol "+" di pojok kanan atas, lalu pilih "New repository"
3. Isi nama repository (misalnya: "website-sekolah-ppdb")
4. Tambahkan deskripsi (opsional): "Aplikasi Website Sekolah dan PPDB Online"
5. Pilih "Public" atau "Private" sesuai kebutuhan
6. Jangan centang opsi "Initialize this repository with a README"
7. Klik "Create repository"

### 2. Inisialisasi Git di Folder Proyek

1. Buka Command Prompt (CMD) atau PowerShell
2. Arahkan ke folder proyek Anda dengan perintah:
   ```
   cd "c:\codingan ku\APLIKASI WEBSITE SEKOLAH DAN PPDB ONLINE-20250318T211200Z-001\APLIKASI WEBSITE SEKOLAH DAN PPDB ONLINE\sekolah"
   ```
3. Inisialisasi Git repository dengan perintah:
   ```
   git init
   ```

### 3. Tambahkan File .gitignore (Opsional tapi Direkomendasikan)

Buat file `.gitignore` untuk mengabaikan file-file yang tidak perlu disimpan di GitHub:

```
# File sistem operasi
.DS_Store
Thumbs.db

# File konfigurasi yang mungkin berisi informasi sensitif
application/config/database.php

# File cache dan temporary
application/cache/*
!application/cache/index.html
!application/cache/.htaccess

# File log
application/logs/*
!application/logs/index.html
!application/logs/.htaccess
error_log

# File media yang diupload user (jika ada)
media_library/files/*
media_library/images/*
!media_library/files/index.html
!media_library/images/index.html

# Folder vendor jika menggunakan composer
vendor/
```

### 4. Tambahkan File ke Staging Area

```
git add .
```

Perintah ini akan menambahkan semua file (kecuali yang disebutkan dalam .gitignore) ke staging area.

### 5. Commit Perubahan

```
git commit -m "Initial commit: Aplikasi Website Sekolah dan PPDB Online"
```

### 6. Hubungkan dengan Repository GitHub

Ganti `username` dengan username GitHub Anda dan `repository-name` dengan nama repository yang telah Anda buat:

```
git remote add origin https://github.com/username/repository-name.git
```

### 7. Upload Kode ke GitHub

```
git push -u origin master
```

Jika Anda menggunakan Git versi terbaru, mungkin perlu menggunakan:

```
git push -u origin main
```

## Mengelola Perubahan Selanjutnya

Setelah melakukan perubahan pada kode, ikuti langkah-langkah berikut untuk menyimpan perubahan ke GitHub:

1. Tambahkan file yang diubah ke staging area:
   ```
   git add .
   ```

2. Commit perubahan dengan pesan yang jelas:
   ```
   git commit -m "Pesan yang menjelaskan perubahan"
   ```

3. Upload perubahan ke GitHub:
   ```
   git push origin master
   ```

## Tips Tambahan

### Melihat Status Perubahan

```
git status
```

### Melihat Riwayat Commit

```
git log
```

### Membuat Branch Baru

```
git checkout -b nama-branch-baru
```

### Beralih Antar Branch

```
git checkout nama-branch
```

### Menggabungkan Branch

```
git checkout master
git merge nama-branch
```

## Kesimpulan

Dengan mengikuti panduan ini, Anda telah berhasil menyimpan kode aplikasi website sekolah dan PPDB online di GitHub. Hal ini memungkinkan Anda untuk:

1. Melacak perubahan pada kode
2. Berkolaborasi dengan pengembang lain
3. Memiliki backup kode yang aman
4. Mengelola versi aplikasi dengan lebih baik

Selamat mencoba dan semoga berhasil!