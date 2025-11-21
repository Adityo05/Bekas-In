# BEKAS-IN

Deskripsi singkat
-----------------
BEKAS-IN adalah aplikasi web statis (frontend) untuk marketplace barang bekas. Proyek ini dibuat sebagai tugas atau portofolio Web Desain. Aplikasi menampilkan daftar barang bekas, memungkinkan pengguna mendaftar/login (disimpan di LocalStorage), menambahkan barang ke keranjang, dan memesan barang. Interface dibuat dengan HTML, CSS, dan JavaScript murni (tanpa backend).

Fitur utama
-----------
- Daftar produk yang di-load dari `barang.json`.
- Halaman detail produk (`menu_beli_barang.html`) dengan tombol Tambah ke Keranjang dan Beli sekarang.
- Keranjang belanja per-user yang disimpan di `localStorage`.
- Sistem registrasi / login sederhana menggunakan `localStorage`.
- Halaman Jual Barang (formulir UI) untuk memasukkan detail jualan (statik, tidak tersimpan ke server).
- Halaman pesanan menampilkan pesanan yang dibuat oleh pengguna (disimpan di `localStorage`).
- UI responsif untuk tampilan mobile.

Struktur proyek
----------------
```
BEKAS-IN/
├─ assets/                # gambar dan ikon
├─ barang.json            # data produk (mock)
├─ home.html              # halaman utama
├─ menu_beli_barang.html  # detail produk
├─ keranjang.html         # keranjang belanja
├─ jual.html              # form jual barang (frontend)
├─ login.html             # login (localStorage)
├─ daftar.html            # register (localStorage)
├─ akun.html              # profil pengguna (localStorage)
├─ pesanan.html           # daftar pesanan
├─ kontak.html            # halaman kontak
└─ README.md              # file ini
```

Cara menjalankan (lokal)
-------------------------
Aplikasi berbasis file statis — cukup buka `home.html` dengan browser, atau jalankan server lokal sederhana (rekomendasi agar fetch ke `barang.json` berjalan tanpa CORS/akses file):

gunakan ekstensi VS Code: Live Server — klik `Go Live` lalu buka `home.html`.

Cara menggunakan
----------------
1. Buka `home.html` di browser.
2. Gunakan form pencarian (placeholder) — saat ini hanya UI.
3. Klik produk untuk membuka `menu_beli_barang.html?id=<id>`.
4. Untuk menambahkan ke keranjang atau memesan, login terlebih dahulu (`daftar.html` → `login.html`).
5. Keranjang dan pesanan disimpan ke `localStorage` sehingga hanya terlihat di browser yang sama.

Cara push ke GitHub (PowerShell)
--------------------------------
Jika belum ada repo lokal:
```powershell
	cd "<path\to\project-folder>"    # ganti dengan lokasi proyek di komputer Anda
git init
git add .
git commit -m "Initial commit: BEKAS-IN project"
# Buat repo baru di GitHub (web) -> salin URL remote
git remote add origin https://github.com/<username>/bekasin.git
git branch -M main
git push -u origin main
```

Jika sudah ada repo remote:
```powershell
	cd "<path\to\project-folder>"    # ganti dengan lokasi proyek di komputer Anda
git add .
git commit -m "Update README and project description"
git push
```

Deployment (GitHub Pages)
-------------------------
- Buka Settings repo → Pages → pilih branch `main` dan folder `/ (root)` → Save.
- Tunggu beberapa menit, lalu situs akan live di `https://<username>.github.io/bekasin/` (pastikan `index.html` tersedia — di repo ini gunakan `home.html` sebagai halaman depan; set `home.html` rename ke `index.html` atau buat `index.html` yang mengarahkan ke `home.html`).

Lisensi
-------
Disarankan menggunakan lisensi MIT jika ingin mempublikasikan sebagai open-source. Tambahkan file `LICENSE` jika setuju.

Kontribusi
----------
- Tambahkan issue untuk bug/fitur baru.
- Buat pull request ke branch `main` dan jelaskan perubahan.

Tentang
-------
BEKAS-IN dibuat untuk materi Web Desain (tugas semester). Tidak ada backend — semua data tersimpan pada LocalStorage atau JSON statis.

Kontak
------
Jika ingin menghubungi pengembang: bekasin@gmail.com
