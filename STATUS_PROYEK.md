# Status data penelitian — 20 Oktober 2026

## Terinformasi dari pengelola/pengamatan awal pengguna

- Tambak Batu Segara Abadi terdiri atas beberapa kolam; luasan kawasan sekitar 3.400 m² adalah informasi awal, bukan luas petak pengukuran.
- Petak terpal berada di dalam salah satu kolam dan airnya berbeda/terpisah.
- Rencana semi-intensif: pakan tambahan, monitoring lebih ketat, intervensi kualitas air; belum berjalan.
- Pengelola menangani budidaya; peneliti mengerjakan sistem IoT, keduanya berkoordinasi.
- Ada PLN, relatif stabil. Tidak ada Wi-Fi tetap, tersedia jaringan seluler.

## Belum terkonfirmasi

- Dimensi, kedalaman, volume air, dan padat tebar petak.
- Umur, jumlah benur, serta target pemindahan.
- Jadwal mulai pemeliharaan dan durasi siklus.
- Apakah blower/aerator telah tersedia dan dapat dipakai.
- Kapasitas blower, jumlah diffuser, jarak panel listrik dan kebutuhan backup.

## Rancangan perangkat, bukan hasil lapangan

- DO optik seawater RS485, pH IP68 RS485, EC PPS/graphite RS485, suhu 1-Wire.
- ESP32 → MiFi 4G → backend + PostgreSQL → web dashboard/PWA.
- Aerasi dasar kontinu + booster otomatis karena DO rendah.
- Ambang DO di dashboard merupakan contoh awal untuk uji teknis, bukan batas aman universal.
- Tidak mengklaim kenaikan survival rate udang.

Dokumen BAB I dan II bersifat draft untuk bimbingan dan akan diperbarui ketika fakta lapangan diketahui.
