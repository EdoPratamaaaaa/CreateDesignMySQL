# Database Create and Design MySQL
# Case
![image](https://github.com/user-attachments/assets/f6be55d5-af05-464d-9798-e41326bcd3d3)

# sql syntax
- Membuat table user
CREATE TABLE `user`(
    id_user int AUTO_INCREMENT PRIMARY KEY,
    username varchar(50),
    passwod varchar(255)
);

- Membuat table kategori
CREATE TABLE kategori (
    id_kategori int AUTO_INCREMENT PRIMARY KEY,
    nama_kategori varchar(100)
);

- Membuat table produk
CREATE TABLE produk (
    id_produk int AUTO_INCREMENT PRIMARY KEY,
    kategori_id int,
    nama_produk varchar (255),
    harga double,
    foto varchar (255) NOT NULL,
    detail text,
    ketersedian_stok ENUM ('Habis', 'Tersedia'),
    FOREIGN KEY (kategori_id) REFERENCES kategori(id_kategori)
);

![image](https://github.com/user-attachments/assets/550bd147-13f4-414c-8ea8-ce66484708aa)
