# Pemantauan CPU

## Kandungan Pelajaran

Mari kita lihat arahan yang berguna, <b>uptime</b>.

<pre>
pete@icebox:~$ uptime
 17:23:35 up 1 day,  5:59,  2 users,  load average: 0.00, 0.02, 0.05
</pre>

Kita telah membincangkan tentang uptime dalam pelajaran pertama kursus ini, tetapi kita belum membincangkan medan purata beban. Purata beban ialah cara yang baik untuk melihat beban CPU pada sistem anda. Nombor ini mewakili purata beban CPU dalam selang 1, 5, dan 15 minit. Apakah yang saya maksudkan dengan beban CPU, beban CPU ialah purata bilangan proses yang sedang menunggu untuk dilaksanakan oleh CPU.

Katakan anda mempunyai CPU teras tunggal, anggap teras ini sebagai satu lorong dalam lalu lintas. Jika waktu sibuk di lebuh raya, lorong ini akan sangat sibuk dan lalu lintas akan berada pada 100% atau beban 1. Sekarang lalu lintas menjadi sangat teruk, ia menyandarkan lebuh raya dan membuat jalan biasa sibuk dengan dua kali ganda jumlah kereta, kita boleh katakan beban anda ialah 200% atau beban 2. Sekarang katakan ia reda sedikit dan hanya separuh kereta di lorong lebuh raya, kita boleh katakan beban lorong ialah 0.5. Apabila lalu lintas tidak wujud dan kita boleh pulang lebih cepat, beban sepatutnya sangat rendah, seperti lalu lintas 2 pagi yang rendah. Kereta dalam kes ini adalah proses dan proses ini hanya menunggu untuk keluar dari lebuh raya dan pulang ke rumah.

Sekarang hanya kerana anda mempunyai purata beban 1 tidak bermakna komputer anda lembap. Kebanyakan mesin moden hari ini mempunyai beberapa teras. Jika anda mempunyai pemproses empat teras (4 teras) dan purata beban anda ialah 1, ia sebenarnya hanya menjejaskan 25% daripada CPU anda. Anggap setiap teras sebagai lorong dalam lalu lintas. Anda boleh melihat jumlah teras yang anda ada pada sistem anda dengan <b>cat /proc/cpuinfo</b>.

Apabila memerhatikan purata beban, anda perlu mengambil kira bilangan teras, jika anda mendapati mesin anda sentiasa menggunakan beban purata yang lebih tinggi daripada biasa, mungkin ada sesuatu yang tidak kena.

## Latihan

Semak purata beban sistem anda dan lihat apa yang dilakukannya.

## Soalan Kuiz

Apakah arahan yang boleh anda gunakan untuk melihat purata beban?

## Jawapan Kuiz

uptime
