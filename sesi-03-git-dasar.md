# Sesi 3: Git & GitHub, Dasar (g3)

**Tanggal:** 23 Nov 2026 · **Fase 0** · **Status:** konsep dipahami, commit pertama belum dibuat

## Konsep inti
- **Git** = sistem riwayat perubahan (seperti *save point* game). **GitHub** = tempat menyimpan repository online. Git itu alat, GitHub itu penyimpanan.
- Tiga area:

```
Working Directory --git add--> Staging Area --git commit--> Repository
(file yang diedit)             (akan disimpan)               (riwayat permanen)
```

Analogi: menyusun barang di meja (`add`), lalu menekan tombol foto (`commit`). Satu foto = satu commit.

## Perintah dasar
| Perintah | Fungsi |
|---|---|
| `git init` | jadikan folder ini repository (sekali) |
| `git status` | lihat file yang berubah |
| `git add file` / `git add .` | masukkan ke staging |
| `git commit -m "pesan"` | simpan sebagai commit |
| `git log --oneline` | lihat riwayat |

Pesan commit yang baik: jelas, misalnya `"tambah file latihan python"`. Hindari `"update"` atau `"asdf"`.

## Setup sekali
```
git --version
git config --global user.name "Nama Anda"
git config --global user.email "emailanda@contoh.com"
```
Git saya: **2.53.0.windows.1** (terpasang).

## GUI vs terminal
VS Code Source Control (ikon cabang) menghasilkan hal yang sama dengan terminal. Kesepakatan: pahami konsep lewat terminal, GUI boleh untuk keseharian.

## Kesalahan di sesi ini (penting)
1. `git remote add origin ...` dijalankan di `C:\Users\ASUS` → `fatal: not a git repository`.
2. `git init` ternyata dijalankan di **folder home**, sehingga Git melihat `AppData`, `NTUSER.DAT`, dan lainnya. Untung belum ada commit atau push.
3. `USERNAME` di URL GitHub hanya contoh, harus diganti username asli.

**Cara membereskan** (cek `pwd` dulu, jangan hapus `.gitconfig`):
```
cd ~
Remove-Item -Recurse -Force .git
```

**Aturan baru:** selalu cek `pwd` sebelum `git init`. Hasilnya harus berakhir `\practice`.

## Latihan yang masih tertinggal
Di `D:\study\practice`: `git init` → `git status` (merah) → `git add .` → `git status` (hijau) → `git commit -m "commit pertama: file latihan"` → `git log --oneline`.

## Uji diri
1. Apa beda `add` dan `commit`?
2. Kenapa `git status` pertama berwarna merah dan kedua hijau?
3. Kenapa harus cek `pwd` sebelum `git init`?
