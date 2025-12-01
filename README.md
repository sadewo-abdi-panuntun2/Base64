# Base64

Pengertian Base64

Base64 adalah metode encoding yang digunakan untuk mengubah data mentah (binary data) menjadi rangkaian karakter ASCII yang aman dikirim melalui media yang hanya mendukung teks. Base64 tidak termasuk teknologi enkripsi; tujuan utamanya bukan melindungi kerahasiaan data, tetapi memastikan data dapat ditransmisikan tanpa rusak.

Dalam prosesnya, Base64 mengambil data dalam kelompok 3 byte (24 bit), lalu membaginya menjadi 4 blok kecil berukuran 6 bit. Setiap blok 6 bit dipetakan ke satu karakter dari tabel Base64. Hasilnya adalah teks yang hanya terdiri dari huruf besar, huruf kecil, angka, serta simbol + dan /. Untuk keperluan kompatibilitas, karakter = sering digunakan sebagai padding di bagian akhir.

Tujuan dan Kegunaan Base64

1. Menjaga kompatibilitas data
Banyak protokol lama seperti email (SMTP) atau sistem web hanya mendukung karakter ASCII. Base64 memastikan file apa pun—gambar, teks, sertifikat, atau byte mentah—dapat dikirim melalui saluran yang hanya menerima teks.


2. Menyembunyikan data dari tampilan langsung (obfuscation ringan)
Walaupun bukan enkripsi, Base64 dapat membuat data terlihat acak sehingga tidak mudah dibaca sekilas oleh manusia.


3. Digunakan dalam berbagai standar internet
Token JWT, header HTTP, metadata MIME, serta berbagai API menggunakan Base64 untuk menyimpan atau mengirim representasi data.

Base64 Bukan Enkripsi

Base64 sering disalahpahami sebagai teknik pengamanan karena hasilnya terlihat acak. Padahal, Base64 dapat dibalik kembali ke bentuk aslinya tanpa memerlukan kunci atau proses khusus. Semua algoritma Base64 bersifat terbuka dan dapat di-decode siapa saja.

Perbedaan singkat:

Encoding: mengubah format data.

Enkripsi: mengunci data agar tidak bisa dibaca tanpa kunci.
Base64 berada pada kategori encoding.

Contoh Penggunaan Base64

Encode teks

echo "Halo Dunia" | base64

Decode teks

echo "SGFsbyBEdW5pYQ==" | base64 -d

Encode file

base64 gambar.png > gambar.txt

Decode file

base64 -d gambar.txt > gambar.png

Kesimpulan

Base64 adalah teknik encoding yang sangat berguna untuk memastikan data dapat dikirim, disimpan, dan diproses dalam lingkungan yang hanya mendukung karakter teks. Walaupun tampilannya menyerupai data terenkripsi, Base64 tidak memberikan keamanan dan tidak boleh digunakan sebagai mekanisme proteksi informasi. Penggunaannya terutama berfokus pada kompatibilitas dan representasi data yang stabil di berbagai sistem.
