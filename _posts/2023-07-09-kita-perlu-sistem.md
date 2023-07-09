---
title: "Software Engineer: Kita Perlu Sistem"
last_modified_at: 2023-7-09T08:20:02-05:00
categories:
  - Blog
  - Git
tags:
  - software enginner
  - produktifitas
---

Para Software Engineer diharapkan untuk mengerjakan pekerjaan dengan super cepat dalam dunia development yang berkembang pesat ini.

Jujur saja, memang jelas kompetisi di luar sana sangat sengit. Kita harus muncul dengan tegap dan gagah. Salah satunya adalah menunjukkan kualitas kerja yang tinggi.

Salah satu cara memproduksi kerjaan yang konsisten adalah dengan membuat sebuah sistem untuk produktifitas yang termasuk di dalamnya mengedepankan tugas dan menghilangkan gangguan walhasil kita bisa fokus pada hal yang sebenarnya harus dikerjakan dan mengerjakannya dengan baik.

Lalu? Ulangi.

<!--more-->
Hampir semua proyek yang kita telah buat ada file `.gitignore`. ini sebenarnya berisi nama-nama file yang akan diabaikan oleh proses-proses Git sehingga tidak akan terlacak oleh Git. Hanya saja, jika kita terlambat menyertakan file `.gitignore` ini atau mungkin kita ingin memperbarui file `.gitignore` agar bisa menghapus file tertentu dari repository, terkadang Git tidak langsung me-refleksikannya, Gimana dong? Kita harus menerapkan `.gitignore` itu lagi.

Dalam artikel kali ini, akan ditunjukkan bagaimana caranya menerapkan `.gitignore` lagi dalam repository proyek kita - maka pastikan setiap perubahan diterapkan ya!

## Menghapus semua file dari Git index

Git menyimpan masing-masing status dari file-file kita dalam sebuah index. Setiap file yang kita kecualikan dengan menuliskan file tersebut pada file `.gitignore`, tidak akan ditambahkan kedalam index tersebut. Namun bagaimana jika file tersebut sudah ada terlebih dulu dalam index? Agar bisa menerapkan aturan `.gitignore` maka kita harus menghapus dulu index tersebut lalu mengisinya lagi.

Menghapus index ini bisa kita lakukan dengan menjalankan command berikut ini. Sangat disarankan memulai dengan direktori yang bersih, jadi sebelum menjalankan command ini lakukan commit atau abaikan perubahan-perubahan, supaya aman.

```bash
git rm -r --cached .
```

Setelah dijalankan akan terlihat banyak baris (asumsi bahwa ini repository yang aktif) seperti berikut ini,
```bash
rm 'nama_folder/nama_file.php'
rm 'nama_folder/nama_file_2.php'
...
```