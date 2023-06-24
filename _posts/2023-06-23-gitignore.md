---
title: "Git: .gitignore"
last_modified_at: 2023-06-23T16:20:02-05:00
categories:
  - Blog
  - Git
tags:
  - gitignore
  - readability
  - standard
---

Git merupakan sebuah alat yang istimewa, digunakan untuk melacak perubahan dengan cara memiliki riwayat versi-versi perubahan dari file-file dalam proyek kita ketika melakukan kolaborasi dalam proses software development.

Hampir semua proyek yang kita telah buat ada file `.gitignore`. ini sebenarnya berisi nama-nama file yang akan diabaikan oleh proses-proses Git sehingga tidak akan terlacak oleh Git. Hanya saja, jika kita terlambat menyertakan file `.gitignore` ini atau mungkin kita ingin memperbarui file `.gitignore` agar bisa menghapus file tertentu dari repository, terkadang Git tidak langsung me-refleksikannya, Gimana dong? Kita harus menerapkan `.gitignore` itu lagi.

Dalam artikel kali ini, akan ditunjukkan bagaimana caranya menerapkan `.gitignore` lagi dalam repository proyek kita - maka pastikan setiap perubahan diterapkan ya!

## Menghapus semua file dari Git index

Git menyimpan masing-masing status dari file-file kita dalam sebuah index. Setiap file yang kita kecualikan dengan menuliskan file tersebut pada file `.gitignore`, tidak akan ditambahkan kedalam index tersebut. Namun bagaimana jika file tersebut sudah ada terlebih dulu dalam index? Agar bisa menerapkan aturan `.gitignore` maka kita harus menghapus dulu index tersebut lalu mengisinya lagi.

Menghapus index ini bisa kita lakukan dengan menjalankan command berikut ini. Sangat disarankan memulai dengan direktori yang bersih, jadi sebelum menjalankan command ini lakukan commit atau abaikan perubahan-perubahan, supaya aman.