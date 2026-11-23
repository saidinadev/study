# Sesi 5: Berpikir Komputasional (g4)

**Tanggal:** 23 Nov 2026 · **Fase 0** · **Status:** logika soal koin dikuasai, algoritma genap belum tuntas

## Empat pilar
1. **Dekomposisi:** pecah masalah besar jadi bagian kecil.
2. **Pengenalan pola:** cari kesamaan antarbagian.
3. **Abstraksi:** abaikan detail yang tidak perlu.
4. **Algoritma:** langkah berurutan yang jelas.

**Pseudocode** = algoritma dalam bahasa sehari-hari, tanpa aturan sintaks. Tulis dulu, baru terjemahkan ke Python/JS.

Contoh (angka terbesar):
```
ambil angka pertama, anggap itu yang terbesar
untuk setiap angka berikutnya:
    jika lebih besar dari yang terbesar:
        ganti yang terbesar
tampilkan yang terbesar
```

## Debugging
Urutan di roadmap: **reproduksi → isolasi → hipotesis → tes**. Ubah satu hal per percobaan. Baca error dari atas.

## Tracing
Menelusuri kode baris demi baris dengan tabel nilai variabel.

| Putaran | p | total_diminta |
|---|---|---|
| awal | | 0 |
| 1 | 5 | 5 |
| 2 | 10 | 15 |
| 3 | 20 | 35 |
| 4 | 45 | 80 |

## Soal koin
Koin tersedia vs total permintaan. Anda menghitung sendiri: 25+15 = 40 (cukup, sisa 60); 50+55 = 105 (tidak cukup, kurang 5).

Algoritma:
```
total_diminta = jumlah semua permintaan
jika total_diminta > koin_tersedia:
    kurang = total_diminta - koin_tersedia
jika tidak:
    sisa = koin_tersedia - total_diminta
```

Python (dijalankan sendiri, output `tidak cukup, kurang 5`):
```python
koin_tersedia = 75
permintaan = [5, 10, 20, 45]
total_diminta = 0

for p in permintaan:
    total_diminta = total_diminta + p

if total_diminta > koin_tersedia:
    print("tidak cukup, kurang", total_diminta - koin_tersedia)
else:
    print("cukup, sisa", koin_tersedia - total_diminta)
```

JavaScript (belum dijalankan):
```js
const koinTersedia = 75;
const permintaan = [5, 10, 20, 45];
let totalDiminta = 0;

for (const p of permintaan) {
  totalDiminta = totalDiminta + p;
}

if (totalDiminta > koinTersedia) {
  console.log("tidak cukup, kurang", totalDiminta - koinTersedia);
} else {
  console.log("cukup, sisa", koinTersedia - totalDiminta);
}
```

Perbedaan sintaks: indentasi dan `:` vs `{ }`, `print` vs `console.log`, `const/let` hanya di JS.

## Pelajaran dari soal angka genap
Saya menjawab dengan hasil satu daftar (4 genap, 3 ganjil). Yang diminta: **langkah umum**.

Kerangka yang belum saya isi:
```
buat penghitung, nilai awalnya ...
untuk setiap angka dalam daftar:
    jika angka itu ...:
        penghitung ditambah ...
tampilkan ...
```
**Algoritma = langkah yang berlaku untuk input apa pun, bukan jawaban satu kasus.**

## Tantangan tertinggal
`koin_tersedia = 80` dengan permintaan yang sama. Cabang mana yang jalan? (Uji operator `>` saat nilai sama.)

## Uji diri
1. Sebutkan empat pilar dan satu contoh tiap pilar.
2. Apa beda "hasilnya 4" dengan algoritma menghitung genap?
3. Kenapa tracing berguna saat debugging?
