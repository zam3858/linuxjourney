# Pembaikan Sistem Fail

## Kandungan Pelajaran

Kadang-kadang sistem fail kita tidak sentiasa dalam keadaan terbaik, jika kita mengalami penutupan secara tiba-tiba, data kita boleh menjadi rosak. Terpulang kepada sistem untuk cuba membawa kita kembali ke keadaan berfungsi (walaupun kita pasti boleh mencubanya sendiri).

Perintah <b>fsck</b> (pemeriksaan sistem fail) digunakan untuk memeriksa ketekalan sistem fail dan malah boleh cuba membaikinya untuk kita. Biasanya apabila anda but cakera, fsck akan berjalan sebelum cakera anda dilekapkan untuk memastikan semuanya ok. Walau bagaimanapun, kadang-kadang cakera anda begitu teruk sehingga anda perlu melakukannya secara manual. Walau bagaimanapun, pastikan anda melakukan ini semasa anda berada dalam cakera penyelamat atau di suatu tempat di mana anda boleh mengakses sistem fail anda tanpa ia dilekapkan.

<pre>$ sudo fsck /dev/sda</pre>

## Latihan

Lihat halaman manual untuk fsck untuk melihat apa lagi yang boleh dilakukannya.

## Soalan Kuiz

Apakah arahan yang digunakan untuk memeriksa integriti sistem fail?

## Jawapan Kuiz

fsck