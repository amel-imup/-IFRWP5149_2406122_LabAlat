### A. Tujuan Praktikum

Tujuan praktikum pertemuan 6 adalah menyusun activity diagram dari tabel skenario use case pertemuan 5, sehingga langkah Kegiatan dan Respon sistem diubah menjadi alur aktivitas yang dapat diikuti dari awal sampai akhir. Secara khusus, praktikum ini bertujuan agar mahasiswa mampu:

1. Menyusun alur utama dari Skenario Normal dengan satu initial node, action yang berurutan, dan activity final node tanpa alur yang terputus.
2. Mengubah Skenario Alternatif menjadi cabang decision dengan guard yang lengkap, lalu mengakhirinya pada jalur akhir yang jelas atau mengembalikannya ke alur utama.
3. Mengenali kebutuhan fork dan join untuk proses yang berjalan paralel, serta menilai apakah skenario yang dikerjakan memerlukannya.
4. Mengelompokkan setiap action ke dalam swimlane sesuai aktor pada tabel skenario.
5. Menelusuri setiap action ke langkah tabel skenario pertemuan 5 dan memeriksa hasil dengan checklist penilaian.

### B. Dasar Teori

Activity diagram adalah diagram UML yang memodelkan alur kegiatan suatu proses, meliputi urutan action, percabangan keputusan, proses paralel, dan pembagian tanggung jawab antar pelaku. Jika use case diagram menunjukkan fungsi apa saja yang disediakan sistem dan tabel skenario menguraikan fungsi itu menjadi langkah, maka activity diagram menggambarkan langkah-langkah tersebut sebagai alur.

Unsur activity diagram yang dipakai pada praktikum ini:

| Unsur | Fungsi |
|---|---|
| Initial node | Titik awal alur; tepat satu pada setiap diagram |
| Action | Satu langkah kegiatan dari tabel skenario, ditulis dengan kata kerja dan objek |
| Control flow | Panah urutan pelaksanaan antar action |
| Decision | Titik cabang bersyarat; setiap alur keluar wajib memiliki guard dalam kurung siku |
| Merge | Titik penggabungan cabang kembali ke alur utama |
| Fork | Membagi alur menjadi dua proses atau lebih yang berjalan paralel |
| Join | Menyatukan proses paralel dari fork; fork selalu berpasangan dengan join |
| Activity final node | Titik akhir alur |
| Swimlane | Pengelompokan action menurut aktor pelaksananya |

Pemetaan dari tabel skenario ke activity diagram: Skenario Normal menjadi alur utama; Skenario Alternatif menjadi cabang decision dengan guard; langkah include menjadi action wajib pada alur utama; langkah extend menjadi cabang decision tersendiri dengan condition yang sama dengan diagram pertemuan 4; kolom Kegiatan menjadi action pada swimlane aktor; kolom Respon sistem menjadi action pada swimlane Sistem; Skenario Akhir menjadi activity final node. Collaboration tidak digambar pada activity diagram.

### C. Hasil Praktikum

Praktikum dikerjakan dengan draw.io dan hasilnya disimpan pada folder 04_model_analisis/P06, dalam satu berkas `P06_2406122_SIA_activity_diagram.drawio` yang berisi satu halaman untuk setiap activity diagram. Pada studi kasus Sistem Informasi Akademik (SIA) disusun sembilan activity diagram dari sembilan tabel skenario pertemuan 5, yaitu:

