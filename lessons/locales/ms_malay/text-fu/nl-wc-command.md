# wc dan nl

## Kandungan Pelajaran

Perintah wc (kiraan perkataan) menunjukkan jumlah kiraan perkataan dalam fail.

<pre>$ wc /etc/passwd
 96     265    5925 /etc/passwd
</pre>

Ia memaparkan bilangan baris, bilangan perkataan dan bilangan bait, masing-masing.

Untuk hanya melihat kiraan medan tertentu, gunakan -l, -w, atau -c masing-masing.

<pre>$ wc -l /etc/passwd
96</pre>

Satu lagi arahan yang boleh anda gunakan untuk menyemak kiraan baris pada fail ialah arahan nl (baris nombor).

<pre>
file1.txt
saya
suka
penyu
</pre>

<pre>$ nl file1.txt
1. saya
2. suka
3. penyu
</pre>

## Latihan

Bagaimanakah anda akan mendapatkan jumlah kiraan baris dengan menggunakan fail nl tanpa mencari melalui keseluruhan output? Petunjuk: Gunakan beberapa arahan lain yang anda pelajari dalam kursus ini.

## Soalan Kuiz

Apakah arahan yang akan anda gunakan untuk mendapatkan jumlah perkataan dalam fail dan hanya perkataan?

## Jawapan Kuiz

wc -w