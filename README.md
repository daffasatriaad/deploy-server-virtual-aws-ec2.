## 💻 Virtual Server Deployment Menggunakan Amazon EC2

Hosting Website Sederhana Menggunakan Amazon EC2 dan NGINX

---

## 📖 Deskripsi Proyek

Proyek ini adalah simulasi sederhana untuk melakukan deployment server virtual menggunakan layanan Amazon EC2 dari AWS. Server ini dikonfigurasi untuk menghosting website sederhana menggunakan NGINX dan dapat diakses secara publik melalui internet.

Proyek ini bertujuan untuk:

- Mempelajari cara membuat dan mengelola instance EC2.
- Mengatur keamanan server menggunakan Security Group.
- Menghubungkan server melalui SSH.
- Menginstall web server NGINX.
- Menghosting website sederhana di cloud.

---

## 🛠 Tools dan Teknologi

- Amazon EC2: Server virtual di cloud.
- Amazon Security Group: Firewall untuk mengatur akses ke server.
- SSH: Menghubungkan server secara remote dan aman.
- NGINX: Web server yang digunakan untuk hosting website.
- AWS Management Console: Untuk melakukan konfigurasi EC2 dan Security Group.

---

## 🌟 Fitur Website

- Hosting website sederhana menggunakan server virtual.
- Akses publik menggunakan alamat IP EC2.
- Website berjalan di atas web server NGINX.
- Akses server aman menggunakan SSH key pair.

---

## 🌐 Link Website

Website dapat diakses melalui link berikut:
👉 http://54.255.223.36

---

🚀 Langkah Pembuatan dan Deployment

1. Buat EC2 Instance

    - Masuk ke AWS Management Console → buka layanan Amazon EC2.
    - Klik Launch Instance.
    - Pilih Amazon Linux 2 → Instance Type: t2.micro (Free Tier).
    - Buat key pair baru untuk koneksi SSH (daffa-key.pem).
    - Atur Security Group:
        Buka port 22 (SSH) untuk remote server.
        Buka port 80 (HTTP) untuk akses website.

2. Hubungkan ke Server via SSH

    - Gunakan terminal dan jalankan perintah:

        chmod 400 webserver-key.pem

        ssh -i "webserver-key.pem" ec2-user@<Public-IP-EC2>

3. Install NGINX Web Server

    - Jalankan perintah berikut di server:

        sudo yum update -y
      
        sudo amazon-linux-extras install nginx1 -y
      
        sudo systemctl start nginx
    
        sudo systemctl enable nginx

4. Upload Website Sederhana

   - Edit file index default NGINX:

       sudo nano /usr/share/nginx/html/index.html

5. Akses Website

   - Buka browser dan ketik:

       http://54.255.223.36

Website sudah bisa diakses secara publik.

---

## 📚 Pelajaran yang Didapat

- Membuat dan mengelola server virtual menggunakan Amazon EC2.\
- Mengatur keamanan server menggunakan Security Group.
- Menghubungkan server menggunakan SSH dengan key pair.\
- Menginstall dan mengkonfigurasi NGINX Web Server.
- Mengupload dan menampilkan website sederhana di EC2.

---

👤 Author

Daffa Satria Adi Dharma

---

## 📌 Catatan

Proyek ini adalah bagian dari portofolio cloud computing saya untuk level pemula.

Jangan lupa untuk mematikan EC2 instance setelah selesai agar tidak terkena biaya.

---
