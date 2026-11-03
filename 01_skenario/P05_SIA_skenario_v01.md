# SKENARIO USE CASE SIA
## PRAKTIKUM PERTEMUAN 5

**NIM:** 2406122  
**Nama:** Ina Amelia Cantika  
**Mata Kuliah:** Sistem Informasi Akademik (SIA)

---

## SIA-UC07 — Lihat Kalender Akademik

**ID Use Case:** SIA-UC07  
**Nama Use Case:** Lihat Kalender Akademik  
**Aktor:** Civitas Akademika (Mahasiswa dan Dosen)

**Tujuan:**
Civitas Akademika dapat melihat informasi kalender akademik yang berlaku.

**Deskripsi:**
Civitas Akademika membuka halaman kalender akademik untuk melihat informasi kegiatan akademik berdasarkan periode yang tersedia.

**Skenario Normal:**

| Kegiatan Aktor | Respon Sistem |
|---|---|
| 1. Civitas Akademika membuka menu Kalender Akademik. | 2. Sistem menampilkan daftar periode kalender akademik. |
| 3. Civitas Akademika memilih periode akademik. | 4. Sistem menampilkan kalender akademik sesuai periode yang dipilih. |
| 5. Civitas Akademika memilih salah satu kegiatan akademik. | 6. Sistem menampilkan detail kegiatan, tanggal, dan keterangan kegiatan. |

**Skenario Alternatif:**

| Kegiatan Aktor | Respon Sistem |
|---|---|
| 7. Civitas Akademika memilih periode yang belum memiliki kalender akademik. | 8. Sistem menampilkan pesan bahwa kalender akademik belum tersedia. |

**Skenario Akhir:**

Civitas Akademika berhasil melihat kalender akademik beserta detail kegiatannya. Jika kalender belum tersedia, sistem menampilkan pemberitahuan.

---

## SIA-UC08 — Input Nilai Mata Kuliah

**ID Use Case:** SIA-UC08  
**Nama Use Case:** Input Nilai Mata Kuliah  
**Aktor:** Dosen

**Tujuan:**
Dosen dapat memasukkan nilai mahasiswa pada mata kuliah yang diampunya.

**Deskripsi:**
Dosen membuka daftar mata kuliah yang diampu, memilih mata kuliah, kemudian memasukkan nilai mahasiswa sesuai ketentuan yang berlaku.

**Skenario Normal:**

| Kegiatan Aktor | Respon Sistem |
|---|---|
| 1. Dosen membuka menu Input Nilai Mata Kuliah. | 2. Sistem menampilkan daftar mata kuliah yang diampu dosen. |
| 3. Dosen memilih salah satu mata kuliah. | 4. Sistem memeriksa hak akses dosen terhadap mata kuliah tersebut. |
| 5. Dosen memasukkan nilai mahasiswa. | 6. Sistem memeriksa validitas nilai yang dimasukkan. |
| 7. Dosen menyimpan nilai mahasiswa. | 8. Sistem menyimpan nilai dan menampilkan konfirmasi berhasil. |

**Skenario Alternatif:**

| Kegiatan Aktor | Respon Sistem |
|---|---|
| 9. Dosen yang bukan pengampu mencoba memasukkan nilai. | 10. Sistem menolak akses dan menampilkan pesan bahwa dosen tidak memiliki hak input nilai. |
| 11. Dosen memasukkan nilai di luar rentang yang sah. | 12. Sistem menolak nilai dan meminta dosen memasukkan nilai yang sesuai. |
| 13. Dosen memasukkan data nilai yang tidak lengkap. | 14. Sistem menampilkan pesan kesalahan dan meminta data dilengkapi. |

**Skenario Akhir:**

Nilai mahasiswa berhasil disimpan apabila dosen memiliki hak akses dan nilai memenuhi ketentuan. Jika tidak, sistem menolak penyimpanan.

**Collaboration:** SIA-CO01 Input Nilai Mata Kuliah.

---

## SIA-UC09 — Lihat KHS

**ID Use Case:** SIA-UC09  
**Nama Use Case:** Lihat KHS  
**Aktor:** Mahasiswa

**Tujuan:**
Mahasiswa dapat melihat Kartu Hasil Studi (KHS) berdasarkan semester yang dipilih.

**Deskripsi:**
Mahasiswa membuka menu KHS untuk melihat hasil studi yang telah dipublikasikan oleh pihak akademik.

