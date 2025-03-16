# Best Practices dalam Menggunakan GitHub

GitHub adalah platform yang sangat berguna untuk kolaborasi dan manajemen proyek berbasis kode. Agar penggunaan GitHub lebih efektif, berikut beberapa best practice yang sebaiknya diikuti.

## 1. Struktur Repository yang Baik
- Gunakan nama repository yang deskriptif dan jelas.
- Sertakan file `README.md` untuk memberikan gambaran tentang proyek.
- Gunakan `.gitignore` untuk mengecualikan file yang tidak perlu.
- Tambahkan `LICENSE` agar pengguna tahu bagaimana kode dapat digunakan.

## 2. Penggunaan Branch yang Terorganisir
- Gunakan branch `main` atau `master` sebagai branch utama.
- Gunakan branch `develop` untuk pengembangan fitur sebelum digabungkan ke branch utama.
- Gunakan branch fitur (`feature/`), perbaikan (`fix/`), atau hotfix (`hotfix/`) untuk perubahan spesifik.

## 3. Commit yang Jelas dan Konsisten
- Gunakan pesan commit yang jelas dan ringkas.
- Gunakan format pesan commit seperti:
  ```
  feat: Menambahkan fitur baru untuk autentikasi
  fix: Memperbaiki bug pada fungsi login
  refactor: Merapikan kode di modul pengguna
  ```
- Gunakan commit kecil dan sering untuk memudahkan tracking perubahan.
