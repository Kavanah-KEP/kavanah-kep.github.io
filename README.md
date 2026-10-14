# kavanah-kep.github.io — Verifikasi Aplikasi Android Absenku

Repo ini **khusus** untuk satu berkas: `.well-known/assetlinks.json`.

Android memeriksa berkas itu di `https://kavanah-kep.github.io/.well-known/assetlinks.json`
untuk memastikan APK Absenku memang milik situs ini. Jika cocok, aplikasi tampil
layar penuh tanpa bilah alamat Chrome.

- `.nojekyll` → wajib ada, agar GitHub Pages tidak menyembunyikan folder `.well-known`
- `index.html` → mengalihkan pengunjung ke `/absenku/`
- Isi `assetlinks.json` diganti dengan berkas `assetlinks.json` dari paket PWABuilder

Berkas ini **aman dipublikasikan** — hanya berisi nama paket dan sidik jari publik
sertifikat, bukan kunci rahasia. Kunci rahasia (`signing.keystore`) JANGAN pernah
dimasukkan ke repo ini.
