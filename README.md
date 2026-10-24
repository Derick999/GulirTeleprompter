# Gulir Teleprompter

Teleprompter pribadi yang jalan di browser HP dan bisa di-install ke layar utama. Tanpa backend, tanpa akun. Naskah tersimpan di perangkat.

## Isi folder

- `index.html` : seluruh aplikasi dalam satu file
- `manifest.webmanifest` : data nama dan ikon untuk install
- `sw.js` : service worker supaya bisa dibuka tanpa internet
- `icons/` : ikon aplikasi

## Deploy ke GitHub Pages

1. Buat repo baru di GitHub, misalnya `gulir-teleprompter` (public).
2. Upload semua isi folder ini ke root repo (`index.html` harus ada di paling atas, bukan di dalam subfolder).
3. Buka Settings > Pages. Di bagian Build and deployment, pilih Deploy from a branch, branch `main`, folder `/ (root)`, lalu Save.
4. Tunggu 1 sampai 2 menit. Alamatnya jadi `https://USERNAME.github.io/gulir-teleprompter/`.

Alternatif: Vercel. Import repo yang sama, framework "Other", tanpa build command.

## Install di HP

Android (Chrome): buka alamat di atas, ketuk menu titik tiga, pilih Install app (atau Add to Home screen).

iPhone (Safari): buka alamat di atas, ketuk tombol Share, pilih Add to Home Screen, lalu Add.

## Cara pakai

- Ketuk layar prompter untuk jeda atau lanjut. Geser jari untuk menggulung manual.
- Tulis catatan di dalam kurung siku, misalnya `[senyum]`, supaya tampil sebagai label kuning.
- Nyalakan "Kamera sebagai latar" di pengaturan untuk merekam video. Browser akan minta izin kamera dan mikrofon. Hasil rekaman bisa dibagikan atau diunduh. Teks prompter tidak ikut terekam.
- Kalau kamera bermasalah, pakai panel "Tes kamera" di pengaturan. Panel itu menampilkan status izin, preview langsung, dan kode error beserta penjelasannya.
- Mode cermin dipakai kalau HP dipasang menghadap kaca beam splitter di depan lensa.
- Di laptop: Spasi putar/jeda, panah atas/bawah ubah kecepatan, + dan - ubah ukuran huruf, M cermin, Esc kembali.

## Mengubah aplikasi

Setelah mengedit `index.html`, naikkan nomor versi di `sw.js` (`gulir-v4` jadi `gulir-v5`) supaya HP mengambil versi terbaru.
