# **Praktikum6.1**
## **PROGRAM INPUT NILAI MAHASISWA MENGGUNAKAN FUNGSI**

```sh
Nama   : Dhefi Nurkholik
NIM    : 312210414
Matkul : Bahas Pemograman
```

## **DESKRIPSI**

1. Deklarasi dictionary dengan nama _dataMahasiswa_ untuk menampung semua data/element.
2. gunakan fungsi _def tambah()_ di isi dengan inputan nama, nim, tugas, uts, uas dan perhitungan nilai akhir untuk dan di masukan ke dictonary _dataMahasiswa_.
3. gunakan fungsi _def tampilkan()_ di isi dengan cetak isi dari dictonary.
4. gunakan fungsi _def hapus(nama)_ di isi dengan syntax delet untuk menghapus element _nama_ pada dictonary _dataMahasiswa_.
5. gunakan fungsi _def ubah(nama)_ di isi dengan inputan _nama_ dan mengubah isi element pada _nama_ tersebut.
6. gunakan _while True_ untuk menlooping/mengulang statment.
7. gunakan statment _if, elif, else,_ di dalam _while True_ dan panggil fungsi dari masing masing fungsi, contoh:
```sh
tambah()
tampilkan()
hapus(nama)
ubah(nama)
```

## **FLOWCHART**

![flowchart](https://user-images.githubusercontent.com/115616418/205866916-95ec1039-9e02-402f-b12a-75092d229573.jpg)

## **PROGRAM**
```SH
dataMahasiswa = {}

print("=" * 65)
print("|\tPROGRAM INPUT NILAI MAHASISWA MENGGUNAKAN FUNGSI\t|")
print("=" * 65)


def tambah():
        nama = str(input("Masukan Nama : "))
        nim = int(input("Masukan Nim   : "))
        tugas = int(input("Masukan Nilai Tugas : "))
        uts = int(input("Masukan Nilai UTS     : "))
        uas = int(input("Masukan Nilai UAS     : "))
        akhir = (tugas / 3) + (uts / 3.5) + (uas / 3.5)
        dataMahasiswa[nama] = nim, tugas, uts, uas, akhir,
        print("\nDATA BERHASIL DI TAMBAHKAN!")
def tampilkan():
        print("=" * 69)
        print("|" + "\t" * 3 + "DAFTAR NILAI MAHASISWA" + "\t" * 3 +
                  "    |")
        print("=" * 69)
        print("| NO |   \tNAMA\t   |\tNIM \t| TUGAS | UTS | UAS | AKHIR |")
        print("=" * 69)
        no = 0
        for tampil in dataMahasiswa.items():
            no += 1
            print("| {6:2} |\t {0:15}   | {1:9} \t| {2:5} | {3:3} | {4:3} | {5:5} |".format(tampil[0], tampil[1][0], tampil[1][1], tampil[1][2], tampil[1][3],"%.2f" % float(tampil[1][4]), no))
            print("=" * 69)
def hapus(nama):
            del dataMahasiswa[nama]
            print("DATA BERHASIL DI HAPUS!")
 
def ubah(nama):
        if nama in dataMahasiswa.keys():
            nim = int(input("Masukan Nim  : "))
            tugas = int(input("Masukan Nilai Tugas : "))
            uts = int(input("Masukan Nilai UTS     : "))
            uas = int(input("Masukan Nilai UAS     : "))
            akhir = (tugas / 3) + (uts / 3.5) + (uas / 3.5)
            dataMahasiswa[nama] = nim, tugas, uts, uas, akhir
            print("\nDATA BERHASIL DI UBAH!")
        else:
            print("\DATA TIDAK DI TEMUKAN!")

while True:
    data = input(
        "\n 1 - Tambah Data,\t 2 - Tampilkan Data,\t 3 - Hapus Data,\t 4 - Ubah Data, 5 - Keluar \n : "
    )
    if (data.lower() == '1'):
        tambah()

    elif (data.lower() == '4'):
        nama = str(input("Masukan Nama : "))
        ubah(nama)
    elif (data.lower() == '3'):
        nama = str(input("Masukan Nama : "))
        if nama in dataMahasiswa:
            hapus(nama)
        else:
            print("DATA TIDAK DI TEMUKAN ".format(nama))
    elif (data.lower() == '2'):
        if dataMahasiswa.items():
            tampilkan()
        else:
            print("=" * 69)
            print("|" + "\t" * 3 + "DAFTAR NILAI MAHASISWA" + "\t" * 3 +
                  "    |")
            print("=" * 69)
            print("| NO |   \tNAMA\t   |\tNIM \t| TUGAS | UTS | UAS | AKHIR |")
            print("=" * 69)
            print("|    " + "\t" * 3 + "TIDAK ADA DATA!" + "\t" * 4 + "    |")
            print("=" * 69)
    elif (data.lower() == '5'):
        print("\nTERIMA KASIH! \n")
        exit()
    else:
        print("PILIHAN MENU TIDAK ADA!")
```

## **TAMPILAN PROGRAM**

![1](https://user-images.githubusercontent.com/115616418/205866259-fa62ca09-c504-48c6-b48f-e14353f4b7e3.png)

![2](https://user-images.githubusercontent.com/115616418/205866503-f0eee5fe-e33e-450f-8904-d09b536dbee9.png)

![3](https://user-images.githubusercontent.com/115616418/205866701-b109800e-5be5-4a94-b750-61846bcabeed.png)

![4](https://user-images.githubusercontent.com/115616418/205866790-09111f00-1d5a-44cf-8180-7870d2813dc5.png)

# **SELESAI**