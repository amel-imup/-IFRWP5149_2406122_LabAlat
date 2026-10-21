<!-- skenario -->
Mahasiswa dan dosen sama-sama merupakan Civitas Akademika yang 
dapat melihat kalender akademik. Dosen menginput nilai mata kuliah yang 
diampunya setelah masa perkuliahan berakhir. Mahasiswa melihat Kartu 
Hasil Studi (KHS) untuk semester yang nilainya sudah dipublikasikan. Admin 
Akademik mengelola data mahasiswa: menambah data mahasiswa baru, 
mengubah data mahasiswa, dan menghapus data mahasiswa. Dua use case 
utama, Input Nilai Mata Kuliah dan Lihat KHS, ditunjukkan realisasinya oleh 
collaboration yang bersesuaian.

<!-- Batas dan asumsi  -->
• Kode kebutuhan dimulai dari SIA-R07 agar SIA-R01 dan SIA-R02 
(Pertemuan 2) serta SIA-R03 sampai SIA-R06 (Pertemuan 3) tetap 
mempunyai identitas berbeda. 
• Pengguna telah terautentikasi dan memiliki hak akses sesuai peran. 
• Kalender akademik pada tugas ini adalah agenda resmi institusi (awal 
semester, batas KRS, masa ujian, dan sejenisnya); jangan 
menyamakannya dengan jadwal kuliah pada Pertemuan 2. 
• Nilai hanya dapat diinput oleh dosen pengampu mata kuliah tersebut. Nilai 
yang diinput belum terpublikasi sebelum dinyatakan resmi oleh ketentuan 
tugas ini: KHS hanya menampilkan nilai yang sudah dipublikasikan. 
• Hapus Data Mahasiswa hanya untuk mahasiswa yang tidak memiliki data 
akademik aktif. Ketentuan ini fiktif untuk latihan. 
• Pengajuan KRS tetap digambar sebagai bagian diagram kumulatif dari 
Pertemuan 3. Pembayaran dan perancangan basis data berada di luar 
tugas ini.

<!-- Katalog Use Case Kumulatif -->
### Tabel Katalog Use Case Sistem Informasi Akademik

| ID Use Case | Nama Use Case | Aktor | Keterangan |
|---|---|---|---|
| SIA-UC01 | Lihat Jadwal Kuliah | Mahasiswa | Dipertahankan dari Pertemuan 2. |
| SIA-UC02 | Kelola Jadwal Kuliah | Dosen Wali | Dipertahankan dari Pertemuan 2. |
| SIA-UC03 | Ajukan KRS | Mahasiswa | Dipertahankan dari Pertemuan 3. |
| SIA-UC04 | Validasi KRS | Dosen Wali | Dipertahankan dari Pertemuan 3. |
| SIA-UC05 | Unduh Bukti Pengajuan KRS | Mahasiswa | Dipertahankan dari Pertemuan 3. |
| SIA-UC06 | Proses Keputusan KRS | Dosen Wali | Dipertahankan dari Pertemuan 3. |
| SIA-UC07 | Lihat Kalender Akademik | Civitas Akademika | Use case baru Pertemuan 4; diwarisi Mahasiswa dan Dosen. |
| SIA-UC08 | Input Nilai Mata Kuliah | Dosen | Use case baru Pertemuan 4. |
| SIA-UC09 | Lihat KHS | Mahasiswa | Use case baru Pertemuan 4. |
| SIA-UC10 | Kelola Data Mahasiswa | Admin Akademik | Use case umum untuk pengelolaan data mahasiswa. |
| SIA-UC11 | Tambah Data Mahasiswa | Admin Akademik | Generalization dari SIA-UC10. |
| SIA-UC12 | Ubah Data Mahasiswa | Admin Akademik | Generalization dari SIA-UC10. |
| SIA-UC13 | Hapus Data Mahasiswa | Admin Akademik | Generalization dari SIA-UC10. |

### Catatan
1. SIA-UC01 sampai SIA-UC06 dipertahankan dari pertemuan sebelumnya.
2. SIA-UC07 sampai SIA-UC13 merupakan penambahan pada Pertemuan 4.
3. SIA-UC07 dihubungkan dengan aktor umum Civitas Akademika. Mahasiswa dan Dosen mewarisi fungsi tersebut melalui generalization.
4. SIA-UC11, SIA-UC12, dan SIA-UC13 merupakan use case khusus dari SIA-UC10 Kelola Data Mahasiswa.
5. Nama aktor dan hubungan untuk SIA-UC01 sampai SIA-UC06 perlu disesuaikan dengan diagram Pertemuan 2 dan 3 yang sudah kamu buat.


<!-- generalization aktor -->
| Aktor Khusus | Aktor Umum | Hubungan |
|---|---|---|
| Mahasiswa | Civitas Akademika | Generalization |
| Dosen | Civitas Akademika | Generalization |

<!-- generalization use case  -->
| ID Use Case | Nama Use Case Khusus | Use Case Umum | Perilaku Pembeda |
|---|---|---|---|
| SIA-UC11 | Tambah Data Mahasiswa | SIA-UC10 Kelola Data Mahasiswa | Admin Akademik menambahkan data mahasiswa baru ke dalam sistem. |
| SIA-UC12 | Ubah Data Mahasiswa | SIA-UC10 Kelola Data Mahasiswa | Admin Akademik memperbarui informasi mahasiswa yang sudah tersimpan di dalam sistem. |
| SIA-UC13 | Hapus Data Mahasiswa | SIA-UC10 Kelola Data Mahasiswa | Admin Akademik menghapus data mahasiswa dari sistem sesuai ketentuan yang berlaku. |

<!-- Tetapkan Collaboration  -->

| ID Collaboration | Nama Collaboration | Use Case yang Direalisasikan |
|---|---|---|
| SIA-CO01 | Input Nilai Mata Kuliah | SIA-UC08 Input Nilai Mata Kuliah |
| SIA-CO02 | Lihat KHS | SIA-UC09 Lihat KHS |

