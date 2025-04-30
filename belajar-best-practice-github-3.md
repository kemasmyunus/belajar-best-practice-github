## 📘 Best Practice GitHub #3: Manajemen Branch & Pull Request yang Efektif

### 🎯 Tujuan
Memahami cara terbaik dalam mengelola *branch* dan melakukan *pull request* (PR) agar kolaborasi dalam proyek menjadi lebih efisien dan minim konflik.

---

## 1. 🌿 Buat Branch Berdasarkan Fitur atau Perbaikan

**Gunakan penamaan branch yang deskriptif dan konsisten**, contohnya:

| Jenis Branch | Contoh Penamaan         |
|--------------|--------------------------|
| Fitur        | `feature/login-page`     |
| Bugfix       | `bugfix/fix-typo-title`  |
| Refactor     | `refactor/clean-header`  |
| Hotfix       | `hotfix/login-error`     |

### Tips:
- Hindari bekerja langsung di `main` atau `master`.
- Satu branch = satu tujuan (*single responsibility*).

---

## 2. 🔄 Lakukan Pull Request (PR) Secara Terstruktur

### Langkah-langkah membuat PR yang baik:
1. **Buat PR ke branch utama (misalnya `main` atau `develop`)**.
2. **Isi judul dan deskripsi PR secara jelas.**
   - Contoh judul: `Add validation to login form`
   - Deskripsi: Jelaskan _what_, _why_, dan _how_ perubahan dilakukan.
3. **Referensikan Issue jika ada.**  
   Gunakan `Closes #123` untuk menutup issue secara otomatis.

---
