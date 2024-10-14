mysql> CREATE TABLE pembelian (
-> id INT AUTO_INCREMENT PRIMARY KEY,
-> tanggal DATE NOT NULL,
-> nomor VARCHAR(20) NOT NULL,
-> produk_id INT NOT NULL,
-> jumlah INT NOT NULL,
-> harga DECIMAL(10,2) NOT NULL,
-> vendor_id INT NOT NULL
-> );

Query OK, 0 rows affected (0.02 sec)

mysql> CREATE TABLE vendor (
-> id INT AUTO_INCREMENT PRIMARY KEY,
-> nomor VARCHAR(20) NOT NULL,
-> nama VARCHAR(50) NOT NULL,
-> kode VARCHAR(10) NOT NULL,
-> alamat VARCHAR(100) NOT NULL,
-> kontak VARCHAR(20) NOT NULL
-> );

Query OK, 0 rows affected (0.01 sec)

mysql> INSERT INTO pembelian (tanggal, nomor, produk_id, jumlah, harga, vendor_id)
-> VALUES
-> ('2023-01-01', 'PO001', 1, 10, 100.00, 1),
-> ('2023-02-15', 'PO002', 2, 5, 150.00, 2),
-> ('2023-03-10', 'PO003', 3, 8, 80.00, 3),
-> ('2023-04-20', 'PO004', 1, 15, 110.00, 2),
-> ('2023-05-05', 'PO005', 4, 12, 90.00, 1);

Query OK, 5 rows affected (0.01 sec)
Records: 5 Duplicates: 0 Warnings: 0

mysql> INSERT INTO vendor (nomor, nama, kode, alamat, kontak)
-> VALUES
-> ('VN001', 'Vendor A', 'VA', 'Jl. Merdeka No. 1', '081234567890'),
-> ('VN002', 'Vendor B', 'VB', 'Jl. Sudirman No. 2', '082345678901'),
-> ('VN003', 'Vendor C', 'VC', 'Jl. Gatot Subroto No. 3', '083456789012'),
-> ('VN004', 'Vendor D', 'VD', 'Jl. Ahmad Yani No. 4', '084567890123'),
-> ('VN005', 'Vendor E', 'VE', 'Jl. Diponegoro No. 5', '085678901234');

Query OK, 5 rows affected (0.01 sec)
Records: 5 Duplicates: 0 Warnings: 0