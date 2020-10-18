# Jarkom_Modul1_Praktikum_E8

### 1. Sebutkan webserver yang digunakan pada "testing.mekanis.me"!
Wireshark Filter Expression
``` http.host contains "testing.mekanis.me" ```
- Gunakan wireshark filter expression di atas
- ![foto 1a](img/1a.png)

- Follow -> HTTP Stream
- ![foto 1b](img/1b.png)


web server yang digunakan : nginx/1.14.0 (Ubuntu)

### 2. Simpan gambar "Tim_Kunjungan_Kerja_BAKN_DPR_RI_ke_Sukabumi141436.jpg"!
Wireshark Filter Expression
- File -> Export Objects -> HTTP
- ![foto 2a](img/2a.png)


- Cari gambar dengan mengetikkan "Tim_Kunjungan_Kerja_BAKN_DPR_RI_ke_Sukabumi141436.jpg"
- ![foto 2b](img/2b.png)


- Save gambar
- ![foto 2c](img/2c.jpg)


### 3. Cari username dan password ketika login di "ppid.dpr.go.id"!
Wireshark Filter Expression
``` http.request.method == POST ```
- Gunakan wireshark filter expression di atas
- ![foto 3a](img/3a.png)

- Follow -> HTTP Stream
- ![foto 3b](img/3b.png)
- ![foto 3c](img/3c.png)

Terlihat bahwa
Username = 10pemuda
Password = guncangdunia

### 4. Temukan paket dari web-web yang menggunakan basic authentication method!
Wireshark Filter Expression
``` http.authbasic ```
- Gunakan wireshark filter expression di atas
- Muncul paket-paket yang menggunakan basic authentication method
- ![foto 4](img/4.png)

### 5. Ikuti perintah di aku.pengen.pw! Username dan password bisa didapatkan dari file .pcapng!
Wireshark Filter Expression
``` http contains "aku.pengen.pw" ```
- Gunakan wireshark filter expression di atas
- ![foto 5a](img/5a.png)

- Follow -> TCP Stream
- ![foto 5b](img/5b.png)

- Cari Authorization
- ![foto 5c](img/5c.png)

- Decode

Mendapat
Username: kakakgamtenk
Password: hartatahtabermuda

- ![foto 5d](img/5d.png)
- ![foto 5e](img/5e.png)

### 6. Seseorang menyimpan file zip melalui FTP dengan nama "Answer.zip". Simpan dan Buka file "Open This.pdf" di Answer.zip. Untuk mendapatkan password zipnya, temukan dalam file zipkey.txt (passwordnya adalah isi dari file txt tersebut).
Wireshark Filter Expression
``` ftp-data ```
Download Answer.zip
- Gunakan wireshark filter expression di atas
- ![foto 6a](img/6a.png)

- Cari yang infonya STOR Answer.zip
- Follow -> TCP Stream
- ![foto 6b](img/6b.png)

- Simpan
- ![foto 6c](img/6c.png)

Cari Password
- ![foto 6d](img/6d.png)
- Gunakan wireshark filter expression di atas
- Cari yang infonya STOR zipkey.txt
- Follow -> TCP Stream
- ![foto 6e](img/6e.png)

- Mendapat password
- ![foto 6f](img/6f.png)
- ![foto 6g](img/6g.png)
- ![foto 6h](img/6h.png)

### 7. Ada 500 file zip yang disimpan ke FTP Server dengan nama 1.zip, 2.zip, ..., 500.zip. Salah satunya berisi pdf yang berisi puisi. Simpan dan Buka file pdf tersebut. Your Super Mega Ultra Rare Hint = nama pdf-nya "Yes.pdf"
Wireshark Filter Expression
``` frame contains “Yes.zip” ```
- Gunakan wireshark filter expression di atas
- ![foto 7a](img/7a.jpg)

- Follow -> TCP Stream
- ![foto 7b](img/7b.jpg)

- Download
- ![foto 7c](img/7c.jpg)

### 8. Cari objek apa saja yang didownload (RETR) dari koneksi FTP dengan Microsoft FTP Service!
Wireshark Filter Expression
``` ftp contains “Microsoft” ```
- Gunakan wireshark  filter expression di atas
- ![foto 8a](img/8a.jpg)

- Dapatkan IP
- Menggunakan IP yang telah ditemukan untuk mencari objek apa saja yang didownload dengan wireshark filter expression di bawah

Wireshark Filter Expression
``` ftp.request.command == RETR && ( ip.src == 198.246.117.106 || ip.dst == 198.246.117.106) ```
- ![foto 8b](img/8b.jpg)

### 9. Cari username dan password ketika login FTP pada localhost!
Wireshark Filter Expression
``` ftp.request.command == RETR ```
- Gunakan wireshark filter expression di atas
- ![foto 9a](img/9a.png)

- Follow -> TCP Stream
- ![foto 9b](img/9b.png)

Mendapat
username : dhana
password : dhana123
- ![foto 9c](img/9c.png)

### 10. Cari file .pdf di wireshark lalu download dan buka file tersebut! clue: "25 50 44 46"
Wireshark Filter Expression
- Search di display filter dengan tombol Ctrl + F
- Cari di hex value 25 50 44 46
- Follow -> TCP Stream
- Save

- ![foto 10a](img/10a.jpg)
- ![foto 10b](img/10b.jpg)
- ![foto 10c](img/10c.jpg)

### 11. Filter sehingga wireshark hanya mengambil paket yang mengandung port 21!
Wireshark Filter Expression
``` port 21 ```
- ![foto 11](img/11.png)

### 12. Filter sehingga wireshark hanya mengambil paket yang berasal dari port 80!
Wireshark Filter Expression
``` src port 80 ```
- ![foto 12](img/12.png)

### 13. Filter sehingga wireshark hanya menampilkan paket yang menuju port 443!
Wireshark Filter Expression
``` dst port 443 ```
- ![foto 13a](img/13a.png)
- ![foto 13b](img/13b.png)

### 14. Filter sehingga wireshark hanya mengambil paket yang berasal dari ip kalian!
Wireshark Filter Expression
``` src host 192.168.42.119 ```
- ![foto 14a](img/14a.png)
- ![foto 14b](img/14b.png)

### 15. Filter sehingga wireshark hanya mengambil paket yang tujuannya ke monta.if.its.ac.id!
Wireshark Filter Expression
``` dst host monta.if.its.ac.id ```
- ![foto 15](img/15.png)
