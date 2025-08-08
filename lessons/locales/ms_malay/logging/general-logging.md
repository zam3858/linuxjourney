# Pengelogan Umum

## Kandungan Pelajaran

Terdapat banyak fail log yang boleh anda lihat pada sistem anda, banyak yang penting boleh didapati di bawah /var/log. Kami tidak akan meneliti kesemuanya, tetapi kami akan membincangkan beberapa yang utama.

Terdapat dua fail log umum yang boleh anda lihat untuk mendapatkan gambaran tentang apa yang sistem anda lakukan:

<b>/var/log/messages</b>

Log ini mengandungi semua mesej bukan kritikal dan bukan debug, termasuk mesej yang dicatat semasa but (dmesg), auth, cron, daemon, dsb. Sangat berguna untuk mendapatkan gambaran tentang bagaimana mesin anda bertindak.

<b>/var/log/syslog</b>

Ini mencatat segala-galanya kecuali mesej pengesahan, ia sangat berguna untuk menyahpepijat ralat pada mesin anda.

Kedua-dua log ini sepatutnya lebih daripada cukup semasa menyelesaikan masalah dengan sistem anda, Walau bagaimanapun, jika anda hanya ingin melihat komponen log tertentu, terdapat juga log berasingan untuknya juga.

## Latihan

Lihat fail /var/log/messages dan /var/log/syslog anda dan lihat apakah perbezaannya.

## Soalan Kuiz

Fail log manakah yang mencatat segala-galanya kecuali mesej pengesahan?

## Jawapan Kuiz

syslog