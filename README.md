# ANDARLAB

Lab simulasi *penetration testing*, analisis log insiden, dan remediasi kerentanan berbasis browser dalam satu berkas HTML (*single-file, zero-dependency*). Dirancang untuk melatih alur investigasi teknis, pembacaan log, identifikasi celah keamanan web maupun API, serta penerapan patch melalui terminal interaktif.

**Live Demo:** https://andarmax.github.io/Hacking/

## Skenario Kasus

| Kasus | Target Simulasi | Fokus Kerentanan & Investigasi | Total XP |
| :--- | :--- | :--- | :--- |
| **01 • PT Nusantara Retail** | `nusantara-retail.test` (`192.168.10.5`) | Password Policy, Phishing Domain Extraction, Open Port (`8080`), Social Engineering, SQL Injection, Stored XSS | 3000 XP |
| **02 • AndarShop** | `andarshop.test` (`192.168.20.7`) | Fake Promo & Account Impersonation, Credential Harvesting, IDOR Order Log, Price Tampering, Brute Force / Rate-Limiting | 3200 XP |
| **03 • AndarPay** | `api.andarpay.test` (`192.168.30.9`) | Exposed Swagger/Debug Env, Leaked JWT Secret, JWT `alg:none`, BOLA/IDOR Wallet History, SSRF Metadata (`169.254.169.254`) | 3500 XP |

## Fitur Utama

* **Terminal Interaktif:** Mendukung perintah investigasi dan patch (`help`, `whoami`, `ls`, `cat`, `scan`, `find flag`, `fix`, `certificate`, `share`, `clear`), output pemindaian bertahap, riwayat perintah (`↑` / `↓`), *autocomplete* (`Tab`), serta bilah pintasan sentuh (*quick-tap bar*) untuk layar ponsel.
* **Variasi Mekanik Investigasi:** Menggabungkan pengujian kekuatan password secara langsung, ekstraksi indikator bukti dari berkas log, inspeksi klik-baris kode/log yang rentan, serta tantangan penerapan patch dalam batas waktu 60 detik.
* **Evidence Board:** Papan indikator terverifikasi di bawah terminal yang otomatis mencatat temuan teknis setiap kali modul selesai.
* **Auto-Save Progres per Akun:** Skor XP, modul selesai, dan waktu pengerjaan per kasus tersimpan otomatis di `localStorage` berdasarkan *username* terdaftar (dilengkapi tombol **Reset** dan **Mode Tamu** tanpa penyimpanan).
* **Audio Synthesizer Opsional:** Efek suara mekanis ringan (`SFX: OFF/ON`) yang dibangkitkan secara lokal melalui Web Audio API tanpa berkas audio eksternal.
* **Laporan Audit & Sertifikat:** Ringkasan temuan teknis dan bukti penyelesaian simulasi yang dapat dicetak atau disimpan ke format PDF.
* **Keamanan Client-Side:**
  * Kebijakan `Content-Security-Policy` ketat dengan `connect-src 'none'`.
  * Penyimpanan kredensial lokal menggunakan *hashing* SHA-256 (Web Crypto API dengan *fallback* murni JavaScript untuk protokol `file://`).
  * Sanitasi output terminal berbasis `textContent` untuk mencegah DOM XSS.
  * Isolasi seluruh *state* permainan di dalam *IIFE closure*.

## Cara Menjalankan

Aplikasi berjalan 100% di sisi klien (*static HTML/CSS/JS*) tanpa memerlukan server atau proses *build*.

1. **Akses Langsung:** Buka [https://andarmax.github.io/Hacking/](https://andarmax.github.io/Hacking/) melalui browser desktop maupun ponsel.
2. **Jalankan Lokal:**
   ```bash
   git clone [https://github.com/andarmax/Hacking.git](https://github.com/andarmax/Hacking.git)
   ```
   Buka berkas `index.html` langsung di browser.

### Akses Masuk
* **Akun Default Lab:** Username `andarlab` / Password `Andar_TE18`
* **Akun Lokal:** Gunakan menu **Buat Akun** untuk menyimpan kredensial dan progres belajar secara otomatis di perangkat.
* **Mode Tamu:** Masukkan nama pada kolom username lalu pilih **Main Sebagai Tamu**.

## Daftar Perintah Terminal

```text
help              Menampilkan daftar perintah sesuai kasus yang aktif
whoami            Menampilkan identitas sesi pentester dan target aktif
ls                Melihat daftar berkas bukti di direktori kasus
cat <nama_file>   Membaca isi log, email, token, atau catatan insiden
scan              Memindai port terbuka pada server target simulasi
find flag         Mengambil flag setelah analisis bukti selesai
fix <parameter>   Menjalankan patch perbaikan pada Modul 08
certificate       Membuka laporan audit & sertifikat (setelah 8/8 modul selesai)
share             Membuat ringkasan hasil untuk dibagikan
clear             Membersihkan layar terminal
```

## Batasan & Etika

Seluruh nama perusahaan, individu, alamat email, domain (`.test`), dan alamat IP di dalam **ANDARLAB** bersifat fiktif. Proyek ini dibuat sebagai media pembelajaran keamanan siber defensif dan tidak ditujukan untuk pengujian pada sistem nyata tanpa izin tertulis.