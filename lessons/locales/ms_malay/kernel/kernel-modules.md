# Modul Kernel

## Kandungan Pelajaran

Katakan saya mempunyai kereta yang hebat, saya melabur banyak masa dan wang ke dalamnya. Saya menambah spoiler, penyangkut, rak basikal dan lain-lain perkara rawak. Komponen ini sebenarnya tidak mengubah fungsi teras kereta dan saya boleh menanggalkan dan menambahnya dengan sangat mudah. Kernel menggunakan konsep yang sama dengan modul kernel.

Kernel itu sendiri adalah perisian monolitik, apabila kita ingin menambah sokongan untuk jenis papan kekunci baharu, kita tidak menulis kod ini terus ke dalam kod kernel. Sama seperti kita tidak akan mencantumkan rak basikal pada kereta kita (mungkin sesetengah orang akan melakukannya). Modul kernel ialah kepingan kod yang boleh dimuatkan dan dinyahmuat ke dalam kernel atas permintaan. Ia membolehkan kita memanjangkan fungsi kernel tanpa benar-benar menambah pada kod kernel teras. Kita juga boleh menambah modul dan tidak perlu but semula sistem (dalam kebanyakan kes).

<b>Lihat senarai modul yang sedang dimuatkan</b>

<pre>$ lsmod</pre>

<b>Muatkan modul</b>

<pre>$ sudo modprobe bluetooth</pre>

Modprobe memuatkan modul dari <b>/lib/modules/(versi kernel)/kernel/drivers</b>. Modul kernel juga mungkin mempunyai kebergantungan, modprobe memuatkan kebergantungan modul kita jika ia belum dimuatkan.

<b>Alih keluar modul</b>

<pre>$ sudo modprobe -r bluetooth</pre>

<b>Muatkan semasa but</b>

Anda juga boleh memuatkan modul semasa but sistem, bukannya memuatkannya buat sementara waktu dengan modprobe (yang akan dinyahmuat apabila anda but semula). Hanya ubah suai direktori <b>/etc/modprobe.d</b> dan tambah fail konfigurasi di dalamnya seperti ini:

<pre>pete@icebox:~$ /etc/modprobe.d/peanutbutter.conf

options peanut_butter type=almond
</pre>

Contoh yang agak pelik, tetapi jika anda mempunyai modul bernama mentega_kacang dan anda ingin menambah parameter kernel untuk jenis=badam, anda boleh memuatkannya semasa permulaan menggunakan fail konfigurasi ini. Juga ambil perhatian bahawa modul kernel mempunyai parameter kernel mereka sendiri jadi anda perlu membaca tentang modul itu secara khusus untuk mengetahui lebih lanjut.

<b>Jangan muat semasa but</b>

Anda juga boleh memastikan modul tidak dimuatkan semasa but dengan menambah fail konfigurasi seperti ini:

<pre>pete@icebox:~$ /etc/modprobe.d/peanutbutter.conf

blacklist peanut_butter
</pre>

## Latihan

Nyahmuat modul bluetooth anda dengan modprobe dan lihat apa yang berlaku. Bagaimanakah anda akan memperbaikinya?

## Soalan Kuiz

Apakah arahan yang digunakan untuk menyahmuat modul?

## Jawapan Kuiz

modprobe -r