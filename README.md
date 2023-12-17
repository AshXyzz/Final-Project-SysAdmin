## Menginstall System Operasi CentOS 7
kita bisa mengunduh nya disini
[Download CentOS](https://www.centos.org/download/)


## Konfigurasi SSH

### Instal OpenSSH
Jalankan Perintah untuk menginstall OpenSSH
```
sudo yum -y install openssh-server
```
### Mulai Layanan OpenSSH
Setelah instalasi selesai, mulai layanan OpenSSH
```
sudo systemctl start sshd
```
### Aktifkan OpenSSH untuk Dimulai Secara Otomatis
Aktifkan layanan OpenSSH agar dimulai otomatis setiap kali sistem dihidupkan
```
sudo systemctl enable sshd
```
### Periksa Status OpenSSH
Periksa status layanan OpenSSH untuk memastikan semuanya berjalan dengan baik
sudo systemctl status sshd
```
sudo systemctl status sshd
```
<img src="\assets\status ssh.png" alt="status ssh">

### Konfigurasi Firewall 
Jika Anda menjalankan firewall, pastikan untuk mengizinkan koneksi ke port SSH (defaultnya adalah port 22)
```
sudo firewall-cmd --permanent --add-service=ssh
sudo firewall-cmd --reload
```

## Konfigurasi Apache Http
### Install Apache
```
sudo yum install httpd
```
### Mulai Layanan Apache
Setelah instalasi selesai, mulai layanan Apache dan atur agar dimulai otomatis setiap kali sistem dihidupkan
```
sudo systemctl start httpd
sudo systemctl enable httpd
```
### 
### Konfigurasi Firewall untuk HTTP
Jika Anda menggunakan firewall, tambahkan aturan untuk memperbolehkan koneksi HTTP
```
sudo firewall-cmd --permanent --add-service=http
sudo firewall-cmd --reload
```
### Verifikasi Status Apache
Periksa status Apache untuk memastikan bahwa layanan berjalan tanpa masalah
```
sudo systemctl status httpd
```
<img src="\assets\status httpd.png" alt="status httpd">

### Tes Instalasi
Buka web browser dan akses alamat IP server atau domain (jika sudah dikonfigurasi) untuk memastikan bahwa halaman selamat datang Apache ditampilkan
### Tambahkan Halaman HTML
Tambahkan halaman HTML ke direktori root situs web. Misalnya
```
sudo mkdir /var/www/namasitus
sudo nano /var/www/namasitus/index.html
```
Tambahkan konten HTML ke file index.html
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Contoh</title>
</head>
<body>
    <h1>Welcome to MySite</h1>
    <p>This is the default page for your website.</p>
</body>
</html>
```
Simpan dan keluar
### Restart Apache
```
sudo systemctl restart httpd
```
