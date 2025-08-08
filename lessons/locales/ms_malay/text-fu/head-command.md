# kepala

## Kandungan Pelajaran

Katakan kita mempunyai fail yang sangat panjang, sebenarnya kita mempunyai banyak pilihan, teruskan dan cat /var/log/syslog. Anda akan melihat halaman demi halaman teks. Bagaimana jika saya hanya ingin melihat beberapa baris pertama dalam fail teks ini? Kita boleh melakukannya dengan arahan kepala, secara lalai arahan kepala akan menunjukkan kepada anda 10 baris pertama dalam fail.

<pre>$ head /var/log/syslog</pre>

Anda juga boleh mengubah suai kiraan baris kepada apa sahaja yang anda pilih, katakan saya ingin melihat 15 baris pertama sebaliknya.

<pre>$ head -n 15 /var/log/syslog</pre>

Bendera -n bermaksud bilangan baris.

## Latihan

Apakah yang dilakukan oleh arahan berikut dan mengapa?

<pre>$ head -c 15 /var/log/syslog</pre>

## Soalan Kuiz

Apakah bendera yang akan anda gunakan untuk menukar bilangan baris yang ingin anda lihat untuk arahan kepala?

## Jawapan Kuiz

-n