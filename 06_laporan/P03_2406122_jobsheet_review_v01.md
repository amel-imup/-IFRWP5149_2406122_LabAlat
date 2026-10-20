# Pengujian Konsistensi Diagram dan Deskripsi Use Case SIA

| **No** | **Situasi Pengujian** | **Hasil yang Diharapkan** | **Konsisten?** |
| ------ | -------------------- | ------------------------- | -------------- |
| 1 | Validasi berhasil, tanpa unduh bukti | SIA-UC04 berhasil memvalidasi KRS, SIA-UC03 menyimpan pengajuan KRS dengan status menunggu persetujuan, dan SIA-UC05 tidak dijalankan. | Ya |
| 2 | Validasi gagal | Sistem menampilkan informasi kegagalan, pengajuan KRS tidak dinyatakan berhasil, dan bukti pengajuan tidak diunduh. | Ya |
| 3 | Validasi berhasil, memilih unduh bukti | KRS berhasil divalidasi dan disimpan terlebih dahulu, kemudian SIA-UC05 dijalankan untuk menyediakan bukti pengajuan yang dapat diunduh mahasiswa. | Ya |


