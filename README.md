# data mahasiswa
<<<<<<< HEAD
 LATIHAN2
 # 1. Buat sebuah database dengan nama latihan2!
mysql> create database latihan02;
=======
# 2. Buat sebuah tabel dengan nama biodata (nama, alamat) didalam database latihan1!

mysql>create table biodata (nama varchar (15), alamat varchar (15));
![gambar1](https://github.com/dhomuhammad/datamahasiswa/blob/main/screenshot/ss1.png)

# 3. Tambahkan sebuah kolom keterangan (varchar 15), sebagai kolom terakhir!
mysql> alter table biodata add column keterangan varchar (15);
mysql> desc biodata
![gambar1](https://github.com/dhomuhammad/datamahasiswa/blob/main/screenshot/ss2.png)

# 4. Tambahkan kolom id (int 11) di awal (sebagai kolom pertama)!
 mysql> alter table biodata add column id int(11) first;
 ![gambar1](https://github.com/dhomuhammad/datamahasiswa/blob/main/screenshot/ss3.png)

# 5. Sisipkan sebuah kolom dengan nama phone (varchar 15) setelah kolom alamat!
mysql> alter table biodata add column phone varchar(15) after alamat;
mysql> desc biodata;
![gambar1](https://github.com/dhomuhammad/datamahasiswa/blob/main/screenshot/ss4.png)

# 6. Ubah tipe data kolom id menjadi char(11)!
mysql> alter table biodata modify column id char (11);
![gambar1](https://github.com/dhomuhammad/datamahasiswa/blob/main/screenshot/ss5.png)

# 7. Ubah nama kolom phone menjadi hp (varchar 20)!
mysql> alter table biodata change column phone hp varchar(20);
mysql> desc biodata;
![gambar1](https://github.com/dhomuhammad/datamahasiswa/blob/main/screenshot/ss6.png)

# 8. Tambahkan kolom email setelah kolom hp!
mysql> alter table biodata add column email varchar(11) after hp;
mysql> desc biodata;
![gambar1](https://github.com/dhomuhammad/datamahasiswa/blob/main/screenshot/ss7.png)

# 9. Hapus kolom keterangan dari tabel!
mysql> alter table biodata drop column keterangan;
![gambar1](https://github.com/dhomuhammad/datamahasiswa/blob/main/screenshot/ss8.png)

# 10. Ganti nama tabel menjadi data_mahasiswa!
mysql> alter table biodata rename data_mahasiswa;
mysql> desc data_mahasiswa;
![gambar1](https://github.com/dhomuhammad/datamahasiswa/blob/main/screenshot/ss9.png)

# 11. Ganti nama field id menjadi nim!
mysql> alter table data_mahasiswa change id nim;
mysql> desc data_mahasiswa;
![gambar1](https://github.com/dhomuhammad/datamahasiswa/blob/main/screenshot/ss10.png)

# 12. Jadikan nim sebagai PRIMARY KEY!
mysql>  alter table data_mahasiswa add primary key (nim);
mysql> desc data_mahasiswa;
![gambar1](https://github.com/dhomuhammad/datamahasiswa/blob/main/screenshot/ss11.png)

# 13. Jadikan kolom email sebagai UNIQUE KEY
mysql> alter table data_mahasiswa add unique key (email);
mysql> desc data_mahasiswa;
![gambar1](https://github.com/dhomuhammad/datamahasiswa/blob/main/screenshot/ss12.png)

# C.	Data dan Analisis 
## 1.	Apa maksud dari Int (11)?
Maksud dari int (11) adalah nama tipe datanya adalah integer dan memiliki panjang 11 karakter.
## 2.	Ketika kita melihat sturktur tabel dengan perintah desc, ada kolom Null yang berisi Yes dan No, apa maksudnya?
Apabila Null berisi no, maka data tersebut nantinya akan dilakukan pengisian atau penginputan. Sedangkan apabila Null berisi yes, maka artinya data tersebut akan dikosongkan atau tidak dilakukan penginputan.

LATIHAN3
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