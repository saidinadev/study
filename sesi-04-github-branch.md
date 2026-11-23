# Sesi 4: GitHub, Branch, dan Pull Request (g3 lanjutan)

**Tanggal:** 23 Nov 2026 · **Fase 0** · **Status:** konsep dibaca, belum dipraktikkan

## Remote dan push
**Remote** = salinan repository di GitHub. Langkah sekali jalan:
1. Buat akun GitHub.
2. New repository, nama `practice`, **jangan** centang "Add README".
3. Hubungkan lalu kirim:

```
git remote add origin https://github.com/USERNAME-ASLI/practice.git
git branch -M main
git push -u origin main
```

`origin` = nama panggilan untuk alamat repository GitHub. `git push` mengirim commit, `git pull` mengambil perubahan terbaru.

## Branch
Branch = jalur kerja terpisah. Bereksperimen tanpa merusak `main`. Kalau bagus di-**merge**, kalau gagal dibuang.

```
main:   A --- B ------------- E   (setelah merge)
               \             /
fitur:          C --- D -----
```

```
git switch -c fitur-baru   # buat branch dan pindah
# edit, add, commit seperti biasa
git switch main            # kembali ke main
git merge fitur-baru       # gabungkan
git branch                 # lihat daftar branch
```

## Pull Request (PR)
Cara di GitHub berkata: "Saya selesai di branch ini, tolong tinjau dan gabungkan ke `main`." Alur: push branch → buka GitHub → klik **Compare & pull request**. Dibahas lebih dalam di topik Kolaborasi & Code Review.

## Yang belum dibahas
`.gitignore` dan resolve conflict (ada di roadmap g3).

## Latihan yang masih tertinggal
1. Buat repo `practice` di GitHub, hubungkan, push.
2. Buat branch `latihan-branch`, tambah satu baris di `belajar1.py`, add dan commit.
3. `git switch main`, buka `belajar1.py`. **Baris tadi masih terlihat atau hilang? Kenapa?** (jawaban belum saya tulis)

## Uji diri
1. Apa fungsi `origin`?
2. Kenapa bereksperimen di branch lebih aman?
3. Apa itu Pull Request?
