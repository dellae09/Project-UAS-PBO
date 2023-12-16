<h1 align="center">PROJECT UAS PBO 👋</h1>

# _Program Migrasi Burung Menggunakan Python_ 

<img align="right" height="150" src="https://i.imgflip.com/65efzo.gif"  />

<h3 align="left"> ANGGOTA KELOMPOK </h3>

   - Nama  : Della Erlina 
     <h5 align="left"> NPM   : G1F022019</h5>
   - Nama  : Diamond Panca Lady
     <h5 align="left"> NPM   : G1F022027</h5>

  - Prodi : Sistem Informasi
  - Fakultas Teknik Universitas Bengkulu
  
## Tugas Project
Buatlah program sederhana dengan menggunakan python  bagaimana konsep OOP diterapkan pada pemrograman tersebut. Program yang dipilih yaitu Migrasi burung dilacak menggunakan Python: Peneliti menggunakan modul GPS untuk melacak hewan seperti kapan dan ke bagian mana mereka bepergian. Kumpulan data Python memberikan detail lokasi menggunakan GPS dan memberikan gambaran tentang tanggal, waktu, lintang, bujur, dan kecepatan burung.

## Pembahasan Project 
- Konsep OOP

1.1 Kode Import Modul
```sh
import random
from datetime import datetime, timedelta
```

1.2 Kode Kelas ( GPS )
```sh
class GPS:
    def __init__(self, nama):
        self.nama = nama
        self.lokasi = []
        self.kecepatan = random.uniform(5, 20)
```
1.3 Kode Metode (tambah_lokasi)
```sh
def tambah_lokasi(self, lintang, bujur):
        waktu_sekarang = datetime.now()
        lokasi_baru = {
            'waktu': waktu_sekarang,
            'lintang': lintang,
            'bujur': bujur,
            'kecepatan': self.kecepatan
        }
        self.lokasi.append(lokasi_baru)
```
1.4 Kode Metode (info_lokasi)
```sh
def info_migrasi(self):
        print(f"Detail Migrasi Burung {self.nama}:")
        for lokasi in self.lokasi:
            print(f"Terlacak: {lokasi['waktu']}, Lintang: {lokasi['lintang']}, Bujur: {lokasi['bujur']}, Kecepatan: {lokasi['kecepatan']} m/s")
```

1.5 Kode Membuat Obejek
```sh
kenari = GPS("Kenari")
elang = GPS("Elang")
```
1.6 Kode Menggunakan Objek dan Metode
```sh
for _ in range(5):
    lintang = random.uniform(-90, 90)
    bujur = random.uniform(-180, 180)
    kenari.tambah_lokasi(lintang, bujur)

    lintang = random.uniform(-90, 90)
    bujur = random.uniform(-180, 180)
    elang.tambah_lokasi(lintang, bujur)
```
1.5 Kode konsep encapsulation 
```sh
kenari.info_migrasi()
print("\n" + "=" * 40 + "\n")
elang.info_migrasi()
```



