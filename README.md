## Laporan praktikum 2 ##
# Kasus 1: Program pemesana tiket bioskop #
Program ini berisi program python sederhana untuk menghitung harga tiket bioskop. Program ini menghitung harga tiket yang akan dibayar, jenis tiket yaitu reguler dan vip dan memberikan diskon 20% untuk pelanggan yang memiliki kartu member.

# Deksripsi Program #
Detail program ini bertujuan untuk menghitung total harga tiket berdasarkan pilihan pelanggan: tiket reguler Rp 50.000 tiket vip Rp 100.000 dan pelanggan yang memiliki kartu member mendapatkan diskon 20%.

Program akan meminta untuk input data:
Tipe tiket yaitu reguler atau vip, status member Ya atau tidak. Program akan menampilkan hitungan total dari harga tiket yang harus dibayar.

# Algoritma #
Langkah-langkah dari program ini:

Program meminta pengguna untuk menginput tipe tiket reguler/vip

Program meminta pengguna untuk mengkonfirmasi apakah mempunyai kartu member atau tidak

Program akan menentukan harga sesuai dengan pelanggan pilih

dan jika pelanggan memiliki kartu member program akan menyesuaikan harga dengan diskon 20%

Program akan menampilkan total harga yang harus dibayar

```
def hitung_harga_tiket(tipe_tiket, status_member):
    # Harga tiket
    harga_reguler = 50000
    harga_vip = 100000
    
    # Menentukan harga berdasarkan tipe tiket
    harga_tiket = harga_reguler if tipe_tiket.lower() == 'reguler' else harga_vip
    
    # Menghitung total harga dengan diskon jika memiliki kartu member
    total_harga = harga_tiket * 0.8 if status_member.lower() == 'ya' else harga_tiket
    
    return total_harga

def main():
    print("Program Hitung Harga Tiket Bioskop")
    
    # Input tipe tiket
    tipe_tiket = input("Masukkan tipe tiket (reguler/VIP): VIP ")
    
    # Input status member
    status_member = input("Apakah Anda memiliki kartu member? (ya/tidak): tidak ")
    
    # Hitung total harga
    total_harga = hitung_harga_tiket(tipe_tiket, status_member)
    
    # Tampilkan hasil
    print(f"Total harga yang harus dibayar: Rp{total_harga:.2f}")

if __name__ == "__main__":
    main()
```

## Kasus 2: Kalkulator Sederhana ##
Program Kalkulator Sederhana yang dapat melakukan operasi aritmatika dasar. Program ini memungkinkan pengguna untuk memasukkan dua angka dan memilih jenis operasi (penjumlahan, pengurangan, perkalian, atau pembagian) yang akan diterapkan pada kedua angka tersebut.

Deskripsi Program
Kalkulator ini mendukung empat operasi aritmatika:

1.Penjumlahan (+)

2.Pengurangan (-)

3.Perkalian (*)

4.Pembagian (/)

Pengguna akan diminta untuk memasukkan dua angka dan operator aritmatika. Program kemudian akan menampilkan hasil dari operasi yang dipilih. Program ini juga menangani pembagian dengan nol dan akan memberikan pesan peringatan jika pembagian tidak bisa dilakukan.

Algoritma
Berikut langkah-langkah dari algoritma program kalkulator sederhana ini:

Program meminta pengguna untuk memasukkan angka pertama.

Program meminta pengguna untuk memasukkan operator aritmatika yang ingin digunakan (+, -, *, atau /).

Program meminta pengguna untuk memasukkan angka kedua.

Berdasarkan operator yang dimasukkan, program melakukan operasi aritmatika pada kedua angka.

Jika operasi adalah pembagian dan angka kedua adalah nol, program menampilkan pesan bahwa pembagian dengan nol tidak dapat dilakukan.

Program menampilkan hasil dari operasi yang dipilih atau pesan error jika operator tidak valid.

```
def kalkulator(angka1, angka2, operator):
    if operator == '+':
        return angka1 + angka2
    elif operator == '-':
        return angka1 - angka2
    elif operator == '*':
        return angka1 * angka2
    elif operator == '/':
        if angka2 != 0:
            return angka1 / angka2
        else:
            return "Error: Pembagian dengan nol tidak diperbolehkan."
    else:
        return "Error: Operator tidak valid."

def main():
    print("Program Kalkulator Sederhana")
    
    # Input angka dan operator
    try:
        angka1 = float(input("Masukkan angka pertama: "))
        angka2 = float(input("Masukkan angka kedua: "))
        operator = input("Masukkan operator (+, -, *, /): ")
        
        # Hitung hasil
        hasil = kalkulator(angka1, angka2, operator)
        
        # Tampilkan hasil
        print(f"Hasil: {hasil}")
        
    except ValueError:
        print("Input tidak valid. Harap masukkan angka.")

if __name__ == "__main__":
    main()
```

## Flowchart ##
# Hasil dari flowchart pemesanan tiket bioskop #
![Flowchart tiket bioskop](https://github.com/user-attachments/assets/a7afa900-ef77-4ddd-a604-92d57e0269bf)

# Hasil dari flowchart kalkulator sederhana #
![Flowchart Kalkulator sederhana](https://github.com/user-attachments/assets/01bceb2e-e12b-4969-af26-9384c8f53906)

# Screenshot code kasus 1 dan kasus 2 #
Kasus Tiket Bioskop
![code kasus1](https://github.com/user-attachments/assets/186bb45d-7b47-470f-9cb3-62663682ea6f)

Hasil
![hasil tiket reguler diskon](https://github.com/user-attachments/assets/fe0dc591-52b6-4e01-b910-d2a31af3091f)

![hasil tiket vip no diskon](https://github.com/user-attachments/assets/cc231f4c-5126-4a52-b999-3a9a05d4e0cb)



Kasus Kalkulator
![code kasus 2](https://github.com/user-attachments/assets/787a247e-c1df-4a88-aefb-c3d21754bf26)

hasil
![hasil kalkulator sederhana](https://github.com/user-attachments/assets/8d6927b2-46f0-479c-b642-8bf7d1f1d9b6)


