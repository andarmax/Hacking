# ANDARMAX ACADEMY — Lab

Lab simulasi berbasis web untuk belajar dasar ethical hacking / white hat.
Semua aktivitas berjalan di browser, di sistem simulasi internal.
Tidak ada sistem eksternal yang diakses, tidak ada data asli yang diproses.

## Cara Menjalankan

1. Clone atau unduh repository ini.
2. Buka `index.html` di browser, atau deploy via GitHub Pages.
3. Masuk dengan kredensial lab:


Kredensial ini hanya untuk membuka simulasi. Bukan akun nyata.

## Yang Dipelajari

Project ini terdiri dari 8 modul berurutan. Setiap modul menguji satu
kemampuan dasar pertahanan sistem.

| Modul | Topik | Yang Diuji |
| --- | --- | --- |
| 01 | Password | Mengukur entropi password: panjang, campuran karakter, tidak ada di daftar umum |
| 02 | Phishing | Mengenali pola link tidak resmi + permintaan OTP |
| 03 | Pemindaian Jaringan | Membaca hasil scan, mengidentifikasi port yang tidak perlu terbuka |
| 04 | Social Engineering | Menolak permintaan kredensial / OTP dari pihak lain |
| 05 | CTF: Flag | Menggunakan terminal untuk menemukan flag di lab |
| 06 | SQL Injection (Defensif) | Memilih perbaikan yang benar: prepared statement |
| 07 | XSS (Defensif) | Memilih perbaikan yang benar: escape output + CSP |
| 08 | Respons Insiden | Memperbaiki 3 temuan dalam 60 detik lewat terminal |

Total: **3000 XP**. Sertifikat penyelesaian terbuka setelah 8/8 modul selesai.

## Perintah Terminal

Terminal di dalam lab adalah simulasi. Perintah yang tersedia:


## Sertifikat

Setelah 3000 XP, sertifikat dapat dibuka lewat banner di atas terminal
atau perintah `certificate`, lalu dicetak / disimpan sebagai PDF
melalui dialog print browser.

Catatan penting: sertifikat ini menyatakan penyelesaian simulasi
pembelajaran. Bukan sertifikasi industri dan bukan lisensi untuk
mengakses sistem tanpa izin.


Tidak ada build step. Tidak ada dependensi. Tidak ada backend.
Satu file HTML bisa langsung dibuka.

## Batasan dan Etika

Project ini dibuat untuk belajar bertahan, bukan menyerang.

- Jangan gunakan pengetahuan dari lab ini untuk mengakses sistem
  milik orang lain tanpa izin tertulis dari pemilik sistem.
- Jangan meminta, membagikan, atau menyimpan OTP / password orang lain.
- Aktivitas ethical hacking yang sah selalu membutuhkan izin tertulis,
  ruang lingkup yang jelas, dan pelaporan yang bertanggung jawab.

Jika menemukan celah di sistem nyata, laporkan melalui jalur
responsible disclosure / bug bounty resmi pemilik sistem.

## Pengembangan

Untuk menambah modul baru, pola yang dipakai:

1. Tambah entri di array `missions` di `index.html`.
2. Tambah handler di `startMission()` dan di listener `cmdInput` jika
   modul membutuhkan perintah terminal.
3. Gunakan `addXP()` agar progres, level, dan sertifikat tetap konsisten.

Hindari menambahkan efek visual yang tidak menambah informasi.
Prioritas project ini: keterbacaan, kecepatan, dan penjelasan teknis
yang akurat.

## Lisensi

Bebas dipakai untuk belajar dan dimodifikasi untuk keperluan
pendidikan, selama penanda "SIMULASI — LAB LOKAL" tidak dihapus.

## Kontak

ANDARMAX ACADEMY — Yogyakarta

