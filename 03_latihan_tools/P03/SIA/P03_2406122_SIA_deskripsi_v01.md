a. Ajukan KRS
|       Elemen        |                                  Deskripsi                                   |
|---------------------|------------------------------------------------------------------------------|
|       Elemen        |                            SIA-UC03 — Ajukan KRS                             |
|       Tujuan        |             Menghasilkan pengajuan KRS mahasiswa yang tersimpan.             |
|     Aktor_utama     |                                  Mahasiswa                                   |
|  Sumber_kebutuhan   |                             SIA-R03 dan SIA-R04                              |
|  Pemicu_Mahasiswa   |                        memilih fungsi pengajuan KRS.                         |
|      Prasyarat      |       Mahasiswa dapat mengakses sistem dan data mata kuliah tersedia.        |
|Pascakondisi_berhasil|               Pengajuan KRS tersimpan dengan status pengajuan.               |
| Pascakondisi_gagal  |          Pengajuan tidak berhasil disimpan apabila validasi gagal.           |
|  Include_SIA-UC04   |                                — Validasi KRS                                |
|   Extension_point   |Bukti pengajuan tersedia setelah pengajuan berhasil, pada langkah konfirmasi. |
|   Extend_SIA-UC05   |          — Unduh Bukti Pengajuan KRS, jika mahasiswa memilih unduh.          |
Alur utama:
1. Mahasiswa memilih fungsi pengajuan KRS.
2. Sistem menampilkan fungsi pengajuan KRS.
3. Mahasiswa memilih mata kuliah yang akan diambil.
4. Mahasiswa mengirim pengajuan KRS.
5. Sistem menjalankan validasi KRS.
6. Jika validasi berhasil, sistem menyimpan pengajuan.
7. Sistem menampilkan konfirmasi bahwa pengajuan berhasil.
8. Mahasiswa memilih apakah akan mengunduh bukti pengajuan.
Alur alternatif — Validasi gagal:
1. Pada langkah 5, sistem menemukan bahwa pengajuan tidak memenuhi ketentuan validasi.
2. Sistem menampilkan informasi bahwa validasi gagal.
3. Pengajuan tidak dinyatakan berhasil.
4. Mahasiswa memperbaiki pengajuan dan mengirimkannya kembali.
Alur tambahan — Unduh bukti:
1. Pada langkah 8, mahasiswa memilih opsi unduh bukti.
2. Sistem menyiapkan bukti pengajuan.
3. Sistem menyediakan bukti untuk diunduh mahasiswa.
4. Jika mahasiswa tidak memilih opsi unduh, proses pengajuan selesai tanpa pengunduhan bukti.

b. Validasi KRS
|       Elemen        |                                  Deskripsi                                  |
|---------------------|-----------------------------------------------------------------------------|
|       Elemen        |                           SIA-UC04 — Validasi KRS                           |
|       Tujuan        |          Memeriksa apakah pengajuan KRS memenuhi ketentuan sistem.          |
|        Aktor        |                                utama Sistem                                 |
|       Sumber        |                              kebutuhan SIA-R04                              |
|       Pemicu        |                      Mahasiswa mengirim pengajuan KRS.                      |
|      Prasyarat      |              Data pengajuan KRS telah dikirim oleh mahasiswa.               |
|Pascakondisi_berhasil|   Pengajuan dinyatakan valid dan dapat dilanjutkan ke proses penyimpanan.   |
| Pascakondisi_gagal  |Pengajuan dinyatakan tidak valid dan sistem menampilkan informasi kegagalan. |
|       Include       |                                 Tidak ada.                                  |
|      Extension      |               point Hasil validasi pada proses pengajuan KRS.               |
|       Extend        |                                 Tidak ada.                                  |
Alur utama:
1. Sistem menerima data pengajuan KRS.
2. Sistem memeriksa pengajuan berdasarkan ketentuan yang berlaku.
3. Sistem menentukan hasil validasi.
4. Jika pengajuan memenuhi ketentuan, sistem menyatakan validasi berhasil.
5. Sistem melanjutkan proses pengajuan KRS.
Alur alternatif — Validasi gagal:
1. Pada langkah 3, sistem menemukan bahwa pengajuan tidak memenuhi ketentuan.
2. Sistem menyatakan validasi gagal.
3. Sistem menampilkan informasi kegagalan kepada mahasiswa.
4. Mahasiswa dapat memperbaiki pengajuan untuk dikirimkan kembali.

c. Unduh bukti pengajuan KRS
|       Elemen        |                           Deskripsi                            |
|---------------------|----------------------------------------------------------------|
|       Elemen        |              SIA-UC05 — Unduh Bukti Pengajuan KRS              |
|       Tujuan        | Menyediakan bukti pengajuan KRS yang dapat diunduh mahasiswa.  |
|        Aktor        |                        utama Mahasiswa                         |
|       Sumber        |                       kebutuhan SIA-R05                        |
|       Pemicu        | Mahasiswa memilih opsi unduh bukti pada konfirmasi pengajuan.  |
|      Prasyarat      |      Pengajuan KRS berhasil dan opsi unduh bukti dipilih.      |
|Pascakondisi_berhasil|    Bukti pengajuan tersedia dan berhasil diunduh mahasiswa.    |
|  Pascakondis_gagal  |                 Bukti tidak berhasil diunduh.                  |
|       Include       |                           Tidak ada.                           |
|      Extension      |   point Konfirmasi pengajuan KRS setelah pengajuan berhasil.   |
|       Extend        |SIA-UC03 — Ajukan KRS, jika mahasiswa memilih opsi unduh bukti. |
Alur utama:
1. Mahasiswa menyelesaikan pengajuan KRS.
2. Sistem menampilkan konfirmasi pengajuan berhasil.
3. Mahasiswa memilih opsi unduh bukti.
4. Sistem menyiapkan bukti pengajuan KRS.
5. Sistem menyediakan berkas bukti untuk diunduh.
6. Mahasiswa mengunduh bukti pengajuan.
Alur alternatif — Bukti gagal diunduh:
1. Pada langkah 5, bukti tidak dapat diunduh.
2. Sistem menampilkan informasi bahwa pengunduhan gagal.
3. Mahasiswa dapat mencoba mengunduh kembali jika fitur tersedia.

