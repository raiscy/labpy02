# labpy02 
Modul Praktikum 2 

Latihan 3 : Buat Program Python Untuk Kasus ini 
Kasus 1 : Program Pemesanan Tiket Bioskop 
Buat program yang menghitung harga tiket bioskop. Tiket reguler berharga Rp50.000, sedangkan tiket VIP berharga Rp100.000. Jika user memiliki kartu member, mereka mendapatkan diskon 20% dari harga tiket. Program ini harus meminta tipe tiket dan status member dari user, lalu menghitung total harga yang harus dibayar. Dengan menggunakan if else dan operator ternary

    def hitung_harga_tiket():
    """
    Fungsi untuk menghitung harga tiket bioskop.

    Returns:
    float: Total harga tiket yang harus dibayar.
    """

    # Input tipe tiket
    tipe_tiket = input("Masukkan tipe tiket (reguler/VIP): ").lower()

    # Input status member
    status_member = input("Apakah Anda member? (ya/tidak): ").lower()

    # Hitung harga tiket berdasarkan tipe tiket
    if tipe_tiket == "reguler":
      harga_tiket = 50000
    elif tipe_tiket == "vip":
      harga_tiket = 100000
    else:
      print("Tipe tiket tidak valid.")
      return

    # Hitung diskon jika member
    if status_member == "ya":
      diskon = harga_tiket * 0.2
      harga_tiket -= diskon

    # Tampilkan total harga tiket
    print("Total harga tiket: Rp", harga_tiket)

    # Panggil fungsi hitung_harga_tiket()
    hitung_harga_tiket()

PROSES INPUT DATA

![kode python tiket bioskop](https://github.com/user-attachments/assets/2bc37b8f-6fbe-422d-8720-872873a4d7a5)
![kode tiket bioskop](https://github.com/user-attachments/assets/c99900a1-c5c7-476d-9a78-522df0e0aa9b)

HASIL OUTPUT DATA
![hasil tiket bioskop](https://github.com/user-attachments/assets/c8b07090-851e-4471-bad3-30b0c9a8b0a6)

PENJELASAN PROGRAM PEMESANAN TIKET BIOSKOP



