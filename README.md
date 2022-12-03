# Praktikum 7

### Nama : Sinta Hardianti Wijaya

### NIM : 312210342

### Kelas : TI.22.A3

## Latihan 

Soal latihan

![latihan 1 prak7](https://user-images.githubusercontent.com/115516473/205430348-c3591f43-c750-4df6-ba0e-a3e3e3c497b7.png)

## - Kode program menggunakan fungsi lambda

```
import math

a = lambda x: x ** 2
print(a(46))

b = lambda x,y: x**2 + y**2
print(b(4,6))

c = lambda *args : sum(args)/len(args)
print(c(5,7,9,11,10))

d = lambda s: "".join(set(s))
print(d("Tertimpa"))
```

## Outputnya :

![output latihan1 prak6](https://user-images.githubusercontent.com/115516473/205430623-1aedcacb-7825-4e82-a17c-bdcf0dcadb36.png)

hasil dari ```"".join(set(s))"``` akan menghasilkan huruf acak

## Tugas Praktikum 7

![soaltugaspraktikum7](https://user-images.githubusercontent.com/115516473/205430699-3c72f86c-26df-4e79-93a8-8d5f637e5aab.png)

### - Buat dictionary nama mahasiswa

``` mahasiswa = {} ```

### - Buat kode untuk menu tambah data dan ubah data

```
from menu.mahasiswa import mahasiswa

def add():
    print("Tambah Data")
    nama = input("Nama\t : ")
    nim = input("NIM\t : ")
    uts = int(input("Nilai UTS\t : "))
    uas = int(input("Nilai UAS\t : "))
    tugas = int(input("Nilai Tugas\t : "))
    akhir = (tugas * 30/100) + (uts * 35/100) + (uas * 35/100)
    mahasiswa[nama] = nim, tugas, uts, uas, akhir

def update():
    print("Ubah Data")
    nama = input("Masukkan Nama : ")
    if nama in mahasiswa.keys():
        nim = input("NIM\t : ")
        uts = int(input("Nilai UTS\t : "))
        uas = int(input("Nilai UAS\t : "))
        tugas = int(input("Nilai Tugas\t : "))
        akhir = (tugas * 30/100) + (uts * 35/100) + (uas * 35/100)
        mahasiswa[nama] = nim, tugas, uts, uas, akhir

    else:
        print("Nama tidak ditemukan ")
 ```
 
 ### - Buat kode untuk lihat data
 
 ```
 from menu.mahasiswa import mahasiswa

def show():
    if mahasiswa.items():
        print("Daftar Nilai")
        print("=================================================================================")
        print("| No |      Nama      |     NIM     |  Tugas  |   UTS   |   UAS   |    Akhir    |")
        print("=================================================================================")
        i = 0
        for a in mahasiswa.items():
            i += 1
            print("| {no:2d} | {0:14s} | {1:11s} | {2:7d} | {3:7d} | {4:7d} |      {5:6.2f} |"
            .format (a[0][: 14],a[1][0],a[1][1],a[1][2],a[1][3],a[1][4], no = i))
        print("=================================================================================")
        
    else:
        print("Daftar Nilai")
        print("=================================================================================")
        print("| No |      Nama      |     NIM     |  Tugas  |   UTS   |   UAS   |    Akhir    |")
        print("=================================================================================")
        print("|                                TIDAK ADA DATA                                 |")
        print("=================================================================================")
 ```
 
 ### - Buat kode untuk hapus data
 
 ```
 from menu.mahasiswa import mahasiswa

def delete():
    print("Hapus Data")
    nama = input("Masukkan Nama : ")
    
    if nama in mahasiswa.keys():
        del mahasiswa[nama]
    
    else:
        print("Nama tidak ditemukan")
```

### - Buat kode untuk main nya agar berjalan

```
from menu.add import add,update
from menu.view import show
from menu.delete import delete

while True:

    print("\n")
    print("================================")
    print("      Program input nilai       ")
    print("================================\n")

    print("[1] Lihat Data")
    print("[2] Tambah Data")
    print("[3] Ubah Data")
    print("[4] Hapus Data")
    print("[5] Keluar")

    x = input("> PILIH MENU : ")

    print("\n")

    if x == '1':
        show()
    elif x == '2':
        add()
    elif x == '3':
        update()
    elif x == '4':
        delete()

    elif x == '5':
        print("==========================================================================")
        print('\n')
        print("> You exit the code                        ")
        print("> Thanks for using it :DDD ")
        print("\n")
        print("==========================================================================")

        exit()

    else:
        print("            KODE YANG ANDA MASUKKAN TIDAK VALID !!!!!!!!!!!")
```

### - Outputnya :

![outputpraktikum7](https://user-images.githubusercontent.com/115516473/205431110-8a96732c-bc55-4675-aac0-ceee1053097f.png)

## Untuk memunculkan datanya, gunakan perintah ```L```

![prak7-1](https://user-images.githubusercontent.com/115516473/205431271-e6b48d36-bd97-4a26-8e63-a9e869dd7445.png)

## Untuk menambahkan data, gunakan perintah ```T```

![prak7-2](https://user-images.githubusercontent.com/115516473/205431401-3f913354-225d-4858-98cb-0a9ae3d9aa9f.png)

![prak7-3](https://user-images.githubusercontent.com/115516473/205431433-16a7dad8-7e1e-461b-a5d9-e2ce79780a00.png)

## Untuk mengubah data, ketik perintah ```U```

![prak7-4](https://user-images.githubusercontent.com/115516473/205431533-12e23603-b33e-4f7f-9af5-4ccfe07a61fe.png)

Setelah menginputkan nama dan mengubah datanya maka data akan terubah.

## Untuk menghapus data, ketik perintah ```H```

Masukkan namanya untuk menghapus data

![prak7-5](https://user-images.githubusercontent.com/115516473/205432039-61f36544-ad7d-4276-b0f7-db10d86ed6bb.png)

## Dan yang terakhir, gunakan perintah ```K``` untuk keluar dari program 

![prak7-6](https://user-images.githubusercontent.com/115516473/205432161-6c7ff00e-0c26-4cc6-a9d5-f1e4bfb74434.png)

## Flowchartnya sebagai berikut 

![Flowchart prak7](https://user-images.githubusercontent.com/115516473/205432257-11c5fb58-6821-4ab3-9b54-aa3ed6c43bd1.png)
