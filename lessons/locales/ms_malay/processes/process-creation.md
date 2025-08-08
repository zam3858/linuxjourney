# Penciptaan Proses

## Kandungan Pelajaran

Sekali lagi pelajaran ini dan yang seterusnya adalah maklumat semata-mata untuk membolehkan anda melihat apa yang ada di bawah hud, jangan ragu untuk kembali ke sini setelah anda bekerja dengan proses lebih sedikit.

Apabila proses baharu dicipta, proses sedia ada pada asasnya mengklonkan dirinya sendiri menggunakan sesuatu yang dipanggil panggilan sistem fork (panggilan sistem akan dibincangkan jauh pada masa hadapan). Panggilan sistem fork mencipta proses anak yang kebanyakannya serupa, proses anak ini mengambil ID proses baharu (PID) dan proses asal menjadi proses induknya dan mempunyai sesuatu yang dipanggil ID proses induk <b>PPID</b>. Selepas itu, proses anak boleh sama ada terus menggunakan program yang sama yang digunakan oleh induknya sebelum ini atau lebih kerap menggunakan panggilan sistem execve untuk melancarkan program baharu. Panggilan sistem ini memusnahkan pengurusan memori yang diletakkan oleh kernel untuk proses itu dan menyediakan yang baharu untuk program baharu.

Kita boleh melihat ini dalam tindakan:

<pre>$ ps l</pre>

Pilihan l memberi kita "format panjang" atau paparan yang lebih terperinci tentang proses yang sedang berjalan. Anda akan melihat lajur berlabel <b>PPID</b>, ini ialah ID induk. Sekarang lihat terminal anda, anda akan melihat proses yang sedang berjalan iaitu shell anda, jadi pada sistem saya, saya mempunyai proses yang menjalankan bash. Sekarang ingat apabila anda menjalankan arahan ps l, anda menjalankannya dari proses yang menjalankan bash. Sekarang anda akan melihat bahawa <b>PID</b> shell bash ialah <b>PPID</b> arahan <b>ps l</b>.

Jadi jika setiap proses mesti mempunyai induk dan ia hanyalah cabang antara satu sama lain, mesti ada ibu kepada semua proses, bukan? Anda betul, apabila sistem but, kernel mencipta proses yang dipanggil <b>init</b>, ia mempunyai PID 1. Proses init tidak boleh ditamatkan melainkan sistem ditutup. Ia berjalan dengan keistimewaan root dan menjalankan banyak proses yang memastikan sistem berjalan. Kita akan melihat lebih dekat pada init dalam kursus but sistem, buat masa ini ketahuilah ia adalah proses yang melahirkan semua proses lain.

## Latihan

Lihat proses yang sedang berjalan, bolehkah anda melihat proses lain yang mempunyai induk?

## Soalan Kuiz

Apakah panggilan sistem yang mencipta proses baharu?

## Jawapan Kuiz

fork
