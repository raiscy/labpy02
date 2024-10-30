# labpy02 
Modul Praktikum 2 

# Latihan 3 : Buat Program Python Untuk Kasus ini 
# Kasus 1 : Program Pemesanan Tiket Bioskop 
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

PENJELASAN PROGRAM PEMESANAN TIKET BIOSKOP : 
1. Kata “Start” dimana proses akan dimulai dan proses input sudah berjalan.
2. Pemilihan antara opsi yang telah diberi tau, Reguler atau VIP
3. Pemeriksaan opsi apakah tiket yang di miiliki Reguler atau bukan
4. Jika tiket yang dimiliki reguler maka harga tiket adalah 50.000 tetapi jika tiket VIP harga menjadi 100.000
5. Cek status apakah pengguna memiliki akses member atau tidak
6. Jika pengguna memiliki akses member maka tiket akan diberikan diskon sebesar 20% dari harga yang di tentukan, baik reguler maupun VIP
7. Menampilkan total harga setelah adanya diskon atau tidak
8. Selesai. 

# Kasus 2 : Program Kalkulator Sederhana
Buat program kalkulator yang menerima dua angka dan satu operator aritmatika dari pengguna (penjumlahan, pengurangan, perkalian, atau pembagian). Program akan menghitung hasil sesuai dengan operator yang dipilih. Dengan menggunakan if elif else untuk menentukan operasi aritmatika

    def kalkulator():
    # Menerima input dari pengguna
    angka1 = float(input("Masukkan angka pertama: "))
    angka2 = float(input("Masukkan angka kedua: "))
    operator = input("Masukkan operator (+, -, *, /): ")

    # Menghitung hasil berdasarkan operator yang dipilih
    if operator == "+":
        hasil = angka1 + angka2
        print(f"Hasil penjumlahan: {hasil}")
    elif operator == "-":
        hasil = angka1 - angka2
        print(f"Hasil pengurangan: {hasil}")
    elif operator == "*":
        hasil = angka1 * angka2
        print(f"Hasil perkalian: {hasil}")
    elif operator == "/":
        if angka2 != 0:
            hasil = angka1 / angka2
            print(f"Hasil pembagian: {hasil}")
        else:
            print("Error: Pembagian dengan nol tidak diperbolehkan.")
    else:
        print("Error: Operator tidak valid.")

    # Memanggil fungsi kalkulator
    kalkulator()

PROSES INPUT DATA
![kode python kalkulator sederhana](https://github.com/user-attachments/assets/0f4d3142-452b-4740-ad99-ebcf1b9b3049)
![kode kalkulator sederhana](https://github.com/user-attachments/assets/e9c53f25-a2d2-4c84-8985-44bd7cbc9204)

HASIL OUTPUT 
![hasil kalkulator sederhana](https://github.com/user-attachments/assets/0e69a719-88f5-4d92-9c79-6882d3e48c68)

PENJELASAN PROGRAM KALKULATOR SEDERHANA
1. Kata “Start” dimana proses akan dimulai dan proses input sudah berjalan.
2. Menginput angka1 yang diinginkan
3. Menginput angka2 yang diinginkan
4. Menginput operator yang berisi +,-,/ atau *
5. Menggunakan stuktur percabangan untuk memeriksa operator yang digunakan
6. Memeriksa apakah angka2 = 0 Jika ya, tampilkan pesan error. Jika tidak, lakukan pembagian. Jika operator tidak valid: tampilkan pesan error
7. Menampilkan hasil perhitungan
8. Selesai. 

# Latihan 1 : Membuat Program Menentukan Nilai Akhir 
    #!/usr/bin/python3

    # Mengambil input dari pengguna
    nama = input("Masukkan nama: ")
    uts = input("Masukkan nilai UTS: ")
    uas = input("Masukkan nilai UAS: ")
    tugas = input("Masukkan nilai Tugas: ")

    # Menghitung nilai akhir
    akhir = (int(tugas) * 0.2) + (int(uts) * 0.4) + (int(uas) * 0.4)

    # Menentukan keterangan lulus atau tidak
    keterangan = ("TIDAK LULUS", "LULUS")[akhir > 60.0]

    # Menentukan nilai huruf
    if akhir > 80:
        huruf = "A"
    elif akhir > 70:
        huruf = "B"
    elif akhir > 50:
        huruf = "C"
    elif akhir > 40:
        huruf = "D"
    else:
        huruf = "E"

    # Menampilkan hasil
    print("\nNama :", nama)
    print("Nilai UTS :", uts)
    print("Nilai UAS :", uas)
    print("Nilai Tugas :", tugas)
    print("Nilai Akhir :", akhir)
    print("\nNilai Huruf :", huruf)
    print("Keterangan :", keterangan)

![kode menentukan nilai akhir](https://github.com/user-attachments/assets/659f1c83-b9cd-4534-8785-53a252602af6)
![Screenshot 2024-10-29 124125](https://github.com/user-attachments/assets/40ae6720-fb78-4e5c-80a9-438b66035842)




