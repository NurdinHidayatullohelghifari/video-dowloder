# Video Studio 🤡 — Android wrapper

Project Android Studio untuk membungkus HTML Video Studio asli sebagai aplikasi WebView. HTML asli, banner, teks ikon badut 🤡, warna neon, dan fitur editor dipertahankan. Tidak memakai backend.

## Batasan tanpa backend
- Bisa memilih file video/audio dari perangkat, memprosesnya dengan FFmpeg WebAssembly (CDN saat pertama dipakai), dan menyimpan hasil ke `Download/VideoStudio`.
- Bisa memuat URL file media langsung jika server sumber mengizinkan CORS.
- URL halaman YouTube/TikTok/Instagram/Facebook hanya pratinjau yang didukung; aplikasi ini TIDAK mengekstrak atau mengunduh video dari halaman platform.
- File besar dapat kehabisan RAM; konversi berjalan di perangkat dan bergantung pada kemampuan WebView/codec.

## Membuat APK melalui GitHub Actions
1. Buat repository GitHub baru dan unggah seluruh isi folder proyek ini (jangan hanya file HTML).
2. Buka tab **Actions** → workflow **Build Android APK** → **Run workflow**.
3. Setelah selesai, buka hasil run dan unduh artifact **VideoStudio-Android-APK**. Di dalam ZIP artifact ada `app-debug.apk`.
4. Pindahkan APK ke Android, izinkan pemasangan dari sumber tersebut bila diminta, lalu pasang.

## Build lokal
Buka folder ini di Android Studio versi terbaru, tunggu Gradle sync, lalu pilih **Build > Build Bundle(s) / APK(s) > Build APK(s)**.

Catatan: APK debug bukan APK Play Store. Untuk rilis publik, buat signing key sendiri dan build release bertanda tangan.
