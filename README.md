# Website Mata Kuliah Keamanan Sistem Informasi

Proyek Quarto berbahasa Indonesia untuk 14 pertemuan. Website mencakup silabus, materi defensif mingguan, aktivitas kelas, tugas, proyek akhir, rubrik, dan glosarium.

## 1. Sesuaikan identitas

Cari teks bertanda kurung siku seperti `[NAMA DOSEN]`, lalu ganti dengan informasi mata kuliah. Pada `_quarto.yml`, ganti `USERNAME` dan `NAMA-REPOSITORY` pada URL website dan repositori.

## 2. Tampilkan secara lokal

Instal Quarto dari <https://quarto.org/docs/get-started/>, kemudian jalankan:

```bash
quarto preview
```

Untuk menghasilkan website:

```bash
quarto render
```

Hasil render berada di folder `docs/`.

## 3. Masukkan ke GitHub

```bash
git init
git add .
git commit -m "Initial information security course website"
git branch -M main
git remote add origin https://github.com/USERNAME/NAMA-REPOSITORY.git
git push -u origin main
```

## 4. Aktifkan GitHub Pages

Workflow `.github/workflows/publish.yml` merender website ke `docs/` dan menerbitkannya ketika ada *push* ke branch `main`.

Di GitHub, buka **Settings → Pages → Build and deployment**, lalu pilih **GitHub Actions** sebagai *Source*. Jalankan workflow dari tab **Actions** atau lakukan *push* baru.

Jika memakai **Deploy from a branch**, jalankan `quarto render`, commit folder `docs/`, kemudian pilih branch `main` dan folder `/docs`.

## Batas penggunaan materi

Latihan hanya untuk skenario sintetis atau lingkungan yang secara eksplisit disediakan dan diizinkan. Jangan menguji sistem, akun, perangkat, aplikasi, atau jaringan milik pihak lain tanpa persetujuan tertulis.

## Struktur

```text
.
├── _quarto.yml
├── index.qmd
├── silabus.qmd
├── tugas.qmd
├── proyek.qmd
├── rubrik.qmd
├── glosarium.qmd
├── materi/
│   ├── index.qmd
│   └── 01-fondasi.qmd ... 14-presentasi.qmd
├── styles.css
└── .github/workflows/publish.yml
```

Dokumentasi publikasi: <https://quarto.org/docs/publishing/github-pages.html>

