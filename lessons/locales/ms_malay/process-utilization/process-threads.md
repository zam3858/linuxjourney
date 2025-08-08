# Benang Proses

## Kandungan Pelajaran

Anda mungkin pernah mendengar istilah proses benang tunggal dan berbilang benang. Benang sangat serupa dengan proses, kerana ia digunakan untuk melaksanakan program yang sama, ia sering dirujuk sebagai proses ringan. Jika proses mempunyai satu benang ia adalah benang tunggal dan jika proses mempunyai lebih daripada satu benang ia adalah berbilang benang. Walau bagaimanapun, semua proses mempunyai sekurang-kurangnya satu benang.

Proses beroperasi dengan sumber sistem terpencil mereka sendiri, walau bagaimanapun benang boleh berkongsi sumber ini antara satu sama lain dengan mudah, menjadikannya lebih mudah untuk mereka berkomunikasi antara satu sama lain dan kadangkala lebih cekap untuk mempunyai aplikasi berbilang benang daripada aplikasi berbilang proses.

Pada asasnya, katakan anda membuka LibreOffice Writer dan Chrome, setiap satunya ialah proses yang berasingan. Sekarang anda masuk ke dalam Writer dan mula menyunting teks, apabila anda menyunting teks ia akan disimpan secara automatik. Kedua-dua "proses ringan" selari menyimpan dan menyunting ini adalah benang.

Untuk melihat benang proses, anda boleh menggunakan:

<pre>
pete@icebox:~$ ps m
  PID TTY      STAT   TIME COMMAND
 2207 pts/2    -      0:01 bash
    - -        Ss     0:01 -
 5252 pts/2    -      0:00 ps m
    - -        R+     0:00 -
</pre>

Proses ditandakan dengan setiap PID dan di bawah proses adalah benang mereka (ditandakan dengan --). Jadi anda boleh lihat bahawa proses di atas kedua-duanya adalah benang tunggal.

## Latihan

Jalankan arahan <b>ps m</b> dan lihat proses apa yang anda jalankan adalah berbilang benang.

## Soalan Kuiz

Benar atau salah, semua proses bermula sebagai benang tunggal.

## Jawapan Kuiz

Benar
