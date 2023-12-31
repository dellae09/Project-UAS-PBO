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

## Source Code
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

<div align="center">
  
![Source Code Definisi Kelas dan Metode](https://github.com/dellae09/Project-UAS-PBO/assets/150639048/a58f7da4-2421-4187-a9d7-0a2c62731b3e)

<h5 align="center"> Gambar Source Code Definisi Kelas dan Metode </h5> 


![Source Code kedua](https://github.com/dellae09/Project-UAS-PBO/assets/150639048/eb45d8a2-b33b-4817-827e-59d01936034f)
<h5 align="center"> Gambar Source Code Tambah Objek dan menggunakan Objek + Metode </h5> 

</div>


## Penjelasan Kode

| Kode                                       | Penjelasan                                                                                                                       |
| ------------------------------------------ | ----------------------------------------------------------------------------------------------------------------------------     |
| **Kelas GPS**                              |                                                                                                                                  |
| 1. `class GPS:`                            | Mendefinisikan kelas GPS.                                                                                                        |
| 2. `def __init__(self, nama):`             | Metode konstruktor untuk inisialisasi objek GPS.                                                                                 |
| 3. `self.nama = nama`                      | Membuat atribut nama untuk objek GPS.                                                                                            |
| 4. `self.lokasi = []`                      | Membuat atribut lokasi sebagai list untuk menyimpan data lokasi.                                                                 |
| 5. `self.kecepatan = random.uniform(5, 20)`| Menghasilkan kecepatan acak untuk objek GPS.                                                                                     |
| **Metode tambah_lokasi**                   |                                                                                                                                  |
| 1. `def tambah_lokasi(self, lintang, bujur):` | Metode untuk menambahkan lokasi baru ke objek GPS.                                                                            |
| 2. `waktu_sekarang = datetime.now()`       | Mendapatkan waktu saat ini.                                                                                                      |
| 3. `lokasi_baru = {'waktu': waktu_sekarang, 'lintang': lintang, 'bujur': bujur, 'kecepatan': self.kecepatan}` | Membuat objek lokasi baru.                                    |
| 4. `self.lokasi.append(lokasi_baru)`       | Menambahkan lokasi baru ke dalam list lokasi objek GPS.                                                                          |
| **Metode info_migrasi**                    |                                                                                                                                  |
| 1. `def info_migrasi(self):`               | Metode untuk menampilkan informasi migrasi objek GPS.                                                                            |
| 2. `for lokasi in self.lokasi:`            | Melakukan iterasi untuk setiap lokasi dalam list lokasi.                                                                         |
| 3. `print(f"Terlacak: {lokasi['waktu']}, Lintang: {lokasi['lintang']}, Bujur: {lokasi['bujur']}, Kecepatan: {lokasi['kecepatan']} m/s")` | Menampilkan informasi lokasi.      |
| **Membuat Objek Kenari dan Elang**         |                                                                                                                                  |
| 1. `kenari = GPS("Kenari")`                | Membuat objek GPS dengan nama "Kenari".                                                                                          |
| 2. `elang = GPS("Elang")`                  | Membuat objek GPS dengan nama "Elang".                                                                                           |
| **Loop untuk Memasukkan Data Lokasi ke Objek Kenari dan Elang** |                                                                                                             |
| 1. `for _ in range(5):`                    | Loop untuk melakukan 5 iterasi.                                                                                                  |
| 2. `lintang = random.uniform(-90, 90)`     | Menghasilkan lintang acak antara -90 dan 90.                                                                                     |
| 3. `bujur = random.uniform(-180, 180)`     | Menghasilkan bujur acak antara -180 dan 180.                                                                                     |
| 4. `kenari.tambah_lokasi(lintang, bujur)`  | Memanggil metode tambah_lokasi untuk objek Kenari.                                                                               |
| 5. `lintang = random.uniform(-90, 90)`     | Menghasilkan lintang acak antara -90 dan 90.                                                                                     |
| 6. `bujur = random.uniform(-180, 180)`     | Menghasilkan bujur acak antara -180 dan 180.                                                                                     |
| 7. `elang.tambah_lokasi(lintang, bujur)`   | Memanggil metode tambah_lokasi untuk objek Elang.                                                                                |
| **Menampilkan Informasi Migrasi Objek Kenari dan Elang** |                                                                                                                    |
| 1. `kenari.info_migrasi()`                 | Menampilkan informasi migrasi untuk objek Kenari.                                                                                |
| 2. `print("\n" + "=" * 40 + "\n")`         | Mencetak garis pemisah.                                                                                                          |
| 3. `elang.info_migrasi()`                  | Menampilkan informasi migrasi untuk objek Elang.                                                                                 |



## Penjelasan Keseluruhan 
- Kelas GPS
- Inisialisasi:
1. Deskripsi: Konstruktor __init__ digunakan untuk inisialisasi objek GPS.
- Atribut:
1. nama: Menyimpan nama objek GPS.
2. lokasi: List untuk menyimpan data lokasi.
3. kecepatan: Menyimpan kecepatan objek GPS.

- Metode tambah_lokasi:
1. Deskripsi: Menambahkan lokasi baru ke dalam list lokasi.
- Parameter:
1. lintang: Koordinat lintang lokasi.
2. bujur: Koordinat bujur lokasi.
- Langkah-langkah:
1. Membuat timestamp waktu sekarang.
2. Membuat dictionary lokasi baru dengan informasi waktu, lintang, bujur, dan kecepatan.
3. Menambahkan lokasi baru ke dalam list lokasi objek GPS.

- Metode info_migrasi:
1. Deskripsi: Menampilkan informasi migrasi objek GPS.
- Langkah-langkah:
1. Menampilkan detail migrasi, termasuk nama burung.
2. Iterasi melalui list lokasi dan menampilkan informasi setiap lokasi seperti waktu, lintang, bujur, dan kecepatan.
3. Penggunaan Objek dan Metode

- Membuat Objek Kenari dan Elang:
- Langkah-langkah:
1. Membuat objek GPS dengan nama "Kenari" dan "Elang" menggunakan konstruktor.
2. Setiap objek memiliki atribut nama, lokasi awal kosong, dan kecepatan acak.
3. Loop untuk Memasukkan Data Lokasi:
- Langkah-langkah:
1. Melakukan loop 5 kali untuk menghasilkan data lokasi acak.
2. Setiap iterasi, menghasilkan lintang dan bujur acak.
3. Memanggil metode tambah_lokasi pada objek Kenari dan Elang untuk menambahkan lokasi baru.

- Menampilkan Informasi Migrasi:
- Langkah-langkah:
1. Memanggil metode info_migrasi pada objek Kenari dan Elang untuk menampilkan informasi migrasi.
2. Mencetak garis pemisah antara informasi migrasi Kenari dan Elang.
3. Keseluruhan Program:
4. Membuat dua objek GPS yang mewakili burung Kenari dan Elang.
5. Menggunakan metode untuk menambahkan lokasi dan menampilkan informasi migrasi.


## OUTPUT
<div align="center">

![Output](https://github.com/dellae09/Project-UAS-PBO/assets/150639048/8de1c644-e542-4c78-abed-05977e36facb)
<h5 align="center"> Gambar Output  </h5> 

| Kode                                       | Penjelasan                                                                                               |
| ------------------------------------------ | -------------------------------------------------------------------------------------------------------- |
| **Detail Migrasi Burung Kenari:**               |                                                                                                     |
| **Data Lokasi 1:**                             |                                                                                                      |
| - Terlacak: 2023-12-14 14:35:34.120202     | Waktu terlacak lokasi 1                                                                                  |
| - Lintang: -60.72062469287152              | Koordinat lintang lokasi 1                                                                               |
| - Bujur: 39.41639078895179                 | Koordinat bujur lokasi 1                                                                                 |
| - Kecepatan: 9.352884316138262 m/s         | Kecepatan pada lokasi 1                                                                                  |
| **Data Lokasi 2:**                             |                                                                                                      |
| - Terlacak: 2023-12-14 14:35:34.120215     | Waktu terlacak lokasi 2                                                                                  |
| - Lintang: 82.33416391213899              | Koordinat lintang lokasi 2                                                                                |
| - Bujur: -10.284229301175287               | Koordinat bujur lokasi 2                                                                                 |
| - Kecepatan: 9.352884316138262 m/s         | Kecepatan pada lokasi 2                                                                                  |
| **Data Lokasi 3:**                             |                                                                                                      |
| - Terlacak: 2023-12-14 14:35:34.120220     | Waktu terlacak lokasi 3                                                                                  |
| - Lintang: -37.742390698429844             | Koordinat lintang lokasi 3                                                                               |
| - Bujur: 143.06626296485575               | Koordinat bujur lokasi 3                                                                                  |
| - Kecepatan: 9.352884316138262 m/s         | Kecepatan pada lokasi 3                                                                                  |
| **Data Lokasi 4:**                             |                                                                                                      |
| - Terlacak: 2023-12-14 14:35:34.120225     | Waktu terlacak lokasi 4                                                                                  |
| - Lintang: 56.952050102899165              | Koordinat lintang lokasi 4                                                                               |
| - Bujur: -24.90889131085578                | Koordinat bujur lokasi 4                                                                                 |
| - Kecepatan: 9.352884316138262 m/s         | Kecepatan pada lokasi 4                                                                                  |
| **Data Lokasi 5:**                             |                                                                                                      |
| - Terlacak: 2023-12-14 14:35:34.120230     | Waktu terlacak lokasi 5                                                                                  |
| - Lintang: 11.981056892750743              | Koordinat lintang lokasi 5                                                                               |
| - Bujur: -72.29659801884829                | Koordinat bujur lokasi 5                                                                                 |
| - Kecepatan: 9.352884316138262 m/s         | Kecepatan pada lokasi 5                                                                                  |
| **Detail Migrasi Burung Elang:**               |                                                                                                      |
| **Data Lokasi 1:**                             |                                                                                                      |
| - Terlacak: 2023-12-14 14:35:34.120212     | Waktu terlacak lokasi 1                                                                                  |
| - Lintang: -21.653472661317693             | Koordinat lintang lokasi 1                                                                               |
| - Bujur: 164.0752065836174                | Koordinat bujur lokasi 1                                                                                  |
| - Kecepatan: 6.395231733395626 m/s         | Kecepatan pada lokasi 1                                                                                  |
| **Data Lokasi 2:**                             |                                                                                                      |
| - Terlacak: 2023-12-14 14:35:34.120218     | Waktu terlacak lokasi 2                                                                                  |
| - Lintang: 64.31437804447896              | Koordinat lintang lokasi 2                                                                                |
| - Bujur: -91.65467080600179               | Koordinat bujur lokasi 2                                                                                  |
| - Kecepatan: 6.395231733395626 m/s         | Kecepatan pada lokasi 2                                                                                  |
| **Data Lokasi 3:**                             |                                                                                                      |
| - Terlacak: 2023-12-14 14:35:34.120223     | Waktu terlacak lokasi 3                                                                                  |
| - Lintang: 63.38029909727001              | Koordinat lintang lokasi 3                                                                                |
| - Bujur: -67.31120148573126               | Koordinat bujur lokasi 3                                                                                  |
| - Kecepatan: 6.395231733395626 m/s         | Kecepatan pada lokasi 3                                                                                  |
| **Data Lokasi 4:**                             |                                                                                                      |
| - Terlacak: 2023-12-14 14:35:34.120227     | Waktu terlacak lokasi 4                                                                                  |
| - Lintang: -44.780549616579904             | Koordinat lintang lokasi 4                                                                               |
| - Bujur: 159.80512620810566               | Koordinat bujur lokasi 4                                                                                  |
| - Kecepatan: 6.395231733395626 m/s         | Kecepatan pada lokasi 4                                                                                  |
|**Data Lokasi 5:**                             |                                                                                                       |
| - Terlacak: 2023-12-14 14:35:34.120232     | Waktu terlacak lokasi 5                                                                                  |
| - Lintang: 10.355233485485556              | Koordinat lintang lokasi 5                                                                               |
| - Bujur: -113.24980300564681               | Koordinat bujur lokasi 5                                                                                 |
| - Kecepatan: 6.395231733395626 m/s         | Kecepatan pada lokasi 5                                                                                  |



</div>

### Penjelasan Output:
Output tersebut adalah hasil dari pemanggilan metode `info_migrasi` pada objek Kenari dan Elang setelah data lokasi ditambahkan melalui loop. 
- Setiap baris mewakili satu data lokasi yang mencakup informasi seperti waktu terlacak, lintang, bujur, dan kecepatan.
- Objek Kenari dan Elang memiliki kecepatan yang sama untuk setiap data lokasi, karena kecepatan diinisialisasi saat objek dibuat.
- Output ini memberikan informasi terstruktur mengenai pergerakan migrasi dari setiap burung selama waktu tertentu.

