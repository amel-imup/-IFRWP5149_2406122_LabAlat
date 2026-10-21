<!-- Use Case Description -->

| Elemen | Deskripsi |
|---|---|
| ID Use Case | SIA-UC08 |
| Nama Use Case | Input Nilai Mata Kuliah |
| Aktor Utama | Dosen |
| Tujuan | Memasukkan nilai mahasiswa untuk mata kuliah yang diampu oleh dosen. |
| Pemicu | Dosen memilih fungsi Input Nilai Mata Kuliah setelah masa perkuliahan berakhir. |
| Prasyarat | Dosen telah login ke sistem dan merupakan dosen pengampu mata kuliah yang akan diinput nilainya. |
| Pascakondisi Berhasil | Nilai yang valid berhasil disimpan ke dalam sistem untuk mata kuliah terkait. |
| Pascakondisi Gagal | Nilai tidak tersimpan dan data nilai yang sebelumnya ada tidak berubah. |
| Collaboration | SIA-CO01 — Input Nilai Mata Kuliah |

<!-- Alur Utama -->

| Langkah | Tindakan Aktor (Dosen) | Respons Sistem |
|---|---|---|
| 1 | Dosen memilih menu Input Nilai Mata Kuliah. | Sistem menampilkan daftar mata kuliah yang diampu dosen. |
| 2 | Dosen memilih mata kuliah yang akan diinput nilainya. | Sistem memeriksa apakah dosen merupakan pengampu mata kuliah tersebut. |
| 3 | Dosen memasukkan nilai mahasiswa. | Sistem memvalidasi data nilai yang dimasukkan. |
| 4 | Dosen menyimpan nilai. | Sistem menyimpan nilai yang valid dan menampilkan konfirmasi bahwa penyimpanan berhasil. |

<!-- Alur Alternatif dan Pengecualian -->

- **A1 — Dosen bukan pengampu mata kuliah:** Sistem menolak akses input nilai dan tidak menyimpan perubahan.
- **A2 — Nilai di luar rentang yang sah:** Sistem menolak nilai tersebut, menampilkan pesan kesalahan, dan meminta dosen memasukkan nilai yang valid.
- **A3 — Data nilai tidak lengkap atau tidak valid:** Sistem menampilkan pesan validasi dan meminta dosen memperbaiki data sebelum menyimpan kembali.

Jika proses gagal, nilai yang tidak valid tidak disimpan dan data nilai sebelumnya tetap tidak berubah.
