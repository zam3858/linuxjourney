# lsof dan fuser

## Kandungan Pelajaran

Katakan anda memasang pemacu USB dan mula bekerja pada beberapa fail, sebaik sahaja anda selesai, anda pergi dan nyahlekap peranti USB dan anda mendapat ralat "Peranti atau Sumber Sibuk". Bagaimanakah anda akan mengetahui fail mana dalam pemacu USB yang masih digunakan? Sebenarnya terdapat dua alat yang boleh anda gunakan untuk ini:

<b>lsof</b>

Ingat fail bukan sahaja fail teks, imej, dsb, ia adalah segala-galanya pada sistem, cakera, paip, soket rangkaian, peranti, dsb. Untuk melihat apa yang digunakan oleh proses, anda boleh menggunakan arahan lsof (singkatan untuk "senarai fail terbuka") ini akan menunjukkan kepada anda senarai semua fail terbuka dan proses yang berkaitan dengannya.

<pre>
pete@icebox:~$ lsof .
COMMAND    PID  USER   FD   TYPE DEVICE SIZE/OFF NODE NAME
lxsession 1491 pete  cwd    DIR    8,6     4096  131 .
update-no 1796 pete  cwd    DIR    8,6     4096  131 .
nm-applet 1804 pete  cwd    DIR    8,6     4096  131 .
indicator 1809 pete  cwd    DIR    8,6     4096  131 .
xterm     2205 pete  cwd    DIR    8,6     4096  131 .
bash      2207 pete  cwd    DIR    8,6     4096  131 .
lsof      5914 pete  cwd    DIR    8,6     4096  131 .
lsof      5915 pete  cwd    DIR    8,6     4096  131 .
</pre>

Sekarang saya boleh lihat proses mana yang sedang memegang peranti/fail terbuka. Dalam contoh USB kami, anda juga boleh membunuh proses ini supaya kami boleh menyahlekap pemacu yang menjengkelkan ini.

<b>fuser</b>

Cara lain untuk menjejaki proses ialah arahan fuser (singkatan untuk "pengguna fail"), ini akan menunjukkan kepada anda maklumat tentang proses yang menggunakan fail atau pengguna fail.

<pre>
pete@icebox:~$ fuser -v .
                     USER        PID ACCESS COMMAND
/home/pete:         pete  1491 ..c.. lxsession
                     pete  1796 ..c.. update-notifier
                     pete  1804 ..c.. nm-applet
                     pete  1809 ..c.. indicator-power
                     pete  2205 ..c.. xterm
                     pete  2207 ..c.. bash
</pre>

Kita boleh lihat proses mana yang sedang menggunakan direktori /home/pete kami. Alat lsof dan fuser sangat serupa, biasakan diri anda dengan alat ini dan cuba gunakannya pada kali seterusnya anda perlu menjejaki fail atau proses.

## Latihan

Baca halaman manual untuk lsof dan fuser, terdapat banyak maklumat yang tidak kami bincangkan yang membolehkan anda mempunyai fleksibiliti yang lebih besar dengan alat ini.

## Soalan Kuiz

Apakah arahan yang digunakan untuk menyenaraikan fail terbuka dan maklumat prosesnya?

## Jawapan Kuiz

lsof