==========================================================
PT2 SBU — Fiber Deployment Tracker
Panduan Hosting Singkat
==========================================================

ISI PAKET:
- index.html  -> file dashboard utama (satu file, tidak butuh backend/database)

CARA HOSTING (pilih salah satu, gratis semua):

1) NETLIFY DROP (paling gampang, tanpa akun)
   - Buka https://app.netlify.com/drop
   - Drag folder/file index.html ke halaman itu
   - Selesai, langsung dapat link publik

2) GITHUB PAGES
   - Buat repo baru di GitHub
   - Upload file index.html ke repo itu
   - Masuk ke Settings > Pages > pilih branch "main" > folder "/ (root)"
   - Tunggu 1-2 menit, link aktif di https://<username>.github.io/<repo>/

3) VERCEL
   - Daftar di vercel.com (bisa pakai akun GitHub)
   - New Project > Upload folder ini
   - Deploy

CATATAN PENTING:
- Dashboard ini berjalan 100% di browser (client-side). Tidak ada data
  yang dikirim ke server manapun — aman untuk data internal perusahaan.
- Data dimuat melalui:
  a) Fetch otomatis dari Google Sheets (perlu sheet di-share "Anyone
     with the link - Viewer" dan di-publish ke web sebagai CSV), ATAU
  b) Upload manual file CSV (tombol "Upload CSV" di dashboard) — cara
     ini selalu berfungsi di manapun dashboard di-hosting.
- Setelah di-hosting (bukan dibuka via file:// lokal), fitur fetch
  otomatis dari Google Sheets biasanya akan berjalan normal karena
  domain hosting punya izin CORS yang benar (beda dengan saat dibuka
  langsung dari file di komputer).
- Tidak perlu setup database atau backend apapun. File ini murni
  HTML+CSS+JS yang berjalan di browser pengguna.
