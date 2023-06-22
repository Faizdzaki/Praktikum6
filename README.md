# tugas 3
## 1 PENGOLAHAN DATA KARYAWAN
# Tabel Departement

# Di bawah ini merupakan perintah dan juga hasil yang di minta
````
CREATE TABLE Departemen ( IDDepartemen INT PRIMARY KEY, NamaDepartemen VARCHAR(255) );
````
![gambar 1](https://github.com/Faizdzaki/Praktikum6/assets/136536503/5321bc1d-6544-4b9c-975d-78a46d7c18ed)

## Tabel Karyawan
### Selanjutnya adalah table karyawan dengan menggunakan perintah seperti di bawah ini beserta hasil

````
CREATE TABLE Karyawan ( IDKaryawan INT PRIMARY KEY, NamaKaryawan VARCHAR(255), IDSupervisor INT, IDDepartemen INT, FOREIGN KEY (IDSupervisor) REFERENCES Karyawan(IDKaryawan), FOREIGN KEY (IDDepartemen) REFERENCES Departemen(IDDepartemen) );
````
![gambar 2](https://github.com/Faizdzaki/Praktikum6/assets/136536503/0722188f-56b7-4092-9daf-69b842f7a0b2)

## Tabel Proyek
### Kemudian kita akan melanjutkan pada tabel proyek dengan menggunakan perintah sepert di bawah ini beserta hasilnya

````
CREATE TABLE Proyek ( IDProyek INT PRIMARY KEY, NamaProyek VARCHAR(255), TanggalMulai DATE, TanggalSelesai DATE );
````
![gambar 3](https://github.com/Faizdzaki/Praktikum6/assets/136536503/7bdd4fdb-7ce5-4775-84ea-00db0aa43261)

## Tabel Supervisor
### Kemudian kita akan melanjutkan pada tabel supervisor dengan menggunakan perintah sepert di bawah ini beserta hasilnya

````
CREATE TABLE Supervisor ( IDSupervisor INT, IDDepartemen INT, FOREIGN KEY (IDSupervisor) REFERENCES Karyawan(IDKaryawan), FOREIGN KEY (IDDepartemen) REFERENCES Departemen(IDDepartemen) );
````
![gambar 4](https://github.com/Faizdzaki/Praktikum6/assets/136536503/ea622171-1fcb-4cf4-9f91-5c86390447da)

## Table Partisipasi
### Kemudian kita akan melanjutkan pada tabel partisipasi dengan menggunakan perintah sepert di bawah ini beserta hasilnya

````
CREATE TABLE Partisipasi ( IDKaryawan INT, IDProyek INT, FOREIGN KEY (IDKaryawan) REFERENCES Karyawan(IDKaryawan), FOREIGN KEY (IDProyek) REFERENCES Proyek(IDProyek) );
````
![gambar 5](https://github.com/Faizdzaki/Praktikum6/assets/136536503/d785bff6-0d33-4f01-a5ad-1ed74c426ed4)
