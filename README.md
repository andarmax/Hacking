# ANDARLAB

Lab simulasi ethical hacking — Kasus 01: PT Nusantara Retail (Fiktif).

Belajar pertahanan sistem lewat investigasi: baca bukti, scan server fiktif, perbaiki temuan, tulis laporan.

100% lokal. Tidak ada server. Tidak ada data yang dikirim ke mana-mana.

---

## Cara Main

1. Buka `index.html` di browser
2. Masuk / buat akun / main sebagai tamu
3. Kerjakan Kasus 01 dari bukti di terminal sampai laporan selesai

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
Dibuat untuk latihan pertahanan, bukan untuk mengakses sistem asli.

### Briefing

HR PT Nusantara Retail (fiktif) meminta audit:
Rina (Staff Finance) menerima email aneh yang meminta OTP.
Server terasa lambat. Izin audit diberikan dalam cerita game.

### Alur

1. Baca briefing dari HR
2. Baca bukti di terminal: