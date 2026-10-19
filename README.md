# TambakOS — Website Rancangan IoT Udang Windu

Website statis interaktif untuk menjelaskan **rancangan implementasi lapangan** Sistem Monitoring Lingkungan Budidaya Udang Windu Berbasis IoT (Batu Segara Abadi, Karawang).

## Jalankan

- Cara paling mudah: buka `index.html` di browser modern. Grafik dan simulasi akan berjalan tanpa server.
- Untuk pengembangan lokal/PWA: masuk ke folder dan jalankan `python -m http.server 8000`, lalu buka `http://localhost:8000`.
- Untuk publish: unggah **seluruh isi folder** ke hosting statis (misalnya Netlify, Vercel static, GitHub Pages). Tidak perlu build.

## Isi website

1. **Dashboard** — metrik empat parameter, grafik, log peristiwa, simulasi logika DO dan motor, outage 4G, buffer LittleFS, serta uji sensor invalid.
2. **Arsitektur** — skema sensor → ESP32 → MiFi → Supabase → PWA, jalur kendali lokal, diagram rencana distribusi daya (bukan wiring detail teknis).
3. **Rancangan fisik** — ilustrasi konseptual alat saat dipasang dan isi boks IP65, beda peralatan permanen vs kalibrasi.
4. **RAB** — semua 35 komponen/kegiatan dari BARANG.pdf, filter, kategori, dan unduh CSV. Total Rp22.679.000.
5. **Pengujian** — indikator, alur pembangunan, daftar prainstalasi yang bisa dicentang, dan catatan keselamatan.

## Batasan penting

- Ini adalah **website desain dan simulasi frontend**, **BUKAN** sistem monitor real-time tersambung ke sensor. Nilai dashboard dibuat untuk demonstrasi. **Tidak ada perintah fisik yang dikirim ke motor**.
- Desain perangkat merupakan **ilustrasi** dan **bukan gambar kerja listrik**. Hubungan 220 V AC, proteksi motor dan grounding harus didesain/dipasang teknisi listrik setelah survei.
- Sumber listrik 220 V **masih asumsi dari dokumen RAB**: keberadaan PLN/listrik pada titik kolam belum terkonfirmasi. Genset, UPS atau solar panel **tidak ada** di anggaran ini.
- Batas kendali DO `<4 mg/L` dua pembacaan valid untuk ON; `>5 mg/L` tiga pembacaan valid dan waktu ON minimum 15 menit untuk OFF. Rentang peringatan suhu awal 25–30°C, pH 7,5–9,0. Ambang salinitas belum ditentukan.
- Kincir 1 HP bukan jaminan mencukupi untuk meratakan oksigen dalam kolam 3.400 m². Hasil pengukuran satu titik tidak mewakili seluruh kolam.
- Durasi pengujian 7–14 hari, interval 5 menit, pembandingan DO/suhu ≥40 pasangan dan pH/salinitas ≥20 pasangan sesuai proposal.

## Sumber data

- Proposal skripsi yang sudah direvisi ke orientasi implementasi lapangan (bukan sekadar prototyping).
- `BARANG.pdf`, lampiran RAB halaman 1–3 dan ringkasan wawancara halaman 4. Website menggunakan angka per item dan total sebagaimana dokumen; istilah lama "RAB Prototipe" di UI diganti menjadi "rancangan implementasi" sesuai permintaan revisi arah penelitian.

## Pengembangan menjadi sistem produksi

Sebelum online diperlukan API/backend nyata, autentikasi dan otorisasi, skema data dan idempotency, firmware ESP32, pembacaan/kalibrasi sensor, pengiriman HTTPS, push notification, mekanisme sinkronisasi konfigurasi berizin, serta uji beban dan keamanan. Semua control state fisik harus didasarkan pada feedback motor, bukan hanya perintah software.
