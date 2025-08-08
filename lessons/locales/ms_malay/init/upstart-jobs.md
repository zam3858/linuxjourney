# Kerja Upstart

## Kandungan Pelajaran

Upstart boleh mencetuskan banyak peristiwa dan kerja untuk dijalankan, malangnya tiada cara mudah untuk melihat dari mana peristiwa atau kerja berasal, jadi anda perlu meneliti konfigurasi kerja dalam /etc/init. Kebanyakan masa, anda tidak akan perlu melihat fail konfigurasi kerja Upstart, tetapi anda akan mahu mengawal beberapa kerja tertentu dengan lebih mudah. Terdapat banyak arahan berguna yang boleh anda gunakan dalam sistem Upstart.

<b>Lihat kerja</b>

<pre>initctl list

shutdown stop/waiting
console stop/waiting
...
</pre>

Anda akan melihat senarai kerja Upstart dengan status yang berbeza dikenakan padanya. Dalam setiap baris, nama kerja ialah nilai pertama dan medan kedua (sebelum /) sebenarnya ialah matlamat kerja, nilai ketiga (selepas /) ialah status semasa. Jadi kita lihat bahawa kerja penutupan kita akhirnya mahu berhenti, tetapi ia sedang dalam keadaan menunggu. Status dan matlamat kerja akan berubah apabila anda memulakan atau menghentikan kerja.

<b>Lihat kerja tertentu</b>

<pre>initctl status networking
networking start/running
</pre>

Kita tidak akan membincangkan butiran cara menulis konfigurasi kerja Upstart, walau bagaimanapun kita sudah tahu bahawa kerja dihentikan, dimulakan dan dimulakan semula dalam konfigurasi ini. Kerja-kerja ini juga mengeluarkan peristiwa, jadi ia boleh memulakan kerja lain. Kami akan melalui arahan manual operasi Upstart, tetapi jika anda ingin tahu, anda harus mendalami fail .conf dengan lebih mendalam.

<b>Mulakan kerja secara manual</b>

<pre>$ sudo initctl start networking</pre>

<b>Hentikan kerja secara manual</b>

<pre>$ sudo initctl stop networking</pre>

<b>Mulakan semula kerja secara manual</b>

<pre>$ sudo initctl restart networking</pre>

<b>Keluarkan peristiwa secara manual</b>

<pre>$ sudo initctl emit some_event</pre>

## Latihan

Perhatikan senarai kerja Upstart anda, sekarang ubah keadaan kerja dengan salah satu arahan yang kita pelajari hari ini. Apa yang anda perhatikan selepas itu?

## Soalan Kuiz

Bagaimanakah saya akan memulakan semula kerja Upstart yang dipanggil kacang secara manual?

## Jawapan Kuiz

sudo initctl restart peanuts
