# Pertemuan 11 Dictionary/Map dan Pasangan Key-Value

Nama: Amandita Pebriana Putri  
NIM: 2225250134  
Kelas: 3A Pendidikan Matematika  

## Tujuan
Memodelkan data pendidikan menggunakan struktur data dictionary dan pasangan key-value untuk melakukan pencarian, penambahan, pembaruan, serta rekapitulasi data mahasiswa berdasarkan identitas unik secara tepat, efisien, dan aman dari kesalahan akses.

## Struktur Data
Program ini menggunakan pendekatan dictionary bersarang (nested dictionary) dengan rincian sebagai berikut:
1. Key utama pada dictionary luar menggunakan Nomor Induk Mahasiswa (NIM) yang bersifat unik (misalnya "A001", "A002", dst.).
2. Value dari setiap key utama berupa dictionary di dalam yang memuat atribut informasi lengkap mahasiswa, meliputi:
   - "nama": Berisi string nama lengkap mahasiswa.
   - "kelas": Berisi string kode kelas mahasiswa.
   - "nilai": Berisi angka numerik (integer/float) nilai ujian mahasiswa.

## Cara Menjalankan
Buka terminal pada direktori utama proyek di VS Code, lalu jalankan perintah berikut:
python3 praktik/data_mahasiswa.py

## Algoritma Program
1. Mendefinisikan fungsi cari_mahasiswa(data, nim) yang memanfaatkan method .get(nim) untuk mencari data mahasiswa secara aman berdasarkan NIM tanpa memicu KeyError jika NIM tidak terdaftar.
2. Mendefinisikan fungsi rata_rata_nilai(data) untuk menghitung rata-rata nilai seluruh mahasiswa dengan menjumlahkan seluruh value nilai melalui perulangan .values() lalu membaginya dengan jumlah total data.
3. Mempersiapkan kamus data utama (data_mahasiswa) yang berisi data awal minimal 5 mahasiswa dengan atribut lengkap.
4. Menguji fungsi pencarian untuk kasus NIM yang tersedia di dalam dictionary maupun kasus NIM yang tidak tersedia.
5. Menambahkan data mahasiswa baru (misalnya "A006") ke dalam struktur dictionary menggunakan assignment langsung.
6. Melakukan pembaruan (update) pada nilai salah satu mahasiswa tertentu (misalnya mengubah nilai "A002").
7. Menelusuri seluruh isi dictionary menggunakan method .items() untuk menampilkan rekapitulasi data secara keseluruhan.
8. Menghitung dan menampilkan hasil akhir berupa nilai rata-rata kelas ke layar terminal.

## Test Case
| Kasus Pengujian | Input / Aksi | Hasil Utama yang Diharapkan | Status |
| :--- | :--- | :--- | :---: |
| Pencarian tersedia | A003 | Data lengkap mahasiswa dengan NIM A003 (Citra) berhasil ditampilkan | Sesuai |
| Pencarian tidak tersedia | A999 | Menampilkan pesan bahwa data tidak ditemukan dengan aman tanpa memicu KeyError | Sesuai |
| Pembaruan nilai | Nilai mahasiswa A002 diubah menjadi 82 | Nilai pada atribut dictionary mahasiswa A002 berhasil diperbarui menjadi 82 | Sesuai |
| Penambahan data | Menambahkan data baru dengan key A006 | Key A006 beserta atribut lengkapnya tersedia dan tercatat di dalam dictionary | Sesuai |
| Rekapitulasi data | Menggunakan method items() | Seluruh pasangan NIM dan informasi detail seluruh mahasiswa tampil secara berurutan | Sesuai |

## Refleksi
Dalam praktik pengolahan data menggunakan dictionary pada Pertemuan 11 ini, tantangan utama adalah menghindari kesalahan KeyError saat mengakses key yang belum didefinisikan atau salah ketik. Hal tersebut dapat diatasi secara optimal dengan memanfaatkan method .get() atau melakukan pengecekan keanggotaan menggunakan operator in. Penggunaan dictionary terbukti jauh lebih unggul dan natural dibandingkan list ketika kita perlu mencari atau memanipulasi data pendidikan berdasarkan pengenal unik seperti NIM, tanpa harus bergantung pada posisi indeks numerik.