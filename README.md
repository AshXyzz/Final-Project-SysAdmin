## Menginstall System Operasi CentOS 7
kita bisa mengunduh nya disini

```
https://www.centos.org/download/
```


## Install SSH

Jalankan Perintah untuk menginstall OpenSSH
```
sudo yum -y install openssh-server
```
Setelah instalasi selesai, mulai layanan OpenSSH
```
sudo systemctl start sshd
```
Aktifkan layanan OpenSSH agar dimulai otomatis setiap kali sistem dihidupkan
```
sudo systemctl enable sshd
```
Periksa status layanan OpenSSH untuk memastikan semuanya berjalan dengan baik
sudo systemctl status sshd
```
sudo systemctl status sshd
```
<img src="\assets\status ssh.png" alt="status ssh">
