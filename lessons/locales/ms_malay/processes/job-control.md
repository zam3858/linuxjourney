# Kawalan Kerja

## Kandungan Pelajaran

Katakan anda sedang bekerja pada satu tetingkap terminal dan anda menjalankan arahan yang mengambil masa yang lama. Anda tidak boleh berinteraksi dengan shell sehingga ia selesai, walau bagaimanapun kami ingin terus bekerja pada mesin kami, jadi kami perlukan shell itu terbuka. Nasib baik kita boleh mengawal bagaimana proses kita berjalan dengan kerja:

<b>Menghantar kerja ke latar belakang</b>

Menambah ampersand (&) pada arahan akan menjalankannya di latar belakang supaya anda masih boleh menggunakan shell anda. Mari kita lihat contoh:

<pre>$ sleep 1000 &
$ sleep 1001 &
$ sleep 1002 &
</pre>

<b>Lihat semua kerja latar belakang</b>

Sekarang anda boleh melihat kerja yang baru anda hantar ke latar belakang.

<pre>$ jobs

[1]    Running     sleep 1000 &
[2]-   Running     sleep 1001 &
[3]+   Running     sleep 1002 &

</pre>

Ini akan menunjukkan kepada anda id kerja dalam lajur pertama, kemudian status dan arahan yang dijalankan. Tanda <b>+</b> di sebelah ID kerja bermakna ia adalah kerja latar belakang terbaharu yang dimulakan. Kerja dengan <b>-</b> ialah arahan kedua terbaharu.

<b>Menghantar kerja ke latar belakang pada kerja sedia ada</b>

Jika anda sudah menjalankan kerja dan ingin menghantarnya ke latar belakang, anda tidak perlu menamatkannya dan memulakan semula. Mula-mula gantung kerja dengan Ctrl-Z, kemudian jalankan arahan <b>bg</b> untuk menghantarnya ke latar belakang.

<pre>
pete@icebox ~ $ sleep 1003
^Z
[4]+    Stopped     sleep 1003

pete@icebox ~ $ bg
[4]+    sleep 1003 &

pete@icebox ~ $ jobs

[1]    Running     sleep 1000 &
[2]    Running     sleep 1001 &
[3]-   Running     sleep 1002 &
[4]+   Running     sleep 1003 &
</pre>

<b>Memindahkan kerja dari latar belakang ke latar depan</b>

Untuk memindahkan kerja keluar dari latar belakang, hanya nyatakan ID kerja yang anda mahu. Jika anda menjalankan fg tanpa sebarang pilihan, ia akan mengembalikan kerja latar belakang terbaharu (kerja dengan tanda + di sebelahnya)

<pre>$ fg %1</pre>

<b>Bunuh kerja latar belakang</b>

Sama seperti memindahkan kerja keluar dari latar belakang, anda boleh menggunakan borang yang sama untuk membunuh proses dengan menggunakan ID Kerja mereka.

<pre>kill %1</pre>

## Latihan

Pindahkan beberapa kerja antara latar belakang dan latar depan

## Soalan Kuiz

Apakah arahan yang digunakan untuk menyenaraikan kerja latar belakang?

## Jawapan Kuiz

jobs
