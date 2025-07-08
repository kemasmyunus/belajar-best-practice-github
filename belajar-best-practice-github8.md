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

Untuk proyek Android Kotlin:

```yaml
# .github/workflows/android.yml
name: Android CI
on:
  push:
    branches: [ main ]
jobs:
  build:
    runs-on: ubuntu-latest
    steps:
    - uses: actions/checkout@v3
    - name: Setup JDK
      uses: actions/setup-java@v3
      with:
        java-version: '17'
    - name: Build APK
      run: ./gradlew build
```

---

## 3. 🔍 Linting Otomatis (Pemeriksaan Format Kode)

Untuk JS/TS dengan ESLint:

```yaml
- name: Run ESLint
  run: npm run lint
```

Untuk Python:

```yaml
- name: Check Python code format
  run: |
    pip install flake8
    flake8 .
```

---

## 4. 📦 Otomatisasi Deploy

Deploy ke Firebase (Hosting):

```yaml
- uses: FirebaseExtended/action-hosting-deploy@v0
  with:
    repoToken: "${{ secrets.GITHUB_TOKEN }}"
    firebaseServiceAccount: "${{ secrets.FIREBASE_SERVICE_ACCOUNT }}"
    channelId: live
    projectId: nama-proyek
```

Deploy ke Vercel:
Gunakan token dan pasang action resmi Vercel dari marketplace.

---

## 5. 🔑 Gunakan Secrets (Rahasia)

Jangan pernah hardcode password/API key di repo.

Gunakan **GitHub Secrets**:

* Masuk ke `Settings` → `Secrets and variables`
* Tambahkan `API_KEY`, `FIREBASE_SERVICE_ACCOUNT`, dll.

Panggil dengan:

```yaml
${{ secrets.API_KEY }}
```

---

## 6. 📤 Kirim Notifikasi ke Discord/Telegram/Slack

Tambahkan notifikasi setelah job sukses/gagal:

```yaml
- name: Kirim notifikasi ke Discord
  run: curl -H "Content-Type: application/json" \
       -d '{"content":"Build sukses! 🎉"}' \
       ${{ secrets.DISCORD_WEBHOOK }}
```

---