| No. | Activity diagram | Sumber skenario | Swimlane | Unsur utama |
|---|---|---|---|---|
| 1 | Lihat Jadwal Kuliah | SIA-UC01 | Mahasiswa, Sistem | Decision Jadwal kuliah tersedia? dengan guard [tersedia] dan [belum tersedia] |
| 2 | Kelola Jadwal Kuliah | SIA-UC02 | Admin Akademik, Sistem | Decision Data lengkap dan tidak terjadi benturan? [ya]/[tidak]; decision Konfirmasi penyimpanan? [simpan]/[batal] |
| 3 | Ajukan KRS | SIA-UC03 | Mahasiswa, Sistem | Action include Menjalankan SIA-UC04 Validasi KRS; decision Hasil validasi memenuhi pemeriksaan? [memenuhi]/[tidak memenuhi]; cabang extend Mahasiswa memilih mengunduh bukti? [ya]/[tidak] menuju SIA-UC05 |
| 4 | Unduh Bukti Pengajuan KRS | SIA-UC05 | Mahasiswa, Sistem | Alur dimulai dari konteks extend; decision Bukti pengajuan KRS dapat disiapkan? [dapat]/[tidak dapat] |
| 5 | Proses Keputusan KRS | SIA-UC06 | Dosen Wali, Sistem | Decision Ada pengajuan KRS yang menunggu? [ada]/[tidak ada]; decision Keputusan dan catatan lengkap? [lengkap]/[tidak lengkap] |
| 6 | Lihat Kalender Akademik | SIA-UC07 | Civitas Akademika, Sistem | Decision Kalender akademik periode tersedia? [tersedia]/[belum tersedia] |
| 7 | Input Nilai Mata Kuliah | SIA-UC08 | Dosen, Sistem | Decision Dosen adalah pengampu? [pengampu]/[bukan pengampu]; Nilai dalam rentang yang sah? [sah]/[di luar rentang]; Data nilai lengkap? [lengkap]/[tidak lengkap] |
| 8 | Lihat KHS | SIA-UC09 | Mahasiswa, Sistem | Decision Data KHS semester ditemukan? dan Nilai semester sudah dipublikasikan?; hanya nilai yang sudah dipublikasikan ditampilkan |
| 9 | Kelola Data Mahasiswa | SIA-UC10 | Admin Akademik, Sistem | Decision Data lengkap dan sah? [lengkap dan sah]/[tidak lengkap/tidak sah] |

Hal-hal penting pada hasil diagram SIA:

1. Activity Ajukan KRS memuat action include Menjalankan SIA-UC04 Validasi KRS sebagai langkah wajib setelah mahasiswa mengirim pengajuan. Jika hasil validasi [tidak memenuhi], sistem menolak penyimpanan dan menampilkan alasan validasi gagal; jika [memenuhi], sistem menyimpan pengajuan dengan status Menunggu persetujuan dosen wali dan menampilkan nomor pengajuan. Setelah konfirmasi, decision Mahasiswa memilih mengunduh bukti? menjadi cabang extend ke Unduh Bukti Pengajuan KRS (SIA-UC05); jika [tidak], alur berakhir karena pengajuan tetap berhasil tersimpan.
2. Activity Kelola Jadwal Kuliah memiliki dua titik keputusan. Pemeriksaan kelengkapan data dan benturan jadwal dilakukan Sistem, sedangkan konfirmasi penyimpanan diputuskan oleh Admin Akademik. Karena itu decision kedua ditempatkan pada swimlane Admin Akademik, dengan cabang [batal] yang kembali menampilkan daftar jadwal kuliah tanpa menyimpan perubahan.
3. Activity Input Nilai Mata Kuliah memuat tiga decision berurutan sesuai tiga cabang alternatif pada skenario: dosen bukan pengampu, nilai di luar rentang yang sah, dan data nilai tidak lengkap. Nilai hanya disimpan jika ketiga pemeriksaan terpenuhi, dan nilai yang tersimpan belum terpublikasi.
4. Activity Lihat KHS memuat dua decision berurutan, yaitu data KHS ditemukan atau tidak, lalu nilai sudah dipublikasikan atau belum, sesuai dua cabang alternatif pada skenario SIA-UC09.
5. Activity Lihat Jadwal Kuliah, Lihat Kalender Akademik, Unduh Bukti Pengajuan KRS, Proses Keputusan KRS, dan Kelola Data Mahasiswa disusun dari alur utama, kemudian ditambah cabang alternatif beserta guard sesuai tabel skenario masing-masing, tanpa menambahkan fitur di luar skenario.

### D. Analisis

