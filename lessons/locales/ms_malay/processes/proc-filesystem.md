# sistem fail /proc

## Kandungan Pelajaran

Ingat semua dalam Linux adalah fail, malah proses. Maklumat proses disimpan dalam sistem fail khas yang dikenali sebagai sistem fail /proc.

<pre>$ ls /proc</pre>

Anda akan melihat beberapa nilai di sini, terdapat sub-direktori untuk setiap PID. Jika anda melihat PID dalam output ps, anda akan dapat menemuinya dalam direktori /proc.

Teruskan dan masukkan salah satu proses dan lihat fail itu:

<pre>$ cat /proc/12345/status</pre>

Anda akan melihat maklumat keadaan proses dan juga maklumat yang lebih terperinci. Direktori /proc ialah cara kernel melihat sistem, jadi terdapat lebih banyak maklumat di sini daripada apa yang anda akan lihat dalam ps.

## Latihan

Tiada latihan untuk pelajaran ini.

## Soalan Kuiz

Apakah sistem fail yang menyimpan maklumat proses?

## Jawapan Kuiz

/proc