**Skenario Normal:**

| Kegiatan Aktor | Respon Sistem |
|---|---|
| 1. Mahasiswa membuka menu Lihat KHS. | 2. Sistem menampilkan daftar semester yang tersedia. |
| 3. Mahasiswa memilih semester yang ingin dilihat. | 4. Sistem mengambil data nilai yang telah dipublikasikan. |
| 5. Mahasiswa melihat KHS semester yang dipilih. | 6. Sistem menampilkan daftar mata kuliah dan nilai yang telah dipublikasikan. |

**Skenario Alternatif:**

| Kegiatan Aktor | Respon Sistem |
|---|---|
| 7. Mahasiswa memilih semester yang nilainya belum dipublikasikan. | 8. Sistem menampilkan pesan bahwa KHS belum tersedia. |
| 9. Mahasiswa memilih semester yang tidak memiliki data KHS. | 10. Sistem menampilkan pesan bahwa data KHS tidak ditemukan. |

**Skenario Akhir:**

Mahasiswa berhasil melihat KHS apabila data nilai telah dipublikasikan. Jika belum tersedia, sistem menampilkan pemberitahuan.

**Collaboration:** SIA-CO02 Lihat KHS.

---

## SIA-UC10 — Kelola Data Mahasiswa

**ID Use Case:** SIA-UC10  
**Nama Use Case:** Kelola Data Mahasiswa  
**Aktor:** Admin Akademik

**Tujuan:**
Admin Akademik dapat mengelola data mahasiswa melalui fungsi tambah, ubah, dan hapus data.

**Deskripsi:**
Admin Akademik membuka menu pengelolaan data mahasiswa dan memilih tindakan yang diperlukan.

**Skenario Normal:**

| Kegiatan Aktor | Respon Sistem |
|---|---|
| 1. Admin Akademik membuka menu Kelola Data Mahasiswa. | 2. Sistem menampilkan daftar data mahasiswa. |
| 3. Admin Akademik memilih fungsi tambah, ubah, atau hapus. | 4. Sistem menampilkan fungsi pengelolaan yang dipilih. |
| 5. Admin Akademik melakukan tindakan pengelolaan. | 6. Sistem memeriksa data yang dimasukkan atau tindakan yang dilakukan. |
| 7. Admin Akademik menyimpan perubahan. | 8. Sistem menyimpan perubahan dan menampilkan konfirmasi berhasil. |

**Skenario Alternatif:**

| Kegiatan Aktor | Respon Sistem |
|---|---|
| 9. Admin Akademik memasukkan data yang tidak lengkap atau tidak sah. | 10. Sistem menolak penyimpanan dan menampilkan pesan kesalahan. |

**Skenario Akhir:**

Pengelolaan data mahasiswa berhasil dilakukan sesuai fungsi yang dipilih. Jika terdapat kesalahan, sistem menolak perubahan.

---

## SIA-UC11 — Tambah Data Mahasiswa

**ID Use Case:** SIA-UC11  
**Nama Use Case:** Tambah Data Mahasiswa  
**Aktor:** Admin Akademik

**Tujuan:**
Admin Akademik dapat menambahkan data mahasiswa baru ke dalam sistem.

**Deskripsi:**
Admin Akademik memasukkan informasi mahasiswa baru dan menyimpan data tersebut.

**Skenario Normal:**

| Kegiatan Aktor | Respon Sistem |
|---|---|
| 1. Admin Akademik memilih fungsi Tambah Data Mahasiswa. | 2. Sistem menampilkan formulir penambahan data mahasiswa. |
| 3. Admin Akademik mengisi data mahasiswa baru. | 4. Sistem memeriksa kelengkapan dan keabsahan data. |
| 5. Admin Akademik menyimpan data mahasiswa. | 6. Sistem menyimpan data dan menampilkan konfirmasi berhasil. |

**Skenario Alternatif:**

| Kegiatan Aktor | Respon Sistem |
|---|---|
| 7. Admin Akademik mengisi data yang tidak lengkap. | 8. Sistem menolak penyimpanan dan meminta data dilengkapi. |
| 9. Admin Akademik memasukkan data yang tidak sah. | 10. Sistem menampilkan pesan kesalahan dan meminta data diperbaiki. |

**Skenario Akhir:**

Data mahasiswa baru berhasil ditambahkan apabila seluruh data telah memenuhi ketentuan. Jika tidak, sistem menolak penyimpanan.

