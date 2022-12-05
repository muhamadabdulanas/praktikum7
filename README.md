# praktikum7


Latihan 1
Ubahlah kode dibawah ini menjadi fungsi menggunakan lambda.
import math

def a(x):
return x**2

def b(x, y):
return math.sqrt(x**2 + y**2)

def c(*args):
return sum(args)/len(args)

def d(s):
return "".join(set(s))
#Code

 ![image](https://user-images.githubusercontent.com/115569493/205496736-5e2dfe7a-00d9-429f-a1d6-e68c8fc08b98.png)

![image](https://user-images.githubusercontent.com/115569493/205496807-9342aaeb-7743-474f-968e-01d299cc7c11.png)

Output
 
# Tugas Praktikum
## Buat program sederhana dengan mengaplikasikan penggunaan fungsi yang akan menampilkan daftar nilai mahasiswa, dengan ketentuan:
#### • Fungsi tambah() untuk menambah data
#### • Fungsi tapilkan() untuk menampilkan data
#### • Fungsi hapus(nama) untuk menghapus data berdasarkan nama
#### • Fungsi ubah(nama) untuk mengubah data berdasarkan nama
#### • Buat flowchart dan penjelasan programnya pada README.md.

 NAS = {}

def TAMBAH():
    print("Tambah Data")
    nama = input("Nama\t : ")
    nim = input("NIM\t : ")
    uts = int(input("Nilai UTS\t : "))
    uas = int(input("Nilai UAS\t : "))
    tugas = int(input("Nilai Tugas\t : "))
    akhir = (tugas * 30/100) + (uts * 35/100) + (uas * 35/100)
    KON[nama] = nim, tugas, uts, uas, akhir
def TAMPILKAN():
    if NAS.items():
        print("Daftar Nilai")
        print("=================================================================================")
        print("| No |      Nama      |     NIM     |  Tugas  |   UTS   |   UAS   |    Akhir    |")
        print("=================================================================================")
        i = 0
        for a in NAS.items():
            i += 1
            print("| {no:2d} | {0:14s} | {1:11s} | {2:7d} | {3:7d} | {4:7d} |      {5:6.2f} |"
            .format (a[0][: 14],a[1][0],a[1][1],a[1][2],a[1][3],a[1][4], no = i))
        print("=================================================================================")

def UBAH():
    print("Ubah Data")
    nama = input("Masukkan Nama : ")
    if nama in KON.keys():
        nim = input("NIM\t : ")
        uts = int(input("Nilai UTS\t : "))
        uas = int(input("Nilai UAS\t : "))
        tugas = int(input("Nilai Tugas\t : "))
        akhir = (tugas * 30/100) + (uts * 35/100) + (uas * 35/100)
        NAS[nama] = nim, tugas, uts, uas, akhir

    else:
        print("Nama tidak ditemukan ")
def HAPUS():
    print("Hapus Data")
    nama = input("Masukkan Nama : ")
    
    if nama in KON.keys():
        del NAS[nama]
    
    else:
        print("Nama tidak ditemukan")
while True:

    print("\n")
    print("================================")
    print("      PROGRAM MAHASISWA UPB     ")
    print("================================\n")

    print("|1| Lihat Data                 |")
    print("|2| Tambah Data                |")
    print("|3| Ubah Data                  |")
    print("|4| Hapus Data                 |")
    print("|5| Keluar                     |")

    x = input("> PILIH MENU : ")

    print("\n")

    if x == '1':
        TAMPILKAN()
    elif x == '2':
        TAMBAH()
    elif x == '3':
        UBAH()
    elif x == '4':
        HAPUS()

    else:

        exit()
