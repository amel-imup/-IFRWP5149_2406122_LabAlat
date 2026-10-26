# Pengujian Konsistensi Diagram dan Deskripsi Use Case SIA

| No | Situasi Pengujian                      | Hasil yang Diharapkan                                                                                                                                                                                             | Konsisten? |
| -- | -------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------- |
| 1  | Validasi berhasil, tanpa unduh bukti   | SIA-UC04 berhasil memvalidasi KRS. SIA-UC03 menyimpan pengajuan KRS dengan status menunggu persetujuan. SIA-UC05 tidak dijalankan karena mahasiswa tidak memilih opsi unduh bukti.                                | Ya         |
| 2  | Validasi gagal                         | Sistem menampilkan informasi kegagalan validasi. Pengajuan KRS tidak dinyatakan berhasil dan bukti pengajuan tidak diunduh. Mahasiswa dapat memperbaiki pengajuan dan mengirimkannya kembali.                     | Ya         |
| 3  | Validasi berhasil, memilih unduh bukti | SIA-UC04 berhasil memvalidasi KRS, kemudian SIA-UC03 menyimpan pengajuan KRS dengan status menunggu persetujuan. Setelah itu, SIA-UC05 dijalankan untuk menyediakan bukti pengajuan yang dapat diunduh mahasiswa. | Ya         |

## Kesimpulan

Berdasarkan ketiga situasi pengujian tersebut, diagram dan deskripsi use case SIA konsisten. Relasi `<<include>>` memastikan validasi KRS menjadi bagian wajib dari proses pengajuan, sedangkan relasi `<<extend>>` menunjukkan bahwa pengunduhan bukti hanya dilakukan apabila mahasiswa memilih opsi tersebut setelah pengajuan berhasil. Jika validasi gagal, pengajuan tidak dinyatakan berhasil dan proses pengunduhan bukti tidak dijalankan.