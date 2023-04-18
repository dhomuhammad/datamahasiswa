# data mahasiswa
<<<<<<< HEAD
 # 1. Buat sebuah database dengan nama latihan3!
mysql> create database latihan03;
=======
# 2. Tampilkan semua isi/record tabel!!

mysql>create table mahasiswa(nim varchar(10) not null, nama varchar(100) not null, jenis_kelamin varchar(10) not null, tgl_lahir date not null, jalan text (20) not null, kota varchar (50) not null, kode_pos varchar (50) not null, no_hp varchar (50) not null, kd_ds varchar (50) not null);
![gambar1](https://github.com/dhomuhammad/datamahasiswa/blob/main/output-latihan3/ss1.jpg)

# 3. Ubah data tanggal lahir mahasiswa yang bernama Ari menjadi: 1979-08-31!
mysql> select * from where nim=’11223344’;
![gambar1](https://github.com/dhomuhammad/datamahasiswa/blob/main/output-latihan3/ss2.jpg)

# 4. Tampilkan satu baris / record data yang telah diubah tadi yaitu record dengan nama Ari saja!
 mysql> select * from where nim=’11223344’;
 ![gambar1](https://github.com/dhomuhammad/datamahasiswa/blob/main/output-latihan3/ss3.jpg)

# 5. Hapus Mahasiswa yang bernama Dina!
mysql>delete from mahasiswa where nim=’11223346’;
mysql>select * from mahasiswa;
![gambar1](https://github.com/dhomuhammad/datamahasiswa/blob/main/output-latihan3/ss4.jpg)

# 6. Tampilkan record atau data yang tanggal kelahirannya lebih dari atau sama dengan 1996-1-2!
mysql>select * from mahasiswa where tgl_lahir >=’1996-1-2’;
![gambar1](https://github.com/dhomuhammad/datamahasiswa/blob/main/output-latihan3/ss5.jpg)

# 7. Tampilkan semua Mahasiswa yang berasal dari Bekasi dan berjenis kelamin perempuan!
mysql>select * from mahasiswa where kota=’Bekasi’ and jenis_kelamin=’Perempuan’;
![gambar1](https://github.com/dhomuhammad/datamahasiswa/blob/main/output-latihan3/ss6.jpg)

# 8. Tampilkan semua Mahasiswa yang berasal dari Bekasi dengan kelamin laki-laki atau Mahasiswa yang berumur lebih dari 22 tahun dengan kelamin wanita!
mysql>select * from mahasiswa where (kota='Bekasi' and jenis_kelamin='Laki-laki') or (jenis_Kelamin='Perempuan' and tgl_lahir <= date_sub(curdate(),interval 22 year));
![gambar1](https://github.com/dhomuhammad/datamahasiswa/blob/main/output-latihan3/ss7.jpg)

# 9. Tampilkan data nama dan alamat mahasiswa saja dari tabel tersebut
mysql>select nama, jalan, kota from mahasiswa;
![gambar1](https://github.com/dhomuhammad/datamahasiswa/blob/main/output-latihan3/ss8.jpg)

# 10. Tampilkan data mahasiswa terurut berdasarkan nama
mysql>select * from mahasiswa order by nama asc;
![gambar1](https://github.com/dhomuhammad/datamahasiswa/blob/main/output-latihan3/ss9.jpg)







=======
>>>>>>> 026813af7fa049f74b5ee14a7526eaf48edf779c