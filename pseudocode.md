Diskon_Member  = 10%
Minimun_Total_Belanja   = 250000
Biaya_Ongkir                  = 15000

FUNCTION hitungCheckout(harga, jumlah, isMember)

    // 1. Validasi input
    IF harga BUKAN Number OR harga <= 0 THEN
        RETURN "Input tidak valid"
    END IF
    IF jumlah BUKAN bilangan bulat OR jumlah <= 0 THEN
        RETURN "Input tidak valid"
    END IF

    // 2. Hitung subtotal
    subtotal = ( harga x jumlah )

    // 3. Keputusan status member
    IF isMember = true THEN
        diskon <- subtotal x Diskon_Member / 100
    ELSE
        diskon <- 0
    END IF

    // 4. Total setelah diskon
    totalSetelahDiskon = ( subtotal - diskon )

    // 5. Keputusan ongkos kirim
    IF totalSetelahDiskon >= 250000 THEN
        ongkir <- 0
    ELSE
        ongkir <- BIAYA_ONGKIR
    END IF

    // 6. Total pembayaran
    totalBayar ( totalSetelahDiskon + ongkir )

    // 7. Output
    RETURN subtotal, diskon, ongkir, totalBayar

END FUNCTION