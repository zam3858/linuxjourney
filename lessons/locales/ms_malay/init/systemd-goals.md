# Matlamat Systemd

## Kandungan Pelajaran

Kami tidak akan membincangkan butiran penulisan fail unit systemd. Walau bagaimanapun, kami akan memberikan gambaran ringkas tentang fail unit dan cara mengawal unit secara manual.

Berikut ialah fail unit perkhidmatan asas: foobar.service

<pre>
[Unit]
Description=My Foobar
Before=bar.target

[Service]
ExecStart=/usr/bin/foobar

[Install]
WantedBy=multi-user.target
</pre>

Ini ialah sasaran perkhidmatan yang mudah, pada permulaan fail kita melihat bahagian untuk [Unit], ini membolehkan kita memberikan perihalan fail unit kita serta mengawal susunan bila hendak mengaktifkan unit. Bahagian seterusnya ialah bahagian [Perkhidmatan], di bawah sini kita boleh memulakan, menghentikan atau memuat semula perkhidmatan. Dan bahagian [Pasang] digunakan untuk kebergantungan. Ini hanyalah puncak gunung ais untuk menulis fail systemd, jadi saya merayu anda untuk membaca tentang subjek ini jika anda ingin mengetahui lebih lanjut.

Sekarang, mari kita lihat beberapa arahan yang boleh anda gunakan dengan unit systemd:

<b>Senaraikan unit</b>

<pre>$ systemctl list-units</pre>

<b>Lihat status unit</b>

<pre>$ systemctl status networking.service</pre>

<b>Mulakan perkhidmatan</b>

<pre>$ sudo systemctl start networking.service</pre>

<b>Hentikan perkhidmatan</b>

<pre>$ sudo systemctl stop networking.service</pre>

<b>Mulakan semula perkhidmatan</b>

<pre>$ sudo systemctl restart networking.service</pre>

<b>Dayakan unit</b>

<pre>$ sudo systemctl enable networking.service</pre>

<b>Lumpuhkan unit</b>

<pre>$ sudo systemctl disable networking.service</pre>

Sekali lagi, anda masih belum melihat betapa mendalamnya systemd, jadi bacalah tentangnya jika anda ingin mengetahui lebih lanjut.

## Latihan

Lihat status unit dan mulakan serta hentikan beberapa perkhidmatan. Apa yang anda perhatikan?

## Soalan Kuiz

Apakah arahan untuk memulakan perkhidmatan bernama peanut.service?

## Jawapan Kuiz

sudo systemctl start peanut.service