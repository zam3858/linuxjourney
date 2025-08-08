# stderr (Ralat Standard)

## Kandungan Pelajaran

Mari kita cuba sesuatu yang sedikit berbeza sekarang, mari kita cuba senaraikan kandungan direktori yang tidak wujud pada sistem anda dan halakan semula output ke fail peanuts.txt sekali lagi.

<pre>$ ls /fake/directory > peanuts.txt </pre>

Apa yang anda akan lihat ialah:

<pre>ls: cannot access /fake/directory: No such file or directory</pre>

Sekarang anda mungkin berfikir, bukankah mesej itu sepatutnya dihantar ke fail? Sebenarnya terdapat satu lagi strim I/O yang dimainkan di sini yang dipanggil ralat standard (stderr). Secara lalai, stderr juga menghantar outputnya ke skrin, ia adalah strim yang sama sekali berbeza daripada stdout. Jadi anda perlu menghalakan semula outputnya dengan cara yang berbeza.

Malangnya pengalih hala tidak sebagus menggunakan <b>&lt;</b> atau <b>&gt;</b> tetapi ia agak hampir. Kita perlu menggunakan deskriptor fail. Deskriptor fail ialah nombor bukan negatif yang digunakan untuk mengakses fail atau strim. Kita akan membincangkan secara mendalam tentang ini kemudian, tetapi buat masa ini ketahuilah bahawa deskriptor fail untuk stdin, stdout dan stderr masing-masing ialah 0, 1, dan 2.

Jadi sekarang jika kita mahu menghalakan semula stderr kita ke fail, kita boleh melakukan ini:

<pre>$ ls /fake/directory 2> peanuts.txt</pre>

Anda akan melihat hanya mesej stderr dalam peanuts.txt.

Sekarang bagaimana jika saya ingin melihat kedua-dua stderr dan stdout dalam fail peanuts.txt? Ia boleh dilakukan dengan menggunakan deskriptor fail juga:

<pre>$ ls /fake/directory > peanuts.txt 2>&1</pre>

Ini menghantar hasil ls /fake/directory ke fail peanuts.txt dan kemudian ia menghalakan semula stderr ke stdout melalui 2>&1. Urutan operasi di sini penting, 2>&1 menghantar stderr ke mana sahaja stdout menunjuk. Dalam kes ini stdout menunjuk ke fail, jadi 2>&1 juga menghantar stderr ke fail. Jadi jika anda membuka fail peanuts.txt itu anda akan melihat kedua-dua stderr dan stdout. Dalam kes kami, arahan di atas hanya mengeluarkan stderr.

Terdapat cara yang lebih pendek untuk menghalakan semula kedua-dua stdout dan stderr ke fail:

<pre>$ ls /fake/directory &> peanuts.txt</pre>

Sekarang bagaimana jika saya tidak mahu sebarang sampah itu dan ingin menyingkirkan mesej stderr sepenuhnya? Anda juga boleh menghalakan semula output ke fail khas yang dipanggil /dev/null dan ia akan membuang sebarang input.

<pre>$ ls /fake/directory 2> /dev/null</pre>

## Latihan

Apakah yang dilakukan oleh arahan berikut?

<pre>$ ls /fake/directory >> /dev/null 2>&1</pre>

## Soalan Kuiz

Apakah pengalih hala untuk stderr?

## Jawapan Kuiz

2>
