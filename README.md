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
