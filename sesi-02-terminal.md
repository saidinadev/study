# Sesi 2: Terminal & Command Line (g2)

**Tanggal:** 23 Nov 2026 · **Fase 0** · **Status:** konsep dikenal, latihan ulang belum tuntas

## Tujuan
Nyaman memakai terminal, karena Python, Node, dan Git semuanya dijalankan dari sana.

## Konsep inti
- **Direktori** = folder. Anda selalu "berada" di satu folder (*working directory*).
- **Path** = alamat file/folder, contoh `~/belajar/python/halo.py`. `~` = folder home.
- **Perintah + argumen:** `mkdir belajar` → perintah `mkdir`, argumen `belajar`.

## Perintah wajib hafal
| Perintah | Fungsi |
|---|---|
| `pwd` | lihat lokasi sekarang |
| `ls` | lihat isi folder (CMD Windows: `dir`) |
| `cd nama` | masuk folder |
| `cd ..` | naik satu folder |
| `mkdir nama` | buat folder |
| `touch file.txt` | buat file kosong (CMD: `type nul > file.txt`) |
| `rm file.txt` | hapus file (**permanen**) |

Tips: `Tab` untuk melengkapi nama, panah atas untuk mengulang perintah.

## Editor vs terminal
| | Editor | Terminal |
|---|---|---|
| Fungsi | menulis **isi file** | menjalankan **perintah** |
| Contoh | `console.log("halo")` | `touch belajar1.js` |

Membuka terminal VS Code: `` Ctrl + ` `` (backtick, tanpa Shift). Sempat salah ditulis `Ctrl + ~` di sesi awal.

## Kejadian di sesi ini
Saya mengetik `touch belajar1.js` **di dalam file `belajar1.js`**, hasilnya garis merah dan 1 error. JavaScript tidak mengenal `touch`. Solusi: hapus barisnya, ketik perintah di terminal.

## Yang belum dibahas
Path absolut vs relatif, `cat`, pipe dan redirect (ada di roadmap g2).

## Latihan yang masih tertinggal
Dari folder `practice`: buat folder `catatan`, masuk, buat `hari1.txt`, kembali naik ke `practice`. Tulis perintah dari ingatan.

```
mkdir catatan
cd catatan
touch hari1.txt
cd ..
```

## Uji diri
1. Apa bedanya `cd ..` dan `cd catatan`?
2. Kenapa `rm` perlu hati-hati?
3. Di mana saya mengetik `touch`, di editor atau terminal?
