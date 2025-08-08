# syslog

## Kandungan Pelajaran

Perkhidmatan syslog mengurus dan menghantar log ke pencatat sistem. Rsyslog ialah versi syslog yang lebih maju, kebanyakan distribusi Linux harus menggunakan versi baharu ini. Output semua log yang dikumpulkan oleh perkhidmatan syslog boleh didapati di /var/log/syslog (setiap mesej kecuali mesej pengesahan).

Untuk mengetahui fail apa yang diselenggara oleh pencatat sistem kami, lihat fail konfigurasi dalam /etc/rsyslog.d:

<pre>
pete@icebox:~$ less /etc/rsyslog.d/50-default.conf
# First some standard log files.  Log by facility.
#
auth,authpriv.*                 /var/log/auth.log
*.*;auth,authpriv.none          -/var/log/syslog
#cron.*                         /var/log/cron.log
#daemon.*                       -/var/log/daemon.log
kern.*                          -/var/log/kern.log
#lpr.*                          -/var/log/lpr.log
mail.*                          -/var/log/mail.log
#user.*                         -/var/log/user.log
</pre>

Peraturan untuk log fail ini ditandakan oleh pemilih pada lajur kiri dan tindakan pada lajur kanan. Tindakan itu memberitahu kami ke mana hendak menghantar maklumat log, dalam fail, konsol, dsb. Ingat tidak setiap aplikasi dan perkhidmatan menggunakan rsyslog untuk mengurus log mereka, jadi jika anda ingin mengetahui secara khusus apa yang dilog, anda perlu melihat di dalam direktori ini.

Mari kita lihat pengelogan dalam tindakan, anda boleh menghantar log secara manual dengan arahan logger:

<pre>
logger -s Hello
</pre>

Sekarang lihat di dalam /var/log/syslog anda dan anda akan melihat entri ini dalam log anda!

## Latihan

Lihat fail konfigurasi /etc/rsyslog.d anda dan lihat apa lagi yang dilog melalui pencatat sistem.

## Soalan Kuiz

Apakah arahan yang boleh anda gunakan untuk mencatat mesej secara manual?

## Jawapan Kuiz

logger