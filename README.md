# Aplikasi Kendaraan Dinas Operasional (KDO) - BPD
### Ujian Praktik Junior Programmer - JP-1 - Track: Backend

Aplikasi untuk mengelola data Kendaraan Dinas Operasional (KDO)
milik Perangkat Daerah sebagai bagian dari pengelolaan Barang Milik Daerah (BMD).

## Entitas
1. **KDO** - Kendaraan Dinas Operasional
   - Nomor polisi, merek, tipe/model, tahun produksi, warna, kondisi/status
2. **PNS** - Pegawai Negeri Sipil (penanggung jawab kendaraan)
   - Nama pegawai, NIP, jabatan, golongan
3. **PD** - Perangkat Daerah
   - Contoh: Dinas Pendidikan, Dinas Kesehatan, Dinas PUPR

Relasi: `PD` (1) -> `PNS` (N) -> `KDO` (N)
Satu PD punya banyak PNS, satu PNS bisa bertanggung jawab atas banyak KDO.
Menghapus PD yang masih dipakai PNS/KDO akan ditolak database (foreign key).

## Teknologi
- CodeIgniter 4
- PHP 8.x (XAMPP)
- MySQL / MariaDB
- Postman untuk pengujian REST API

## Cara Jalanin (Manual Setup)
1. Clone repo ini
2. Import database: file `database-bpd.sql` ke phpMyAdmin
3. udpdate /config/database, sesuaikan database
4. Jalankan server:
   ```bash
   D:\xampp\php\php.exe spark serve

## Import Collection Postman
1. upload/import file bpd.postman_collection