d. Proses keputusan KRS
|       Elemen        |                                     Deskripsi                                      |
|---------------------|------------------------------------------------------------------------------------|
|       Elemen        |                          SIA-UC06 — Proses Keputusan KRS                           |
|       Tujuan        |      Memproses keputusan persetujuan atau penolakan pengajuan KRS mahasiswa.       |
|        Aktor        |                                  utama Dosen Wali                                  |
|       Sumber        |                                 kebutuhan SIA-R06                                  |
|       Pemicu        |                Dosen wali memilih pengajuan KRS yang akan diproses.                |
|      Prasyarat      |         Pengajuan KRS mahasiswa tersedia untuk diperiksa oleh dosen wali.          |
|Pascakondisi_berhasil|Keputusan tersimpan dan status pengajuan diperbarui menjadi Disetujui atau Ditolak. |
| Pascakondisi_gagal  |          Keputusan belum tersimpan dan status pengajuan belum diperbarui.          |
|       Include       |                                     Tidak ada.                                     |
|      Extension      |                  point Penentuan hasil pemeriksaan pengajuan KRS.                  |
|       Extend        |                                     Tidak ada.                                     |
Alur utama:
1. Dosen wali membuka daftar pengajuan KRS mahasiswa.
2. Sistem menampilkan pengajuan yang tersedia.
3. Dosen wali memilih pengajuan yang akan diperiksa.
4. Dosen wali memeriksa pengajuan KRS.
5. Dosen wali menentukan keputusan persetujuan atau penolakan.
6. Sistem menyimpan keputusan dan memperbarui status pengajuan.
Alur alternatif 1 — Pengajuan disetujui:
1. Pada langkah 5, dosen wali memilih Setujui.
2. Sistem menyimpan keputusan persetujuan.
3. Sistem mengubah status pengajuan menjadi Disetujui.
4. Proses keputusan selesai.
Alur alternatif 2 — Pengajuan ditolak:
1. Pada langkah 5, dosen wali memilih Tolak.
2. Dosen wali mengisi alasan penolakan jika diwajibkan oleh sistem.
3. Sistem menyimpan keputusan penolakan.
4. Sistem mengubah status pengajuan menjadi Ditolak.
5. Proses keputusan selesai.


Pemeriksaan Konsistensi Diagram dan Deskripsi Use Case SIA
a. Validasi berhasil dan mahasiswa tidak mengunduh bukti
- Proses: Mahasiswa mengajukan KRS, sistem memvalidasi pengajuan, dan validasi berhasil.
- Hasil: Sistem menyimpan pengajuan KRS dan menampilkan konfirmasi keberhasilan. Mahasiswa tidak memilih opsi unduh bukti sehingga bukti tidak diunduh.
- Konsistensi: Konsisten. Relasi <<include>> memastikan Validasi KRS menjadi bagian dari Ajukan KRS, sedangkan <<extend>> untuk Unduh Bukti Pengajuan KRS hanya dijalankan jika mahasiswa memilih opsi tersebut.

b. Validasi gagal
- Proses: Mahasiswa mengajukan KRS, kemudian sistem melakukan validasi dan menemukan bahwa pengajuan tidak memenuhi ketentuan.
- Hasil: Sistem menampilkan informasi kegagalan dan pengajuan tidak dinyatakan berhasil. Mahasiswa dapat memperbaiki pengajuan dan mengirimkannya kembali.
- Konsistensi: Konsisten. Diagram menunjukkan validasi sebagai bagian dari pengajuan, dan deskripsi menjelaskan alur alternatif ketika validasi gagal. Pengajuan tidak boleh dianggap berhasil atau dilanjutkan ke pengunduhan bukti sebagai bukti pengajuan yang berhasil.

c. Validasi berhasil dan mahasiswa memilih mengunduh bukti
- Proses: Mahasiswa mengajukan KRS, sistem memvalidasi pengajuan dan menyatakan validasi berhasil, lalu mahasiswa memilih opsi unduh bukti.
- Hasil: Sistem menyimpan pengajuan, menampilkan konfirmasi, kemudian menyediakan bukti pengajuan untuk diunduh mahasiswa.
- Konsistensi: Konsisten. Relasi <<include>> menunjukkan validasi wajib dilakukan, sedangkan relasi <<extend>> menunjukkan pengunduhan bukti sebagai proses opsional yang dijalankan ketika mahasiswa memilihnya.

Kesimpulan
Ketiga situasi tersebut konsisten antara diagram dan deskripsi use case, dengan catatan bahwa diagram menggambarkan hubungan antar-use-case, sedangkan alur utama dan alternatif dalam deskripsi menjelaskan kondisi serta hasil setiap proses.
Agar lebih jelas, pastikan deskripsi Ajukan KRS secara eksplisit menyatakan bahwa pengajuan hanya disimpan sebagai pengajuan berhasil setelah validasi dinyatakan berhasil, dan bahwa pengunduhan bukti hanya dilakukan jika mahasiswa memilih opsi tersebut.