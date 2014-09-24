## Nginx Auto Installer 

### Requirements

* Sebuah VPS / Dedicated server dengan setidaknya 512MB RAM 
* Instalasi baru dari CentOS 6,0-6,5 (CentOS 7.0 pun sudah support) 
* Dosis Centmin Mod 
* Pengetahuan dasar perintah SSH 
* Pengetahuan dasar untuk menggunakan Putty (Windows) atau Terminal (Linux / Mac)
* Secangkir kopi.

### How to

**Matikan apache (httpd) web servernya terlebih dahulu**
``` sh
service httpd stop
```
**Hapus package dari apache (httpd)**
``` sh
yum remove httpd -y
```
**Masuk ke direktori src**
``` sh
cd /usr/local/src
```
**Lakukan curl installernya**

*Server GitHub*
``` sh
curl -sL https://raw.githubusercontent.com/NginxID/yum-installer/master/installer.sh | bash
```
*Server Centminmod*
``` sh
curl -sL http://centminmod.com/installer.sh | bash
```
### Selesai...

Jika Anda menggunakan reverse proxy atau layanan proxy seperti Cloudflare, Incapsula, Google PageSpeed, Varnish Cache di depan server web Nginx. Anda harus benar untuk menginstal Nginx via HttpRealIpModule. Anda dapat menemukan panduan link pada halaman [Nginx Konfigurasi](http://centminmod.com/nginx_configure.html) atau langsung [di sini](http://centminmod.com/nginx_configure_cloudflare.html).

Tak lupa juga untuk membaca README versi resmi dari centminmod [disini](https://github.com/NginxID/yum-installer/blob/master/readme-en.md#readme)

Selengkapnya anda bisa mengkonfigurasi Nginx anda lewat website centminmod resminya [disini](http://centminmod.com/)