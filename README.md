# TambakOS Research Space — Udang Windu

Website statis untuk merencanakan penelitian IoT petak pemeliharaan udang windu berlapis terpal di Batu Segara Abadi. Dibuat 20 Oktober 2026.

## Jalankan

Buka `index.html` lewat browser. Tidak butuh npm, server, database atau instalasi paket untuk demo ini. Fonts eksternal opsional (ada fallback lokal).

## Isi situs

- Ringkasan proyek dan kondisi lokasi yang diketahui/belum diketahui.
- Monitoring **SIMULASI**, bukan pembacaan fisik. Skenario DO rendah/kritis/pulih, sensor invalid, dan koneksi 4G putus dapat dicoba. Tidak ada perintah dikirim ke perangkat.
- Sketsa petak terpal, rancangan komunikasi ESP32, sensor, dua aerasi.
- Alur rencana pemeliharaan benur hingga kolam pembesaran.
- 42 baris RAB versi hemat (rincian persis dari Excel sebelumnya), dengan filter/pencarian.
- Dua file `.docx` terbaru untuk BAB I dan BAB II beserta sampul asli.
- Checklist survei dan catatan yang disimpan **hanya pada browser** lewat `localStorage`.
- Rencana skenario pengujian sebelum dan setelah pemasangan.

## Publish ke GitHub Pages

1. Ekstrak ZIP ini.
2. Di repo https://github.com/ibrahalim/tambak, upload **isi folder** ini, terutama `index.html`, folder `docs`, dan README. Jangan unggah ZIP saja karena GitHub Pages tidak membukanya otomatis.
3. Jika repo sudah punya versi lama, replace `index.html`, tambahkan folder `docs/` dan commit perubahan.
4. Settings → Pages → Deploy from a branch → `main` → `/(root)` → Save.
5. Situs akan berada di https://ibrahalim.github.io/tambak/ setelah proses deploy selesai.

**Perhatian:** Repo Public berarti file Word/Excel dalam `docs/` juga dapat diakses publik. Periksa identitas dan informasi yang ingin dipublikasikan sebelum upload.

## Batasan penting

- Tidak terhubung dengan ESP32, sensor, server, ataupun aktuator sungguhan.
- Ambang DO hanya setelan awal rekayasa; harus divalidasi oleh pengelola dan pengujian lapangan.
- Ukuran petak, jadwal benur, dan kapasitas blower belum diketahui.
- Sketsa listrik bukan panduan instalasi jaringan AC. Perlindungan dan pemasangan 220 V wajib dikerjakan teknisi listrik yang berkompeten.
- RAB adalah anggaran indikatif, bukan penawaran harga terkini.
