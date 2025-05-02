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
