# Ringkasan Temuan Utama untuk Hasil dan Pembahasan

## Dasar penghitungan

Seluruh tabel pertumbuhan dan jumlah kota menggunakan dataset cleaning `output/data_clean.csv` tanpa mengulang proses cleaning. Unit jumlah kota adalah `Id Proyek` unik di dalam tiap tahun. Satu ID yang tercatat pada lebih dari satu tahun tetap dihitung pada setiap tahun terkait; jumlah lintas tahun karena itu merupakan proyek-tahun, bukan jumlah proyek unik sepanjang periode. Agregat sektor/kecamatan juga dapat menghitung proyek yang memiliki beberapa KBLI atau lokasi.

## Temuan deskriptif dan pertumbuhan

- Jumlah `Id Proyek` unik kota: 2021: 30.252, 2022: 114.972, 2023: 129.053, 2024: 137.449, 2025: 108.324.
- Sebanyak 24 `Id Proyek` tercatat pada lebih dari satu tahun; angka tahunan menghitungnya sekali di setiap tahun kemunculannya. Ada 520,026 ID unik pada seluruh periode.
- Perubahan jumlah kota dari 2021 ke 2025 adalah 78,072 proyek (258.07%); jumlah proyek unik 2024 adalah 137,449, bukan hasil penjumlahan sektor-kecamatan.
- Pada 2024, agregat jumlah unik per kombinasi kecamatan-KBLI adalah 137,450, satu lebih banyak daripada total kota 137,449. Tabel 15 menunjukkan proyek dapat mengisi lebih dari satu kombinasi KBLI-kecamatan; baris berulang dalam kombinasi yang sama dipisahkan dari pengulangan lintas kategori.
- Kelompok dengan jumlah proyek-tahun tertinggi adalah KBLI 47 (Perdagangan Eceran, Bukan Mobil dan Sepeda Motor); terendah KBLI 39 (Aktivitas Remediasi dan Pengelolaan Sampah Lainnya).
- Kecamatan dengan jumlah proyek-tahun tertinggi adalah Rungkut; yang terendah Bulak.
- Pertumbuhan absolut kecamatan terbesar 2021-2025 ada di Semampir (2,704 proyek; 728.84% dari baseline). Persentase tetap perlu dibaca bersama jumlah awal dan akhir.
- YoY 2021 sengaja kosong sebagai baseline. Perubahan 2021-2025 ditampilkan terpisah sebagai kumulatif; CAGR adalah ukuran tersendiri pada analisis gabungan.

## Konsentrasi LQ

- LQ diklasifikasikan dengan LQ > 1 sebagai basis, LQ < 1 sebagai non-basis, dan LQ = 1 sebagai setara. Seluruh 31 kecamatan dan 83 kode KBLI masuk panel; kombinasi tanpa aktivitas menjadi LQ 0 bila sektor aktif di kota, sedangkan sektor tanpa aktivitas kota pada tahun itu berstatus LQ tidak tersedia.
- Tabel LQ lama hanya memuat kombinasi dengan kegiatan; tabel jurnal melengkapi kombinasi struktural nol. Pada 2024, tepat satu `Id Proyek` tercatat di dua kecamatan pada tahun yang sama (tanpa KBLI ganda), sehingga agregat LQ berbasis lokasi satu lebih besar dari hitungan unik kota. Tabel 15-16 merinci sumber selisih dan perbandingan klasifikasi.
- LQ tertinggi perlu dibaca bersama jumlah kegiatan lokal dan skala sektor kota pada Tabel 13. Konsentrasi relatif yang tinggi tidak menyatakan jumlah absolut yang besar.
- Agregat LQ menjumlahkan kombinasi kecamatan-KBLI. Satu proyek dengan beberapa KBLI dapat masuk ke lebih dari satu kombinasi; totalnya tidak boleh disamakan dengan jumlah proyek unik kota.

## Analisis gabungan dan implikasi

