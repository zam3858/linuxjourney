# sysfs

## Kandungan Pelajaran

Sysfs dicipta lama dahulu untuk mengurus peranti pada sistem kita dengan lebih baik yang gagal dilakukan oleh direktori /dev. Sysfs ialah sistem fail maya, selalunya dilekapkan pada direktori /sys. Ia memberi kita maklumat yang lebih terperinci daripada apa yang kita dapat lihat dalam direktori /dev. Kedua-dua direktori /sys dan /dev kelihatan sangat serupa dan dalam beberapa hal ia memang begitu, tetapi ia mempunyai perbezaan besar. Pada asasnya, direktori /dev adalah mudah, ia membolehkan program lain mengakses peranti itu sendiri, manakala sistem fail /sys digunakan untuk melihat maklumat dan mengurus peranti.

Sistem fail /sys pada asasnya mengandungi semua maklumat untuk semua peranti pada sistem anda, seperti pengilang dan model, di mana peranti itu dipalamkan, keadaan peranti, hierarki peranti dan banyak lagi. Fail yang anda lihat di sini bukanlah nod peranti, jadi anda tidak benar-benar berinteraksi dengan peranti dari direktori /sys, sebaliknya anda mengurus peranti.

Lihat kandungan direktori /sys:

<pre>
pete@icebox:~$ ls /sys/block/sda
alignment_offset  discard_alignment  holders   removable  sda6       trace
bdi               events             inflight  ro         size       uevent
capability        events_async       power     sda1       slaves
dev               events_poll_msecs  queue     sda2       stat
device            ext_range          range     sda5       subsystem
</pre>


## Latihan

Semak kandungan direktori /sys dan lihat fail apa yang terdapat di sana.

## Soalan Kuiz

Direktori manakah yang digunakan untuk melihat maklumat terperinci tentang peranti?

## Jawapan Kuiz

/sys