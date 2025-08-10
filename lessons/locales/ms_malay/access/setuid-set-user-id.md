# Setuid

## Kandungan Pelajaran

Terdapat banyak kes di mana pengguna biasa memerlukan akses yang lebih tinggi untuk melakukan sesuatu. Pentadbir sistem tidak boleh sentiasa ada untuk memasukkan kata laluan root setiap kali pengguna memerlukan akses kepada fail yang dilindungi, jadi terdapat bit kebenaran fail khas untuk membolehkan tingkah laku ini. Set User ID (SUID) membolehkan pengguna menjalankan program sebagai pemilik fail program dan bukannya sebagai diri mereka sendiri.

Mari lihat satu contoh:

Katakan saya ingin menukar kata laluan saya, mudah bukan? Saya hanya menggunakan perintah passwd:

<pre>$ passwd</pre>

Apa yang dilakukan oleh perintah kata laluan? Ia mengubah beberapa fail, tetapi yang paling penting ia mengubah fail /etc/shadow. Mari lihat fail itu sebentar:

<pre>$ ls -l /etc/shadow

-rw-r----- 1 root shadow 1134 Dec 1 11:45 /etc/shadow
</pre>

Oh tunggu sebentar, fail ini dimiliki oleh root? Bagaimana mungkin kita dapat mengubah fail yang dimiliki oleh root?

Mari lihat set kebenaran lain, kali ini perintah yang kita jalankan:

<pre>$ ls -l /usr/bin/passwd

-rwsr-xr-x 1 root root 47032 Dec 1 11:45 /usr/bin/passwd
</pre>

Anda akan perhatikan bit kebenaran baru di sini <b>s</b>. Bit kebenaran ini adalah SUID, apabila fail mempunyai set kebenaran ini, ia membolehkan pengguna yang melancarkan program untuk mendapatkan kebenaran pemilik fail serta kebenaran pelaksanaan, dalam kes ini root. Jadi pada dasarnya semasa pengguna menjalankan perintah kata laluan, mereka berjalan sebagai root.

Itulah sebabnya kita dapat mengakses fail yang dilindungi seperti /etc/shadow apabila kita menjalankan perintah passwd. Sekarang jika anda menghapuskan bit itu, anda akan melihat bahawa anda tidak akan dapat mengubah /etc/shadow dan oleh itu menukar kata laluan anda.

<b>Mengubah SUID</b>

Sama seperti kebenaran biasa terdapat dua cara untuk mengubah kebenaran SUID.

<i>Cara simbolik:</i>
<pre>$ sudo chmod u+s myfile</pre>

<i>Cara angka:</i>
<pre> sudo chmod 4755 myfile</pre>

Seperti yang anda lihat SUID ditandakan dengan 4 dan ditambahkan ke set kebenaran. Anda mungkin melihat SUID ditandakan sebagai huruf besar <b>S</b> ini bermakna ia masih melakukan perkara yang sama, tetapi ia tidak mempunyai kebenaran pelaksanaan.

## Latihan

Lihat kebenaran untuk /etc/passwd secara terperinci, adakah anda perhatikan sesuatu yang lain? Fail dengan SUID diaktifkan juga mudah dibezakan.

## Soalan Kuiz

Nombor apakah yang mewakili SUID?

## Jawapan Kuiz

4
