# Studio.Flow Workspace

Workspace internal untuk Owner, Desainer Grafis, dan Admin Sosial Media/Shopee — Papan Tugas, Tugas Admin, dan Laporan Bulanan dalam satu halaman.

## Menjalankan secara lokal
Cukup buka `index.html` langsung di browser. Untuk mode sinkron (Firebase), pastikan `firebaseConfig` di dalam file sudah diisi.

## Deploy ke GitHub Pages
1. Push repo ini ke GitHub (branch `main`).
2. Buka **Settings > Pages** di repo.
3. Pada **Source**, pilih branch `main` dan folder `/ (root)`.
4. Simpan — GitHub akan memberi URL publik (biasanya `https://<username>.github.io/<repo>/`).
5. Bagikan URL itu ke tim. Tidak perlu server tambahan — Firebase menangani penyimpanan & sinkronisasi data.

## Firebase (penyimpanan & sinkronisasi)
Data (tugas, briefing, laporan, PIN) tersimpan di Firebase Realtime Database supaya semua peran (Owner, Admin, Desainer) melihat data yang sama secara real-time, dari lokasi mana pun.

Jika perlu mengganti project Firebase, update objek `firebaseConfig` di bagian atas script pada `index.html`.

**Catatan keamanan:** Rules Database sebaiknya tidak dibiarkan permanen dalam "test mode" (baca/tulis bebas untuk siapa saja yang tahu URL project). Setelah stabil, minta bantuan mempersempit Rules-nya.