**Relasi:** Generalization dari SIA-UC10 Kelola Data Mahasiswa.

---

## SIA-UC12 — Ubah Data Mahasiswa

**ID Use Case:** SIA-UC12  
**Nama Use Case:** Ubah Data Mahasiswa  
**Aktor:** Admin Akademik

**Tujuan:**
Admin Akademik dapat mengubah informasi data mahasiswa yang sudah tersimpan dalam sistem.

**Deskripsi:**
Admin Akademik memilih data mahasiswa yang akan diperbarui, mengubah informasi yang diperlukan, kemudian menyimpan perubahan.

**Skenario Normal:**

| Kegiatan Aktor | Respon Sistem |
|---|---|
| 1. Admin Akademik memilih fungsi Ubah Data Mahasiswa. | 2. Sistem menampilkan daftar data mahasiswa. |
| 3. Admin Akademik memilih data mahasiswa yang akan diubah. | 4. Sistem menampilkan informasi mahasiswa yang dipilih. |
| 5. Admin Akademik mengubah informasi data mahasiswa. | 6. Sistem memeriksa kelengkapan dan keabsahan perubahan data. |
| 7. Admin Akademik menyimpan perubahan. | 8. Sistem memperbarui data mahasiswa dan menampilkan konfirmasi berhasil. |

**Skenario Alternatif:**

| Kegiatan Aktor | Respon Sistem |
|---|---|
| 9. Data mahasiswa yang dipilih tidak ditemukan. | 10. Sistem menampilkan pesan bahwa data mahasiswa tidak ditemukan. |
| 11. Admin Akademik memasukkan perubahan yang tidak lengkap atau tidak sah. | 12. Sistem menolak perubahan dan meminta data diperbaiki. |

**Skenario Akhir:**

Data mahasiswa berhasil diperbarui apabila data ditemukan dan perubahan memenuhi ketentuan. Jika tidak, sistem tidak mengubah data sebelumnya.

**Relasi:** Generalization dari SIA-UC10 Kelola Data Mahasiswa.

---

## SIA-UC13 — Hapus Data Mahasiswa

**ID Use Case:** SIA-UC13  
**Nama Use Case:** Hapus Data Mahasiswa  
**Aktor:** Admin Akademik

**Tujuan:**
Admin Akademik dapat menghapus data mahasiswa yang tidak memiliki data akademik aktif.

**Deskripsi:**
Admin Akademik memilih data mahasiswa yang akan dihapus. Sistem memeriksa apakah mahasiswa masih memiliki data akademik aktif sebelum melakukan penghapusan.

**Skenario Normal:**

| Kegiatan Aktor | Respon Sistem |
|---|---|
| 1. Admin Akademik memilih fungsi Hapus Data Mahasiswa. | 2. Sistem menampilkan daftar data mahasiswa. |
| 3. Admin Akademik memilih data mahasiswa yang akan dihapus. | 4. Sistem menampilkan informasi data mahasiswa. |
| 5. Admin Akademik mengonfirmasi penghapusan. | 6. Sistem memeriksa apakah mahasiswa memiliki data akademik aktif. |
| 7. Admin Akademik melanjutkan penghapusan jika tidak ada data akademik aktif. | 8. Sistem menghapus data mahasiswa dan menampilkan konfirmasi berhasil. |

**Skenario Alternatif:**

| Kegiatan Aktor | Respon Sistem |
|---|---|
| 9. Data mahasiswa yang dipilih tidak ditemukan. | 10. Sistem menampilkan pesan bahwa data mahasiswa tidak ditemukan. |
| 11. Mahasiswa masih memiliki data akademik aktif. | 12. Sistem menolak penghapusan dan menampilkan pesan bahwa data mahasiswa masih memiliki data akademik aktif. |

**Skenario Akhir:**

Data mahasiswa berhasil dihapus apabila tidak memiliki data akademik aktif. Jika masih memiliki data akademik aktif, sistem menolak penghapusan.

**Relasi:** Generalization dari SIA-UC10 Kelola Data Mahasiswa.

---

## PENUTUP

Dokumen ini berisi skenario use case Sistem Informasi Akademik (SIA) Pertemuan 5, mulai dari SIA-UC07 sampai SIA-UC13.

Setiap use case memiliki skenario normal, skenario alternatif, dan skenario akhir untuk menggambarkan interaksi antara aktor dengan sistem.