1. Keterlacakan ke skenario. Setiap action pada diagram memakai kata kerja dan objek yang sama dengan bunyi langkah pada tabel skenario pertemuan 5, sehingga sumber langkahnya mudah ditunjuk. Action yang berasal dari use case lain diberi rujukan ID, misalnya SIA-UC04 pada Activity Ajukan KRS dan SIA-UC05 sebagai cabang extend.
2. Include dan extend. Include digambar sebagai action wajib pada alur utama (Menjalankan SIA-UC04 Validasi KRS pada Ajukan KRS). Extend digambar sebagai cabang bersyarat setelah konfirmasi penyimpanan, yaitu decision Mahasiswa memilih mengunduh bukti? dengan guard [ya] dan [tidak], sesuai extension point pada tabel skenario SIA-UC03. Activity Unduh Bukti Pengajuan KRS dimulai dari konteks extend tersebut.
3. Use case yang tidak dibuatkan activity sendiri. SIA-UC04 Validasi KRS tidak memiliki tabel skenario pada berkas pertemuan 5 sehingga hanya muncul sebagai action include pada Activity Ajukan KRS. SIA-UC11, UC12, dan UC13 (tambah, ubah, hapus data mahasiswa) juga tidak dibuatkan activity sendiri karena langkah pembedanya tidak ada pada berkas skenario yang dikerjakan; ketiganya tercakup oleh langkah memilih fungsi tambah, ubah, atau hapus pada Activity Kelola Data Mahasiswa.
4. Pembagian swimlane. Action aktor ditempatkan pada swimlane aktor yang melakukannya (kiri), dan respon sistem pada swimlane Sistem (kanan). Setiap diagram hanya memuat satu aktor karena setiap tabel skenario hanya melibatkan satu aktor. Pada Activity Lihat Kalender Akademik aktornya adalah Civitas Akademika, yang mencakup Mahasiswa dan Dosen melalui generalization aktor.
5. Fork dan join. Tidak ada diagram SIA yang memakai fork dan join karena tidak ada langkah pada kesembilan skenario yang berjalan paralel; seluruh langkah berjalan berurutan. Pasangan fork dan join baru diperlukan jika suatu skenario memuat dua proses independen yang harus selesai bersama sebelum alur dilanjutkan.
6. Decision, guard, dan merge. Setiap alur keluar decision diberi guard dalam kurung siku yang saling lepas dan menutup semua kemungkinan, misalnya [tersedia] dan [belum tersedia]. Cabang alternatif pada skenario SIA berakhir pada kondisi akhir sendiri, yaitu pesan penolakan atau pemberitahuan, sehingga setiap cabang bermuara ke activity final node dan tidak ada alur yang menggantung. Karena itu diagram SIA tidak memerlukan merge.
7. Kendala dan perbaikan. Nama halaman pada berkas skenario tidak selalu sama dengan ID use case di dalam tabelnya, misalnya halaman bernama SIA-UC03 berisi SIA-UC07. Penomoran diagram mengikuti ID pada tabel skenario, dan halaman diurutkan dari SIA-UC01 sampai SIA-UC10. Kesalahan lain yang perlu dihindari adalah guard yang belum lengkap, cabang yang menggantung, dan action yang salah swimlane, sehingga seluruh diagram diperiksa dengan checklist penilaian sebelum diekspor ke PNG.

### E. Kesimpulan

Berdasarkan praktikum pertemuan 6, dapat disimpulkan bahwa activity diagram menggambarkan langkah-langkah pada tabel skenario sebagai alur yang utuh dari initial node sampai activity final node. Skenario Normal menjadi alur utama, Skenario Alternatif menjadi cabang decision dengan guard, dan pembagian aktor pada tabel skenario menjadi swimlane, sehingga tanggung jawab setiap action terbaca dari partisinya.

Pada Activity Ajukan KRS, hubungan include digambar sebagai action wajib dan hubungan extend digambar sebagai cabang bersyarat, sehingga konsisten dengan diagram use case pertemuan 4. Dengan menelusuri setiap action ke tabel skenario dan memeriksa hasilnya dengan checklist, kesembilan activity diagram SIA yang dibuat menjadi konsisten dengan skenario pertemuan 5.
