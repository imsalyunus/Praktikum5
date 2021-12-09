# Praktikum5
Tugas Pertemuan ke 10
 Disini saya menggunakan
 import os ,sys
 
 pertama” kita akan membuat Perulangan dahulu dengan menggunakan fungsi while true
 
 
 variabel c adalah fungsi input untuk pilihan menu
 
 if c.lower() , fungsinya ialah apabila user menginputkan dengan huruf besar ,maka otomatis akan menjadi huruf kecil sehingga kodisi yang di inginkan tercapai
baik seperti pada gambar di atas per-tama² kita buat dulu fungsi

if c.lower() == ‘q’ , maka program akan berhenti / keluar

karena sebelumnya kita memakai perulangan while True , maka kita hanya perlu menambahkan fungsi break untuk menghentikan perulangan tersebut .
baik selanjutnya mari kita buat fungsi if c.lower() == ‘l’ :
nah fungsi ini adalah untuk menampilkan list ,data di dalam database yang tersedia
namun jika di dalam database tidak ada data
maka hasil print out dalam tabel juga tidak akan di tampilkan

Nah ,,
karena pada soal di atas menggunakan format table saat menampilkan listnya
maka kita perlu membuat logika untuk format tabelnya

pertama kita buka dulu file database.txt dan tambahkan “a” di belakang fungsi open , fungsinya adalah append atau menambahkan tanpa menghapus baris sebelumnya (jika sudah ada) sebelumnya
logika yang di buat dari line 142 – 147 adalah untuk memasukan nama ,namun user bebas bisa memasukan string atau int . Namun coba anda perhatikan pada line 175 -183 ,tentunya berbeda
pada line ini saya menambahkan int pada fungsi inputnya , dan menggunakan try di dalam while true tujuanya ialah kondisi dari pasanganya try yaitu except , saya menambahkan fungsi ini karena untuk mendeteksi jika format yang di inputkan bukan merupakan type angka maka akan muncul eror ValueError dan akan mencetak “masukan UAS dengan angka” . . . dan fungsi else-nya ialah jika tidak eror dan type yang dimasukan sesuai maka proses while True(perulanngan) akan berhenti dengan menambahkan break di dalam else

nah karena pada menu ada kolom AKHIR yang di dapatkan dengan menggunakan rumus
maka disini saya akan menggunakan fungsi round dan float
round untuk menentukan banyaknya angka di belakang koma ,bagian ini disebut sebagai ndigits
float disini saya gunakan untuk untuk mengubah bilangan menjadi float(desimal) , yang nantinya akan di kembalikan dengan round sehingga nanti hasil dari rumus AKHIR menjadi seperti yang di inginkan misal dalam kasus ini saya membuat angka akhir menjadi 2 angka di belakang koma,

nantinya setelah angka akhir di dapatkan ,maka hasil input tadi akan di tulis kedalam database yang tadi sudah kita buat pada awal menu add td
nah maka file akan kita simpan dengan format string kedalam file database.txt

dan untuk bagian tengahnya kita menggunakan fungsi for untuk memfilter jika di dalam database (kosong,ada baris yang kosong) maka akan di lewati oleh print dan akan langsung mencetak bagian footer 

jika di dalam database tidak terdapat “apa-apa” atau database kosong dan atau jika ada baris yang kosong di dalam database maka akan langsung di lewati , program akan langsung mencetak bagian footer ..
Nah jika di dalam database terdapat data nya , maka program akan memproses dan akan me-replace string [nama : , Nim ,Tugas ,uts ,uas dan akhir] menjadi [ ]/(tidak ada) jadi yang tersisa adalah nilai dari data input saja ..
yg terpisah oleh [ “|” ]
DAN saya akan menggunakan fungsi strip dan split
atau kalian bisa lihat pada gambar di atas pada line 24 ,baik mari kita bahas bagian printnya

(na[:15]).ljust(17,’.’) => maka yang akan di ambil adalah 15 space dari nilai nama dan jika melebihi dari 15 maka baris ke 16 – 17 akan di ubah menjadi ‘ . ‘ (titik) dan akan berhenti pada space ke 17
(ni).ljust(17) => ini seperti diatas , namun lebi baik di buat seperti di atas supaya lebih rapi apabila kemungkinan nilai ni/nim melebihi 17 space, maka tabel akan kacau , alangkah lebih baik di buat sperti ini (ni[:15]).ljust(17)
nah untuk 4 bagian lainya formatnya seperti ini :
(tu).ljust(6) => tabel ini saya buat tidak lebih dari 7 space , karena saya rasa nilai yg di inputkan tidak lebih dari nilai 100

untuk bagian edit itu kurang lebih saja dengan add dan bagian search itu kurang lebih dengan list hanya saja bagian ini cuman mencetak data yang di cari
