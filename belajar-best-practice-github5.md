## 📘 Best Practice GitHub #4: Dokumentasi dan Standar Proyek

### 🎯 Tujuan

Menjadikan proyek GitHub mudah dipahami, digunakan, dan dikembangkan oleh orang lain (termasuk dirimu sendiri di masa depan).

---

## 1. 📄 README yang Informatif

README adalah **halaman muka proyek**. Wajib ada dan informatif.

### Struktur README yang disarankan:

````md
# Nama Proyek

Deskripsi singkat dan tujuan proyek.

## Fitur
- ✅ Fitur 1
- ✅ Fitur 2

## Instalasi
```bash
git clone https://github.com/username/repo
cd repo
npm install
npm start
````

## Penggunaan

Tulis contoh penggunaan, gambar, atau demo jika perlu.

## Kontribusi

Petunjuk kontribusi dan style guide (jika ada).

## Lisensi

MIT / GPL / Custom License

## Kontak

Nama, email, atau link ke profil

````

---

## 2. 📘 Buat File Kontribusi (`CONTRIBUTING.md`)

File ini menjelaskan **aturan kontribusi** seperti:
- Format commit message
- Standar penulisan kode
- Alur PR dan issue
- Style guide (naming, struktur folder, dll)

Contoh:
```md
## Cara Kontribusi

1. Fork repo
2. Buat branch `feature/nama-fitur`
3. Commit dengan format: `[fitur] Judul singkat`
4. Buat PR ke branch `develop`
````

---

## 3. ✅ Tambahkan Lisensi (`LICENSE`)

Setiap proyek **wajib punya lisensi**, agar orang lain tahu hak penggunaan kode.

Beberapa lisensi populer:

| Lisensi | Keterangan                          |
| ------- | ----------------------------------- |
| MIT     | Bebas pakai & modifikasi            |
| GPL     | Wajib buka source jika dimodifikasi |
| Apache  | Mirip MIT tapi lebih legalistik     |

> Bisa generate otomatis di GitHub saat membuat repo.

---

## 4. 🧭 Gunakan `.gitignore` yang Sesuai

`.gitignore` mencegah file tidak penting (misal: build, log, secret) masuk repo.

Contoh untuk Node.js:

```
node_modules/
.env
dist/
```

Contoh untuk Android:

```
*.iml
.gradle
/local.properties
```

Gunakan [gitignore.io](https://www.toptal.com/developers/gitignore) untuk generate otomatis.

---

## 5. 🔧 Standarisasi Struktur Folder

Struktur folder yang rapi = tim lebih mudah bekerja sama.

Contoh frontend web:

```
/src
  /components
  /pages
  /utils
/public
/tests
```

Contoh backend API:

```
/controllers
/routes
/models
/utils
```

---

## 6. 💬 Tambahkan Komentar dan Dokumentasi Kode

Komentar yang baik = kode lebih mudah dipahami. Gunakan standar seperti:

```js
/**
 * Menghitung total harga dengan diskon
 * @param {number} harga
 * @param {number} diskon
 * @returns {number}
 */
function hitungHarga(harga, diskon) {
  return harga - harga * diskon;
}
```

Gunakan tool dokumentasi otomatis:

* JSDoc (JavaScript)
* Doxygen (C/C++)
* Sphinx (Python)

---

## 7. 🧪 Tambahkan Tes (Unit Test)

Testing = kode lebih andal.

Gunakan:

* Jest / Vitest untuk JS/TS
* Pytest untuk Python
* JUnit untuk Java
* Espresso untuk Android

Struktur folder tes:

```
/tests
  login.test.js
  user.test.js
```

---

## 8. 🧠 Buat Wiki (Opsional)

Untuk dokumentasi tambahan seperti:

* Arsitektur sistem
* Panduan deploy
* Konsep data flow

GitHub menyediakan tab **Wiki** khusus untuk ini.

---
