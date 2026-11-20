# LYOS: Lucky Personal Operating System

Aplikasi pribadi untuk memudahkan kehidupan sehari-hari. Modul pertama: **Keuangan**
(pencatatan pemasukan dan pengeluaran, anggaran per kategori, grafik laju belanja,
perkiraan akhir bulan, cadangan data).

## Lokasi

- Kode: https://github.com/lukianprayoga-stack/lyos (branch `main`)
- Aplikasi untuk HP (setelah GitHub Pages aktif): https://lukianprayoga-stack.github.io/lyos/
- Versi di Claude (data tersimpan di akun Claude): artifact "LYOS"

## Isi folder

| File | Fungsi |
|---|---|
| `index.html` | Seluruh aplikasi (tampilan + logika) |
| `manifest.webmanifest` | Nama, warna, dan ikon agar bisa diinstal di HP |
| `sw.js` | Membuat aplikasi tetap bisa dibuka tanpa internet |
| `icons/` | Ikon aplikasi |

## Cara memasang di HP

Aplikasi ini perlu ditaruh di sebuah alamat web (https) satu kali. Setelah itu bisa diinstal
ke layar utama HP dan dibuka seperti aplikasi biasa, termasuk saat offline.

### Langkah 1: Online-kan folder ini (gratis)

**Pilihan A: Netlify Drop (paling mudah, lewat laptop)**
1. Ekstrak file zip ini sampai muncul folder `lyos`.
2. Buka https://app.netlify.com/drop lalu seret folder `lyos` ke halaman itu.
3. Buat akun Netlify gratis dan klaim situsnya. Situs yang tidak diklaim akan dihapus otomatis.
4. Anda akan mendapat alamat seperti `https://nama-acak.netlify.app`. Nama ini bisa diganti
   di pengaturan situs, misalnya `lyos-lucky.netlify.app`.

**Pilihan B: GitHub Pages**
1. Buat repositori baru di GitHub, unggah semua isi folder `lyos`.
2. Buka Settings, lalu Pages, lalu pilih branch `main` dan folder root, lalu Save.
3. Alamatnya menjadi `https://username.github.io/nama-repo/`.

### Langkah 2: Instal di HP

- **Android (Chrome):** buka alamat tadi, ketuk menu titik tiga, lalu pilih **Instal aplikasi**
  (atau **Tambahkan ke layar utama**).
- **iPhone (Safari):** buka alamat tadi, ketuk tombol **Bagikan**, lalu pilih
  **Tambahkan ke Layar Utama**.

Ikon LYOS akan muncul di layar utama.

## Tentang penyimpanan data

- Versi yang terpasang di HP menyimpan data **di HP itu saja** (tidak ada server).
- Tekan **Cadangkan data** secara rutin. Hasilnya file `.json` yang bisa disimpan ke
  Google Drive atau dikirim ke diri sendiri.
- Untuk pindah HP atau memindahkan data dari versi di Claude: tekan **Pulihkan dari file** dan
  pilih file cadangan tersebut. Transaksi yang sama tidak akan tergandakan.

## Memperbarui aplikasi

1. Ganti `index.html` dengan versi baru.
2. Di `sw.js`, naikkan `VERSI` (misalnya `lyos-v1` menjadi `lyos-v2`).
3. Unggah ulang folder ke Netlify atau GitHub. HP akan memakai versi baru saat aplikasi dibuka
   lagi dengan internet. Data yang sudah tersimpan tidak hilang.

## Rencana pengembangan

LYOS dirancang sebagai "sistem operasi pribadi": modul lain bisa ditambahkan di samping
Keuangan, misalnya tagihan rutin dan pengingat jatuh tempo, target tabungan, daftar tugas,
kebiasaan harian, atau catatan.
