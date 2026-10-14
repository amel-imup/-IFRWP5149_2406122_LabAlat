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

c. 