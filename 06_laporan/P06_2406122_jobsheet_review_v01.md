# Review Activity Diagram SIA (Checklist Bagian C.4)

| No | Butir checklist | Hasil | Keterangan |
| --- | --- | --- | --- |
| 1 | Tepat satu initial node dan satu activity final node, tidak ada action terputus | Terpenuhi | Initial node di swimlane Dosen, activity final node di swimlane Mahasiswa |
| 2 | Semua alur keluar decision memiliki guard | Terpenuhi | [lengkap] dan [belum lengkap], saling lepas dan menutup semua kemungkinan |
| 3 | Cabang decision kembali melalui merge | Terpenuhi | Cabang [belum lengkap] melalui Melengkapi nilai mata kuliah yang belum lengkap lalu bergabung di merge sebelum pengesahan |
| 4 | Fork berpasangan dengan join | Terpenuhi | Satu fork dan satu join setelah Menyiapkan publikasi hasil studi; proses paralel disatukan oleh join, bukan merge |
| 5 | Action berada pada swimlane aktor yang tepat | Terpenuhi | Dosen, Sistem, Admin Akademik, Mahasiswa |
| 6 | Action tertelusur ke langkah tabel skenario | Terpenuhi | Lihat `P06_2406122_SIA_skenario_v01.md` |
| 7 | Collaboration tidak digambar | Terpenuhi | Tidak ada collaboration sebagai action atau swimlane |
| 8 | Berkas sumber dan ekspor sama versi | Terpenuhi | `.drawio` dan `.png` sama-sama v01 |
