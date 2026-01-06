---
title: "Menginstal Laravel: Bukan Soal Langkah, Tapi Konteks"
date: 2023-06-24
last_modified_at: 2023-06-24
categories:
  - Catatan
tags:
  - laravel
  - instalasi
  - pengembangan-aplikasi
  - sistem
  - praktik-kerja
---

Tulisan tentang instalasi Laravel biasanya dimulai dengan daftar command.  
`composer create-project`,  
atur `.env`,  
jalankan `php artisan serve`.

Semua itu benar.  
Dan semua itu mudah ditemukan.

Masalahnya, pengalaman di lapangan jarang gagal karena langkah instalasi.  
Ia gagal karena **konteks tidak pernah dibicarakan**.

<!--more-->

Saya pernah melihat Laravel “gagal” dipakai bukan karena framework-nya,  
tetapi karena lingkungan tempat ia dipasang tidak pernah disiapkan dengan sadar.

Instalasi dianggap urusan teknis belaka.  
Padahal ia adalah keputusan awal yang menentukan arah kerja.

Laravel datang dengan asumsi tertentu:  
ada Composer, ada struktur direktori, ada dependensi yang dikelola, ada kebiasaan dokumentasi.  
Semua itu masuk akal—jika lingkungannya siap.

Masalah muncul ketika Laravel dipasang di lingkungan yang tidak mendukung asumsi itu.  
Server seadanya.  
Versi PHP tidak jelas.  
Akses terbatas.  
Atau tim yang belum terbiasa membaca dokumentasi.

Di situ, proses instalasi menjadi awal dari friksi, bukan kemudahan.

---

Saya mulai melihat instalasi bukan sebagai “memulai proyek”,  
tetapi sebagai **menyetujui seperangkat konsekuensi**.

Menginstal Laravel berarti:
- menerima struktur yang lebih ketat
- menerima ketergantungan pada ekosistem
- menerima kebutuhan belajar yang berkelanjutan

Itu bukan hal buruk.  
Justru sering kali itulah yang dibutuhkan.

Namun, tidak semua proyek perlu itu sejak hari pertama.

Ada proyek yang butuh cepat hidup.  
Ada tim yang butuh kontrol penuh atas setiap baris kode.  
Ada konteks di mana kesederhanaan lebih penting daripada kelengkapan.

Dalam kondisi seperti itu, instalasi yang “berhasil” secara teknis  
bisa menjadi kegagalan secara operasional.

---

Sekarang, sebelum memasang Laravel, saya tidak lagi bertanya *“bagaimana caranya”*.  
Saya bertanya:

- Siapa yang akan merawat aplikasi ini enam bulan lagi?
- Seberapa sering sistem ini berubah?
- Seberapa siap lingkungan dan timnya?
- Apa risiko terbesar jika sesuatu rusak?

Jika jawabannya selaras dengan asumsi Laravel,  
instalasi biasanya berjalan mulus—bahkan membosankan.

Dan justru di situlah tandanya benar.

---

Menginstal Laravel bukan tentang mengikuti langkah.  
Ia tentang memahami konteks tempat langkah itu diambil.

Ketika konteksnya tepat,  
proses instalasi hanyalah menjadi todo-list.

Dan ketika konteksnya keliru,  
tidak ada command yang cukup untuk menyelamatkannya. Haha...
