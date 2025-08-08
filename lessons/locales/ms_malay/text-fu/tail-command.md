# ekor

## Kandungan Pelajaran

Sama seperti arahan kepala, arahan ekor membolehkan anda melihat 10 baris terakhir fail secara lalai.

<pre>$ tail /var/log/syslog</pre>

Bersama dengan kepala anda boleh menukar bilangan baris yang ingin anda lihat.

<pre>$ tail -n 10 /var/log/syslog</pre>

Satu lagi pilihan hebat yang boleh anda gunakan ialah bendera -f (ikut), ini akan mengikuti fail semasa ia berkembang. Cubalah dan lihat apa yang berlaku.

<pre>$ tail -f /var/log/syslog</pre>

Fail syslog anda akan sentiasa berubah semasa anda berinteraksi dengan sistem anda dan menggunakan tail -f anda boleh melihat semua yang ditambahkan pada fail itu.

## Latihan

Lihat halaman manual ekor dan baca beberapa arahan lain yang tidak kami bincangkan.

<pre>$ man tail</pre>

## Soalan Kuiz

Apakah bendera yang digunakan untuk mengikuti fail dalam ekor?

## Jawapan Kuiz

-f