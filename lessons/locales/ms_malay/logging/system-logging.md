# Pengelogan Sistem

## Kandungan Pelajaran

Perkhidmatan, kernel, daemon, dsb pada sistem anda sentiasa melakukan sesuatu, data ini sebenarnya dihantar untuk disimpan pada sistem anda dalam bentuk log. Ini membolehkan kita mempunyai jurnal peristiwa yang boleh dibaca manusia yang berlaku pada sistem kita. Data ini biasanya disimpan dalam direktori /var, direktori /var ialah tempat kita menyimpan data pembolehubah kita, seperti log!

Bagaimanakah mesej ini diterima pada sistem anda? Terdapat perkhidmatan yang dipanggil syslog yang menghantar maklumat ini kepada pencatat sistem.

Syslog sebenarnya mengandungi banyak komponen, salah satu yang penting ialah daemon yang berjalan dipanggil syslogd (distribusi Linux yang lebih baharu menggunakan rsyslogd), yang menunggu mesej peristiwa berlaku dan menapis yang ingin diketahuinya, dan bergantung pada apa yang sepatutnya dilakukan dengan mesej itu, ia akan menghantarnya ke fail, konsol anda atau tidak melakukan apa-apa dengannya.

Anda mungkin fikir bahawa pencatat sistem ini adalah tempat terpusat untuk mengurus log, tetapi malangnya tidak. Anda akan melihat banyak aplikasi yang menulis peraturan pengelogan mereka sendiri dan menjana fail log yang berbeza, walau bagaimanapun secara amnya format log harus menyertakan cap masa dan butiran peristiwa.

Berikut ialah contoh baris daripada syslog:

<pre>
pete@icebox:~$ less /var/log/syslog
Jan 27 07:41:32 icebox anacron[4650]: Job `cron.weekly' started
</pre>

Di sini kita dapat melihat bahawa pada 27 Jan 07:41:32 perkhidmatan cron kami menjalankan kerja cron.weekly. Anda boleh melihat semua mesej peristiwa yang dikumpulkan oleh syslog dalam fail /var/log/syslog.

## Latihan

Lihat fail /var/log/syslog anda dan lihat apa lagi yang berlaku pada mesin anda.

## Soalan Kuiz

Apakah daemon yang mengurus log pada sistem Linux yang lebih baharu?

## Jawapan Kuiz

rsyslogd
