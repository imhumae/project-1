# Mini Project: Sistem Checkout Produk Sederhana

**Nama:** Muhamad Nurhamam

## Deskripsi Case Study

Program menghitung total pembayaran checkout dari tiga input: harga produk, jumlah produk, dan status member. Aturannya:

1. Harga harus angka positif dan jumlah harus bilangan bulat positif. Jika tidak valid, program menampilkan pesan "Input tidak valid" dan tidak melanjutkan perhitungan.
2. Subtotal = harga x jumlah.
3. Member mendapat diskon 10% dari subtotal. Non-member tidak mendapat diskon.
4. Ongkos kirim gratis jika total setelah diskon minimal Rp250.000. Jika kurang, ongkos kirim Rp15.000.
5. Total pembayaran = total setelah diskon + ongkos kirim.

## Struktur File

| File | Isi |
|---|---|
| `analysis.md` | Problem decomposition: input, proses, output, pattern, abstraction |
| `flowchart.drawio` | File flowchart (bisa dibuka di draw.io) |
| `flowchart.png` | Hasil export flowchart |
| `pseudocode.md` | Pseudocode yang mengikuti flowchart |
| `checkout.js` | Implementasi JavaScript fungsi `hitungCheckout(harga, jumlah, isMember)` |
| `testing.md` | 10 skenario uji beserta hasilnya |

## Cara Menjalankan

1. Pastikan Node.js sudah terpasang (cek dengan `node -v`).
2. Clone atau download repository ini.
3. Buka terminal di folder repository, lalu jalankan:

```
node checkout.js
```

Program akan menjalankan 10 skenario uji dan menampilkan hasilnya di terminal.

Untuk memakai fungsinya langsung:

```js
const { hitungCheckout } = require("./checkout");
console.log(hitungCheckout(100000, 3, true));
```

## Penggunaan AI

AI (Claude) digunakan sebagai partner diskusi dan pembantu penyusunan draf dokumen dan kode, yaitu:
- Diskusi alur logika dan aturan keputusan case study.
- Draf awal `analysis.md`, flowchart, `pseudocode.md`, `checkout.js`, dan `testing.md`.

Saya sudah membaca, memahami, dan memeriksa seluruh hasilnya, serta menjalankan sendiri program di Node.js untuk memastikan hasil pengujian sesuai.