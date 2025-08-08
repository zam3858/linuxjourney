# udev

## Kandungan Pelajaran

Pada zaman dahulu dan sebenarnya hari ini jika anda benar-benar mahu, anda akan mencipta nod peranti menggunakan arahan seperti:

<pre>$ mknod /dev/sdb1 b 8 3</pre>

Perintah ini akan membuat nod peranti /dev/sdb1 dan ia akan menjadikannya peranti blok (b) dengan nombor utama 8 dan nombor kecil 3.

Untuk mengalih keluar peranti, anda hanya perlu <b>rm</b> fail peranti dalam direktori /dev.

Nasib baik, kita tidak perlu melakukan ini lagi kerana udev. Sistem udev secara dinamik mencipta dan mengalih keluar fail peranti untuk kita bergantung pada sama ada ia disambungkan atau tidak. Terdapat daemon udevd yang berjalan pada sistem dan ia mendengar mesej daripada kernel tentang peranti yang disambungkan ke sistem. Udevd akan menghuraikan maklumat itu dan ia akan memadankan data dengan peraturan yang dinyatakan dalam /etc/udev/rules.d, bergantung pada peraturan tersebut ia kemungkinan besar akan mencipta nod peranti dan pautan simbolik untuk peranti tersebut. Anda boleh menulis peraturan udev anda sendiri, tetapi itu sedikit di luar skop pelajaran ini. Nasib baik, sistem anda sudah dilengkapi dengan banyak peraturan udev jadi anda mungkin tidak perlu menulis sendiri.

Anda juga boleh melihat pangkalan data udev dan sysfs menggunakan arahan <b>udevadm</b>. Alat ini sangat berguna, tetapi kadang-kadang boleh menjadi sangat berbelit-belit, arahan mudah untuk melihat maklumat untuk peranti ialah:

<pre>$ udevadm info --query=all --name=/dev/sda</pre>

## Latihan

Jalankan arahan udevadm yang diberikan dan semak input.

## Soalan Kuiz

Apakah yang menambah dan mengalih keluar peranti secara dinamik?

## Jawapan Kuiz

udev