- Klasifikasi memakai rata-rata LQ 31 kecamatan dengan bobot kecamatan yang sama, lalu rata-rata 2021-2025 dengan bobot tahun yang sama, serta CAGR dari jumlah unik sektoral 2021 ke 2025 untuk empat interval. Analisis ini menggunakan LQ dan CAGR, bukan DLQ.
- Ringkasan kategori:
- Sektor Basis dan Tumbuh: 33 kelompok
- Sektor Basis tetapi Tidak Tumbuh: 2 kelompok
- Sektor Non-Basis tetapi Tumbuh: 43 kelompok
- Sektor Non-Basis dan Tidak Tumbuh: 2 kelompok
- Data Tidak Memadai: 3 kelompok
- Sektor menonjol untuk pendalaman:
- KBLI 11 (Industri Minuman), Sektor Basis dan Tumbuh: CAGR 89.56%, jumlah 2021 190, jumlah 2025 2,453.
- KBLI 51 (Angkutan Udara), Sektor Basis dan Tumbuh: CAGR 59.67%, jumlah 2021 2, jumlah 2025 13.
- KBLI 10 (Industri Makanan), Sektor Basis dan Tumbuh: CAGR 56.35%, jumlah 2021 1,437, jumlah 2025 8,588.
- KBLI 50 (Angkutan Perairan), Sektor Basis dan Tumbuh: CAGR 51.37%, jumlah 2021 48, jumlah 2025 252.
- KBLI 60 (Aktivitas Penyiaran dan Pemrograman serta Distribusi Konten), Sektor Basis dan Tumbuh: CAGR 50.77%, jumlah 2021 6, jumlah 2025 31.
- KBLI 05 (Pertambangan Batu Bara dan Lignit), Sektor Basis tetapi Tidak Tumbuh: CAGR -2.60%, jumlah 2021 10, jumlah 2025 9.
- KBLI 21 (Industri Farmasi, Produk Obat Kimia, dan Obat Tradisional), Sektor Basis tetapi Tidak Tumbuh: CAGR -3.78%, jumlah 2021 70, jumlah 2025 60.
- KBLI 07 (Pertambangan Bijih Logam), Sektor Non-Basis dan Tidak Tumbuh: CAGR -1.84%, jumlah 2021 14, jumlah 2025 13.
- KBLI 06 (Pertambangan Minyak Bumi, Gas Alam, dan Panas Bumi), Sektor Non-Basis dan Tidak Tumbuh: CAGR -33.13%, jumlah 2021 5, jumlah 2025 1.
- KBLI 55 (Penyediaan Akomodasi), Sektor Non-Basis tetapi Tumbuh: CAGR 79.67%, jumlah 2021 216, jumlah 2025 2,251.
- KBLI 90 (Kegiatan Kesenian, Hiburan, dan Rekreasi), Sektor Non-Basis tetapi Tumbuh: CAGR 71.95%, jumlah 2021 31, jumlah 2025 271.
- KBLI 78 (Aktivitas Ketenagakerjaan), Sektor Non-Basis tetapi Tumbuh: CAGR 69.08%, jumlah 2021 179, jumlah 2025 1,463.
- Hasil dapat digunakan sebagai informasi awal untuk menelaah sektor yang terkonsentrasi dan tumbuh serta perbedaan antarwilayah. Analisis ini tidak mengukur nilai investasi, produktivitas, kesempatan kerja, atau penyebab perubahan; penetapan program/perencanaan perlu dipadukan dengan indikator dan validasi lapangan yang relevan.

## Pemeriksaan yang masih memerlukan tinjauan manual

- Pastikan kembali padanan nama resmi setiap KBLI terhadap nomenklatur KBLI 2020 yang dipakai dalam artikel dan cantumkan rujukannya.
- Pemeriksaan visual browser untuk tile, batas 31 kecamatan, filter, legenda, dan data peta telah lulus; tinjau kembali ukuran/penempatan peta pada layout artikel.
- Verifikasi interpretasi substantif dan batasan data bersama penulis/ahli sektor; hasil statistik tidak mengidentifikasi hubungan sebab-akibat.
