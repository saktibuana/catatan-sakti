---
title: "Git: Memahami dan Menggunakan .gitignore dengan Benar"
date: 2023-06-23
last_modified_at: 2023-06-23T16:20:02-05:00
categories:
  - Blog
  - Git
tags:
  - gitignore
  - readability
  - standard
  - git
  - gitignore
  - version-control
  - tutorial
---

Hampir semua proyek yang menggunakan Git akan memiliki berkas bernama `.gitignore`.
Namun cukup banyak pengembang yang menggunakannya tanpa benar-benar memahami cara kerjanya.

Padahal, `.gitignore` berperan penting dalam menjaga repositori tetap bersih, konsisten, dan mudah dikelola.

<!--more-->

## Apa itu `.gitignore`

`.gitignore` adalah berkas konfigurasi yang memberi tahu Git **file atau folder apa saja yang tidak perlu dilacak**.

File yang diabaikan biasanya:
- hasil build
- dependensi
- file konfigurasi lokal
- file sementara
- artefak dari editor atau OS

Tujuannya sederhana:
**hanya hal yang relevan dengan kode sumber yang masuk ke repositori.**

---

## Contoh sederhana `.gitignore`

Berikut contoh `.gitignore` yang umum digunakan pada proyek PHP:

```gitignore
/vendor/
/node_modules/
.env
.env.*
*.log
````

Artinya:

* `/vendor/` dan `/node_modules/` tidak dilacak
* semua file `.env` diabaikan
* semua file `.log` diabaikan

---

## Kenapa `.gitignore` penting

Tanpa `.gitignore`, repositori akan cepat dipenuhi oleh:

* file yang hanya berlaku di satu mesin
* konfigurasi sensitif
* hasil kompilasi atau build

Akibatnya:

* ukuran repo membesar
* perubahan sulit dilacak
* konflik tidak perlu sering terjadi

`.gitignore` membantu menjaga fokus Git pada **kode yang benar-benar perlu dikontrol versinya**.

---

## Kesalahan umum saat menggunakan `.gitignore`

### 1. File sudah terlanjur ter-commit

`.gitignore` **tidak berlaku untuk file yang sudah pernah di-commit**.

Jika file sudah terlanjur masuk ke repositori, jalankan:

```bash
git rm --cached nama_file
git commit -m "Remove tracked file and apply gitignore"
```

---

### 2. Mengabaikan terlalu banyak hal

Mengabaikan file penting demi “repositori bersih” bisa berbahaya.

Pastikan:

* file konfigurasi contoh (`.env.example`) tetap di-commit
* dokumentasi setup tetap tersedia

---

### 3. `.gitignore` tidak konsisten antar tim

Setiap anggota tim seharusnya menggunakan `.gitignore` yang sama.

Solusinya:

* simpan `.gitignore` di root project
* review setiap perubahan `.gitignore` seperti kode biasa

---

## Pola `.gitignore` yang sering dipakai

```gitignore
# OS
.DS_Store
Thumbs.db

# Editor
.vscode/
.idea/

# Logs
*.log

# Cache
*.cache
```

Komentar (`#`) membantu menjelaskan tujuan setiap bagian, terutama dalam tim.

---

## Kapan `.gitignore` dibuat

Idealnya:

* **sebelum commit pertama**

Dengan begitu:

* tidak ada file “salah masuk”
* histori Git tetap bersih
* aturan sudah jelas sejak awal

---

## Penutup

`.gitignore` bukan fitur tambahan.
Ia bagian dari kebiasaan kerja yang rapi.

Dengan memahami dan menggunakannya dengan benar,
Git akan bekerja sebagaimana mestinya:
mencatat perubahan penting, tanpa terganggu oleh hal-hal yang seharusnya tidak ikut dicatat.
