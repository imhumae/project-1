# Analysis - Sistem Checkout Produk Sederhana

## Input
harga	  ( Number )	Harus (> 0)
jumlah	  ( Number )	Harus (> 0)
isMember  ( Boolean )	true jika member, false jika bukan
## Proses
Validasi input. Jika harga tidak valid atau jumlah bukan bilangan bulat, kembalikan pesan error dan hentikan perhitungan.
Hitung subtotal = harga x jumlah.
Cek status member.
Member:     diskon = 10% dari subtotal.
Non-member: diskon = 0 Tidak dapat diskon.
Hitung total setelah diskon = subtotal - diskon.
Cek ongkos kirim.
Total setelah diskon >= Rp250.000: ongkir = Rp0 (Dapatgratisongkir).
Total setelah diskon <= Rp250.000: ongkir = Rp15.000.
Hitung total pembayaran = total setelah diskon + ongkir.
## Output
Jika input valid: subtotal, diskon, total setelah diskon, ongkos kirim, dan total pembayaran.
Jika input tidak valid: pesan "input tidak valid".
## Aturan Keputusan
Apakah input valid?	(T) Lanjut hitung. (F) Tampilkan error, berhenti.
Apakah member?	(T) Diskon 10%. (F) Diskon 0%
Apakah total setelah diskon >= Rp250.000?	(T) Ongkir Rp0. (F)	Ongkir Rp15.000.

Catatan: batas Rp250.000 dibandingkan dengan total setelah diskon, bukan subtotal. Total tepat Rp250.000 mendapat ongkir gratis.
## Pattern
Alur selalu berurutan: validasi, hitung subtotal, keputusan diskon, keputusan ongkir, hitung total.
Dua keputusan memakai bentuk yang sama: satu kondisi menghasilkan salah satu dari dua nilai (if-else).
Aturan bisnis memakai nilai tetap: diskon 10%, batas gratis ongkir Rp250.000, 
ongkir Rp15.000.
## Abstraction
Yang diabaikan: tampilan (UI), API, database, pembayaran sungguhan, stok, dan variasi produk.
Yang dipertahankan: hanya data yang memengaruhi perhitungan, yaitu harga, jumlah, dan status member.
Semua logika dibungkus dalam satu fungsi hitungCheckout(harga, jumlah, isMember) sehingga mudah diuji.