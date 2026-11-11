# Polling Tugas Akhir (3D)

Web app polling interaktif 3D untuk memilih jalur tugas akhir: **Book Chapter** atau **Digital Product**.

- **Frontend:** `index.html` (statis, Three.js via CDN) di-host di GitHub Pages
- **Backend:** Google Apps Script (`apps-script/Code.gs`) + Google Sheets sebagai database

## Deploy ke GitHub Pages
1. Buat repository baru, lalu unggah `index.html`, `.nojekyll`, `README.md`, dan folder `apps-script/`.
2. Buka **Settings → Pages**. Pada *Source* pilih **Deploy from a branch**, branch `main`, folder `/ (root)`.
3. Tunggu 1–2 menit. Situs tersedia di `https://USERNAME.github.io/NAMA-REPO/`.

## Memperbarui backend Apps Script (wajib, sekali saja)
1. Buka project Apps Script, ganti seluruh isi `Code.gs` dengan `apps-script/Code.gs`.
2. Hapus file HTML `Index` di project Apps Script (tidak dipakai lagi).
3. **Deploy → Manage deployments → ikon pensil → Version: New version → Deploy.**
   Pengaturan: *Execute as: Me*, *Who has access: Anyone*. URL `/exec` tetap sama.
4. Tes di browser: `URL_EXEC?action=results` harus menampilkan JSON.

## Mengganti URL backend
Ubah konstanta `API_URL` di `index.html`.
