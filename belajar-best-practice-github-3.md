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

## 3. ✅ Review Code Sebelum Merge

- **Gunakan fitur Review Request di GitHub.**
- Komentar dengan sopan dan fokus pada perbaikan kode, bukan personal.
- Tambahkan label seperti:
  - `needs review`
  - `ready to merge`
  - `work in progress`

---

## 4. 🔀 Strategi Merge: Rebase vs Merge Commit

| Strategi     | Kapan Digunakan         | Kelebihan                    |
|--------------|--------------------------|------------------------------|
| Merge commit | Untuk kolaborasi umum    | Sejarah lengkap              |
| Rebase       | Untuk PR pribadi kecil   | Riwayat bersih & linear      |

> 🎯 **Gunakan squash merge untuk menggabungkan commit menjadi satu jika terlalu banyak commit kecil.**

---

## 5. 🚨 Hindari Force Push ke Branch Bersama

`git push --force` bisa menghapus histori kerja tim. Gunakan hanya di branch pribadi.

Jika perlu pakai:
```bash
git push --force-with-lease
```

---

## 6. 📌 Tambahkan Template PR & Issue

Buat file `.github/pull_request_template.md` agar PR lebih konsisten:

```md
### Deskripsi
...

### Perubahan
- [ ] ...

### Checklist
- [ ] Sudah diuji
- [ ] Tidak merusak fitur lain
```

---


## 7. 📚 Dokumentasi dan Catatan Rilis

- Gunakan `CHANGELOG.md` untuk mencatat perubahan penting.
- Buat rilis GitHub di tab **"Releases"** setelah merge ke `main`.

---

### 🧠 Kesimpulan

Branching dan PR yang rapi akan:
- Memudahkan kolaborasi tim
- Mencegah konflik besar
- Meningkatkan kualitas kode

> 🔁 “Write code for others to read, not just for machines to run.”

---
