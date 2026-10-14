<!-- SKENARIO -->
Mahasiswa mengajukan KRS dengan memilih mata kuliah. Setiap pengajuan menjalankan validasi KRS yang memeriksa kelengkapan, prasyarat mata kuliah, dan benturan jadwal. Jika validasi berhasil, sistem menyimpan pengajuan berstatus menunggu persetujuan dosen wali. Pada konfirmasi penyimpanan, mahasiswa dapat memilih mengunduh bukti pengajuan. Dosen wali menyetujui atau menolak KRS dan memberikan catatan keputusan.

<!-- Tabel Kebutuhan -->
|ID     |                             Kebutuhan tugas                             |
|-------|-------------------------------------------------------------------------|
|SIA-R01|                  Mahasiswa dapat melihat jadwal kuliah                  |
|SIA-R02|              Admin akademik dapat mengelola jadwal kuliah               |
|SIA-R03|                     Mahasiswa dapat mengajukan KRS                      |
|SIA-R04|             Sistem memvalidasi KRS sebagai bagian pengajuan             |
|SIA-R05|Mahasiswa dapat mengunduh bukti jika memilihnya pada konfirmasi pengajuan|
|SIA-R06|        Dosen wali dapat memproses persetujuan atau penolakan KRS        |
|       |                                                                         |

<!-- Batas dan aturan: -->
• Pengguna telah terautentikasi.
• Data mata kuliah, prasyarat, dan jadwal tersedia.
• Validasi gagal menyebabkan pengajuan belum berhasil tersimpan.
• Unduh bukti tidak menjadi syarat keberhasilan pengajuan.
• KRS tersimpan belum berarti disetujui.
• Pembayaran, pengisian nilai, dan implementasi basis data berada di luar tugas

<!-- TENTUKAN AKTOR -->
|    Aktor     |                                  Tujuan                                  |
|--------------|--------------------------------------------------------------------------|
|Admin_Akademik| mengelola jadwal mata kuliah yang digunakan dalam proses pengajuan KRS.  |
|  Mahasiswa   |               Mengajukan KRS dan mengunduh bukti pengajuan               |
|  Dosen_Wali  |Menyetujui atau menolak pengajuan KRS serta memberikan catatan keputusan. |

<!-- Katalog use case -->
Nama ID	 Nama_Fungsi	                Aktor Terkait	Sumber Kebutuhan
SIA-UC01	Melihat Jadwal Kuliah	Mahasiswa	    SIA-R01
SIA-UC02	Mengelola Jadwal Kuliah Admin Akademik	SIA-R02
SIA-UC03	Mengajukan KRS	        Mahasiswa	    SIA-R03
SIA-UC04	Memvalidasi KRS	        Sistem	        SIA-R04
SIA-UC05	Mengunduh Bukti Pengajuan KRS Mahasiswa	SIA-R05
SIA-UC06	Memproses Persetujuan atau Penolakan KRS Dosen Wali	SIA-R06

<!-- Tentukan Relasi include -->
Use Case Utama	Relasi	Use Case yang Disertakan	Alasan
SIA-UC03 — Mengajukan KRS	<<include>>	SIA-UC04 — Memvalidasi KRS	Sistem memvalidasi KRS sebagai bagian dari proses pengajuan.

<!-- Tentukan Relasi extend  -->
Use Case Tambahan	Relasi	Use Case Dasar	Alasan
SIA-UC05 — Mengunduh Bukti Pengajuan KRS	<<extend>>	SIA-UC03 — Mengajukan KRS	Pengunduhan bukti hanya dilakukan jika mahasiswa memilih opsi tersebut pada konfirmasi pengajuan.