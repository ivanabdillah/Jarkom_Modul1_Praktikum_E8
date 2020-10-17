# Jarkom_Modul1_Praktikum_E8

### 1. Sebutkan webserver yang digunakan pada "testing.mekanis.me"!
Wireshark Filter Expression
``` http.host contains "testing.mekanis.me" ```


### 2. Simpan gambar "Tim_Kunjungan_Kerja_BAKN_DPR_RI_ke_Sukabumi141436.jpg"!
Wireshark Filter Expression

### 3. Cari username dan password ketika login di "ppid.dpr.go.id"!
Wireshark Filter Expression
``` http.request.method == POST ```

### 4. Temukan paket dari web-web yang menggunakan basic authentication method!
Wireshark Filter Expression
``` http.authbasic ```

### 5. Ikuti perintah di aku.pengen.pw! Username dan password bisa didapatkan dari file .pcapng!
Wireshark Filter Expression
``` http contains "aku.pengen.pw" ```

### 6. Seseorang menyimpan file zip melalui FTP dengan nama "Answer.zip". Simpan dan Buka file "Open This.pdf" di Answer.zip. Untuk mendapatkan password zipnya, temukan dalam file zipkey.txt (passwordnya adalah isi dari file txt tersebut).
Wireshark Filter Expression
``` ftp-data ```

### 7. Ada 500 file zip yang disimpan ke FTP Server dengan nama 1.zip, 2.zip, ..., 500.zip. Salah satunya berisi pdf yang berisi puisi. Simpan dan Buka file pdf tersebut. Your Super Mega Ultra Rare Hint = nama pdf-nya "Yes.pdf"
Wireshark Filter Expression

### 8. Cari objek apa saja yang didownload (RETR) dari koneksi FTP dengan Microsoft FTP Service!
Wireshark Filter Expression

### 9. Cari username dan password ketika login FTP pada localhost!
Wireshark Filter Expression
``` ftp.request.command == RETR ```

### 10. Cari file .pdf di wireshark lalu download dan buka file tersebut! clue: "25 50 44 46"
Wireshark Filter Expression

### 11. Filter sehingga wireshark hanya mengambil paket yang mengandung port 21!
Wireshark Filter Expression
``` port 21 ```

### 12. Filter sehingga wireshark hanya mengambil paket yang berasal dari port 80!
Wireshark Filter Expression
``` src port 80 ```

### 13. Filter sehingga wireshark hanya menampilkan paket yang menuju port 443!
Wireshark Filter Expression
``` dst port 443 ```

### 14. Filter sehingga wireshark hanya mengambil paket yang berasal dari ip kalian!
Wireshark Filter Expression
``` src host 192.168.42.119 ```

### 15. Filter sehingga wireshark hanya mengambil paket yang tujuannya ke monta.if.its.ac.id!
Wireshark Filter Expression
``` dst host monta.if.its.ac.id ```

