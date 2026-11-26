# ANDARLAB

Lab simulasi ethical hacking — Kasus 01 & 02.

Belajar pertahanan sistem lewat investigasi: baca bukti, scan server fiktif, perbaiki temuan, tulis laporan.

100% lokal. Tidak ada server. Tidak ada data yang dikirim ke mana-mana.

---

## Cara Main

1. Buka `index.html` di browser
2. Masuk / buat akun / main sebagai tamu
3. Pilih kasus di halaman utama
4. Kerjakan dari bukti di terminal sampai laporan selesai

---

## Akun

### 1. Akun Lab (bawaan)

- **Username:** `andarlab`
- **Password:** `Andar_TE18`

Akun ini untuk demo / kelas. Boleh dipakai siapa saja.

### 2. Akun Pemain (buat sendiri)

- Di halaman login, klik **Buat Akun**
- Isi username + password sendiri
- Username: minimal 3 karakter, huruf / angka / `_` saja
- Password: minimal 6 karakter
- Setelah dibuat, langsung login pakai akun itu

Akun pemain tersimpan lokal di perangkat (`localStorage`).
Tidak dikirim ke server.

> Kalau ganti HP / ganti browser / hapus data browser, akun hilang.
> Buat lagi saja. Itu wajar untuk lab lokal.

### 3. Mode Tamu

- Isi nama saja, kosongkan password
- Klik **Main Sebagai Tamu**
- XP, timer, dan sertifikat tetap jalan

---

## Kasus 01 — PT Nusantara Retail

Target fiktif: `nusantara-retail.test`
Server fiktif: `192.168.10.5`

Semua nama, email, IP, dan perusahaan dalam kasus ini fiktif.

### Briefing

HR PT Nusantara Retail (fiktif) meminta audit:
Rina (Staff Finance) menerima email aneh yang meminta OTP.
Server terasa lambat. Izin audit diberikan dalam cerita game.

### Alur

1. Baca bukti di terminal:
    • cat email-rina.txt
    • cat chat-rina.txt
    • cat log.txt
    • cat backup.txt
2. Selesaikan 8 modul:
   - 01 — Password Rina
   - 02 — Email Phishing ke Rina
   - 03 — Scan Server 192.168.10.5
   - 04 — Chat Social Engineering
   - 05 — File Backup
   - 06 — SQLi di Login Internal
   - 07 — XSS di Komentar Internal
   - 08 — Perbaiki Sebelum Maintenance


Flag Kasus 01: `FLAG{ANDARLAB_WHITE_HAT_2026}`

---

## Kasus 02 — AndarShop (Toko Online Fiktif)

Target fiktif: `andarshop.test`
Server fiktif: `192.168.20.7`

Kasus baru. Lebih sulit dari Kasus 01. Ada forensik pesanan.

### Briefing

Owner AndarShop (fiktif) meminta audit:
Kode voucher 90% beredar padahal owner tidak pernah membuat voucher itu.
Akun admin tidak bisa login. Ada pesanan yang alamatnya diubah setelah dibayar.
Izin audit diberikan dalam cerita game.


Flag Kasus 02: `FLAG{ANDARSHOP_DEFENDED_2026}`

### Yang Dipelajari di Kasus 02

- Voucher palsu: cek ke sumber resmi, bukan dari grup chat
- Akun palsu: cek handle persis, bukan foto profil
- Login palsu: credential harvesting, wajib reset + MFA
- IDOR: server harus cek kepemilikan pesanan
- Harga: jangan percaya harga dari client, harga final harus dari server
- Brute force: rate-limit + lockout + alert + MFA

---

## Fitur

- **2 kasus** — Kasus 01 dan 02, progress dipisah per kasus
- **Akun pemain** — buat username + password sendiri, tersimpan lokal
- **Mode Tamu** — main tanpa daftar
- **Timer per kasus** — jalan dari masuk sampai audit kasus itu selesai
- **Share** — salin hasil ke WA / IG Story, per kasus
- **Laporan Audit + Sertifikat** — bisa cetak / simpan PDF, per kasus
- **Bukti fiktif** — email, chat, log, backup bisa dibaca di terminal
- **100% lokal** — 1 file `index.html`, tanpa install, tanpa backend

---

## Skor

| Kasus | Total XP | Rank Tertinggi |
| --- | --- | --- |
| Kasus 01 — PT Nusantara Retail | 3000 XP | MASTER WHITE HAT |
| Kasus 02 — AndarShop | 3200 XP | MASTER WHITE HAT |
| **Total** | **6200 XP** | **DOUBLE MASTER** |

- 8/8 modul selesai di satu kasus = **MASTER WHITE HAT** kasus itu
- 8/8 di dua kasus = **DOUBLE MASTER**
- Waktu audit tampil di laporan dan di teks share, per kasus


---

## Aturan Main

1. Semua target dalam game ini fiktif.
2. Jangan gunakan teknik dalam game ini ke sistem tanpa izin tertulis dari pemiliknya.
3. Ethical hacking yang sah = ada izin, ada ruang lingkup, ada laporan.
4. Jangan pernah bagikan OTP / password asli ke siapa pun, termasuk yang mengaku dari IT.
5. Jangan percaya voucher / link promo dari akun yang meniru akun resmi. Cek handle dan sumber resmi.

---

Tidak ada build. Tidak ada `npm install`. Buka `index.html` langsung jalan.

---

## Roadmap

- [x] Kasus 01 — PT Nusantara Retail
- [x] Kasus 02 — AndarShop (Toko Online Fiktif)
- [x] Akun pemain lokal + Mode Tamu
- [x] Timer + Share + Laporan Audit per kasus
- [ ] Kasus 03 — Sekolah Fiktif / Ujian Online
- [ ] Leaderboard lokal 5 tercepat per kasus
- [ ] Daily Challenge
- [ ] Akun online (butuh backend + database) — nanti, kalau sudah ramai

---

## Untuk Guru / Komunitas

Boleh dipakai untuk kelas / workshop / komunitas, selama:

- Tetap menyebut ANDARLAB
- Tetap menjelaskan bahwa semua target fiktif
- Tetap menekankan aturan: tanpa izin = bukan ethical hacking

---

## Lisensi

Untuk pembelajaran. Bebas dipakai untuk kelas / komunitas.

ANDARLAB — Yogyakarta



