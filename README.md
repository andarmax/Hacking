# ANDARLAB

Lab simulasi *penetration testing* dan analisis insiden berbasis browser tanpa dependensi eksternal (*single-file HTML*). Dirancang untuk melatih alur investigasi dasar, pembacaan log, identifikasi kerentanan web, serta langkah mitigasi melalui antarmuka terminal interaktif.

## Skenario Kasus

| Kasus | Target Simulasi | Fokus Kerentanan & Analisis | Total XP |
| :--- | :--- | :--- | :--- |
| **Kasus 01 — PT Nusantara Retail** | `nusantara-retail.test` (`192.168.10.5`) | Password Policy, Phishing, Open Port (`8080`), Social Engineering, SQL Injection, XSS | 3000 XP |
| **Kasus 02 — AndarShop** | `andarshop.test` (`192.168.20.7`) | Account Impersonation, Credential Harvesting, IDOR, Price Manipulation, Brute Force / Rate-Limiting | 3200 XP |

## Fitur Utama

* **Terminal Simulasi:** Mendukung perintah investigasi dan remediasi (`help`, `whoami`, `ls`, `cat`, `scan`, `find flag`, `fix`, `certificate`, `share`, `clear`).
* **Penilaian & Timer Audit:** Pelacakan progres per kasus, akumulasi XP, kenaikan peringkat (`NEWBIE` hingga `MASTER WHITE HAT`), serta pencatatan durasi penyelesaian.
* **Tantangan Perbaikan (Modul 08):** Simulasi remediasi celah keamanan melalui terminal dalam batas waktu 60 detik.
* **Laporan Audit & Sertifikat:** Ringkasan temuan teknis dan bukti penyelesaian simulasi yang dapat langsung dicetak atau disimpan sebagai PDF.
* **Keamanan Client-Side:**
  * Penyimpanan akun lokal di `localStorage` menggunakan *hashing* SHA-256 (Web Crypto API dengan *fallback* untuk protokol `file://`).
  * Sanitasi output terminal berbasis `textContent` untuk mencegah DOM XSS.
  * Isolasi *state* permainan dan skor XP di dalam *IIFE closure*.

## Cara Menjalankan

Aplikasi berjalan sepenuhnya di sisi klien (*static HTML/CSS/JS*) tanpa memerlukan server atau proses *build*.

1. *Clone* atau unduh repositori ini:
   ```bash
   git clone [https://github.com/andarmax/andarlab.git](https://github.com/andarmax/andarlab.git)
   ```
2. Buka `index.html` langsung di browser (desktop maupun mobile), atau *deploy* sebagai halaman statis di GitHub Pages / Netlify.

### Akses Masuk
* **Akun Default Lab:** Username `andarlab` / Password `Andar_TE18`
* **Akun Lokal:** Gunakan menu **Buat Akun** untuk menyimpan kredensial sendiri secara lokal di perangkat.
* **Mode Tamu:** Isi nama pada kolom username lalu pilih **Main Sebagai Tamu**.

## Daftar Perintah Terminal

```text
help              Menampilkan daftar perintah sesuai kasus yang aktif
whoami            Menampilkan identitas sesi pentester dan target aktif
ls                Melihat daftar file bukti di direktori kasus
cat <nama_file>   Membaca isi log, email, atau catatan insiden
scan              Memindai port terbuka pada server target simulasi
find flag         Mengambil flag setelah analisis bukti selesai
fix <parameter>   Menjalankan patch perbaikan pada Modul 08
certificate       Membuka laporan audit & sertifikat (setelah 8/8 modul selesai)
share             Membuat ringkasan hasil untuk dibagikan
clear             Membersihkan layar terminal
```

## Batasan & Etika

Seluruh nama perusahaan, individu, alamat email, domain (`.test`), dan alamat IP di dalam **ANDARLAB** bersifat fiktif. Proyek ini dibuat sebagai media pembelajaran keamanan siber defensif dan tidak ditujukan untuk pengujian pada sistem nyata tanpa izin tertulis.