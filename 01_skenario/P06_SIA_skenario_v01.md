# Tabel Skenario Sumber: SIA-UC08 dan SIA-UC09

Sumber langkah untuk Activity Diagram Input Nilai sampai Lihat KHS (`P06_2406122_SIA_activity_v01.drawio`).

## SIA-UC08 Input Nilai Mata Kuliah (aktor: Dosen)

| No | Kegiatan (aktor) | Respon sistem |
| --- | --- | --- |
| 1 | Dosen memasukkan nilai mata kuliah | |
| 2 | | Sistem menyimpan nilai |
| 3 | | Sistem memeriksa kelengkapan nilai |
| 3a (Alternative) | Jika nilai belum lengkap, Dosen melengkapi nilai mata kuliah yang belum lengkap | Alur kembali ke alur utama sebelum pengesahan |
| 4 | Admin Akademik memeriksa dan mengesahkan nilai | |
| 5 | | Sistem menyiapkan publikasi hasil studi |
| 6 | | Sistem menerbitkan KHS pada portal akademik (paralel dengan langkah 7) |
| 7 | | Sistem mengirim pemberitahuan hasil studi kepada mahasiswa (paralel dengan langkah 6) |

Skenario akhir: nilai sah, KHS terbit, dan mahasiswa menerima pemberitahuan.

## SIA-UC09 Lihat KHS (aktor: Mahasiswa)

| No | Kegiatan (aktor) | Respon sistem |
| --- | --- | --- |
| 1 | Mahasiswa melihat KHS | Sistem menampilkan KHS pada portal akademik |

Skenario akhir: mahasiswa telah melihat KHS.

## Keterlacakan action pada diagram

| Action pada diagram | Swimlane | Sumber langkah |
| --- | --- | --- |
| Memasukkan nilai mata kuliah | Dosen | SIA-UC08 langkah 1 |
| Menyimpan nilai | Sistem | SIA-UC08 langkah 2 |
| Decision Nilai sudah lengkap? [lengkap] / [belum lengkap] | Sistem | SIA-UC08 langkah 3 |
| Melengkapi nilai mata kuliah yang belum lengkap | Dosen | SIA-UC08 langkah 3a |
| Memeriksa dan mengesahkan nilai | Admin Akademik | SIA-UC08 langkah 4 |
| Menyiapkan publikasi hasil studi | Sistem | SIA-UC08 langkah 5 |
| Menerbitkan KHS pada portal akademik (setelah fork) | Sistem | SIA-UC08 langkah 6 |
| Mengirim pemberitahuan hasil studi kepada mahasiswa (setelah fork) | Sistem | SIA-UC08 langkah 7 |
| Melihat KHS | Mahasiswa | SIA-UC09 langkah 1 |
