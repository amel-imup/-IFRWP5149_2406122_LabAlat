|               Sumber                |  Hubungan   |                 Tujuan                  |
|-------------------------------------|-------------|-----------------------------------------|
|              Mahasiswa              |  Asosiasi   |    SIA-UC01 — Melihat Jadwal Kuliah     |
|              Mahasiswa              |  Asosiasi   |        SIA-UC03 — Mengajukan KRS        |
|              Mahasiswa              |  Asosiasi   |SIA-UC05 — Mengunduh Bukti Pengajuan KRS |
|           Admin_Akademik            |  Asosiasi   |   SIA-UC02 — Mengelola Jadwal Kuliah    |
|                Dosen                |Wali_Asosiasi|   SIA-UC06 — Memproses Keputusan KRS    |
|       SIA-UC03_MengajukanKRS        | <<include>> |       SIA-UC04 — Memvalidasi KRS        |
|SIA-UC05_Mengunduh_Bukti_PengajuanKRS| <<extend>>  |        SIA-UC03 — Mengajukan KRS        |
