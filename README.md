## Menginstall System Operasi CentOS 7
kita bisa mengunduh nya disini

```
https://www.centos.org/download/
```
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
