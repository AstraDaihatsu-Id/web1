# Deploy ke GitHub Pages (Website Statis)

Berikut langkah deploy website **ASTRA DAIHATSU ID BLITAR** ke **GitHub Pages** (tanpa domain custom).

## 1) Buat repository di GitHub
1. Buka GitHub → **New repository**
2. Nama repo bebas (contoh: `astra-daihatsu-blitar`)
3. Pilih **Public** (Pages paling gampang) → Create

## 2) Upload semua file website
Upload isi folder proyek ini ke root repo (file `index.html`, folder `assets/`, folder `artikel/`, `robots.txt`, `sitemap.xml`, dll).

Cara cepat:
- Drag & drop via GitHub Web (Add file → Upload files), atau
- Via Git (clone repo → copy file → commit → push)

## 3) Aktifkan GitHub Pages via Actions
Repo ini sudah saya siapkan workflow: **`.github/workflows/pages.yml`**

Langkahnya:
1. Masuk repo → **Settings**
2. Menu kiri → **Pages**
3. Pada “Build and deployment” pilih:
   - **Source: GitHub Actions**

Setelah itu:
- Push ke branch **main** → otomatis deploy

## 4) Ambil link hasil deploy
Setelah workflow sukses, URL biasanya:
`https://USERNAME.github.io/REPO/`

Anda bisa lihat di:
- Tab **Actions** (status workflow), atau
- Settings → Pages (akan muncul link)

## 5) (Opsional tapi disarankan) Update URL SEO (example.com)
Saat Anda sudah tahu URL final GitHub Pages, ganti placeholder `https://example.com` di:
- `index.html` → meta `og:url`
- `robots.txt` → baris `Sitemap:`
- `sitemap.xml` → semua `<loc>`

Kalau Anda kirim **USERNAME** GitHub + **nama repo**, saya bisa update otomatis file-file tersebut agar SEO lebih rapi.

