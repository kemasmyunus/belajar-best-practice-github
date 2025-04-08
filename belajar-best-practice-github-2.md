# Best Practices Menggunakan GitHub - 2

Setelah memahami dasar-dasar penggunaan GitHub secara efisien, ada beberapa praktik lanjutan yang dapat meningkatkan produktivitas, kolaborasi, dan keberlanjutan proyek.

## 1. Gunakan Semantic Versioning
- Terapkan [Semantic Versioning (SemVer)](https://semver.org/) untuk merilis versi software:
  ```
  MAJOR.MINOR.PATCH
  Contoh: 2.1.3
  ```
- Gunakan tag seperti `v1.0.0` untuk menandai rilis dalam repositori.

## 2. Manfaatkan Releases
- Buat rilis baru pada setiap versi penting.
- Sertakan changelog yang jelas (fitur baru, perbaikan, perubahan besar).
- Gunakan fitur *pre-release* untuk versi beta/eksperimen.

## 3. Tulis Changelog yang Terstruktur
- Gunakan file `CHANGELOG.md` untuk mencatat perubahan setiap versi.
- Format yang disarankan:
  ```markdown
  ## [1.2.0] - 2025-04-08
  ### Added
  - Fitur ekspor data ke CSV
  ### Fixed
  - Bug saat login dengan akun Google
  ```

## 4. Buat Template Issue dan PR
- Gunakan `.github/ISSUE_TEMPLATE/` dan `.github/PULL_REQUEST_TEMPLATE.md`.
- Dengan template, semua kontributor memiliki panduan saat membuat issue atau PR.
- Contoh struktur template:
  ```markdown
  ### Deskripsi
  Jelaskan perubahan atau masalah yang ditemukan.

  ### Langkah Reproduksi
  1. ...
  2. ...

  ### Checklist
  - [ ] Sudah diuji
  - [ ] Dokumentasi diperbarui
  ```

## 5. Dokumentasi Kontributor
- Tambahkan `CONTRIBUTING.md` yang menjelaskan:
  - Cara memulai proyek secara lokal
  - Aturan penamaan branch dan commit
  - Cara membuat pull request

## 6. Gunakan GitHub Discussions
- Aktifkan fitur Discussions untuk berdiskusi tanpa harus membuat issue.
- Cocok untuk ide fitur baru, feedback, atau tanya jawab teknis.
