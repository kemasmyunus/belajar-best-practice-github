## ⚙️ Best Practice GitHub #7: Otomatisasi dengan GitHub Actions

### 🎯 Tujuan

Mengotomatisasi proses-proses penting seperti build, test, deploy, dan cek kualitas kode setiap kali kamu push atau membuat pull request.

---

## 1. 🚀 Apa Itu GitHub Actions?

GitHub Actions adalah **fitur CI/CD bawaan GitHub**.

Dengan Actions, kamu bisa otomatis:

* Build project setelah push
* Jalankan test otomatis
* Cek format kode (lint)
* Deploy aplikasi ke server, Firebase, Vercel, dsb.
* Kirim notifikasi ke Discord, Telegram, dsb.

Semua dikendalikan dengan file `.yml` di folder:

```
.github/workflows/
```

---

## 2. ⚙️ Contoh Dasar: Build & Test Otomatis

Contoh workflow Node.js:

```yaml
# .github/workflows/ci.yml
name: CI
on: [push, pull_request]
jobs:
  build:
    runs-on: ubuntu-latest
    steps:
    - uses: actions/checkout@v3
    - name: Setup Node.js
      uses: actions/setup-node@v4
      with:
        node-version: '18'
    - run: npm install
    - run: npm run lint
    - run: npm test
```
