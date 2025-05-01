
## 8. 🔐 Gunakan Proteksi Branch

### Mengapa penting?
Proteksi branch mencegah:
- Push langsung ke `main`
- Merge tanpa review
- Hapus branch secara tidak sengaja

### Cara mengaktifkan:
1. Masuk ke repo → `Settings`
2. Pilih `Branches`
3. Tambahkan **branch protection rule**
4. Centang opsi seperti:
   - ✅ Require pull request reviews
   - ✅ Require status checks to pass
   - ✅ Restrict who can push

---

## 9. 📊 Gunakan GitHub Projects atau Issues untuk Manajemen Tugas

Gunakan fitur **GitHub Issues** untuk mencatat:
- Bug
- Request fitur
- Diskusi teknis

Gunakan **Projects (Board)** seperti Kanban:
| Todo | In Progress | Done |
|------|-------------|------|
| #45  | #32         | #12  |

> 📌 Gunakan label seperti `bug`, `enhancement`, `help wanted` untuk pengelompokan yang rapi.

---

## 10. 🛠️ Continuous Integration (CI)

Integrasikan **GitHub Actions** untuk otomatisasi:
- Cek linting (format kode)
- Jalankan unit test
- Build proyek

Contoh `.github/workflows/ci.yml`:

```yaml
name: CI
on: [push, pull_request]
jobs:
  build:
    runs-on: ubuntu-latest
    steps:
    - uses: actions/checkout@v3
    - name: Setup Node
      uses: actions/setup-node@v4
      with:
        node-version: '18'
    - run: npm install
    - run: npm run lint
    - run: npm test
```

---

## 11. 👥 Kolaborasi Tim: Assign & Mention

Gunakan fitur GitHub untuk:
- **Assign issue/PR** ke tim yang bertanggung jawab
- **Mention anggota tim** dengan `@username` di komentar

Contoh komentar:
```
@pachanpanatto Tolong review bagian validasi email ya 🙏
```

---
