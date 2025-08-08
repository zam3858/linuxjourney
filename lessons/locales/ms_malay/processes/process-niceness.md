# niceness

## Kandungan Pelajaran

Apabila anda menjalankan beberapa perkara pada komputer anda, seperti mungkin Chrome, Microsoft Word atau Photoshop pada masa yang sama, ia mungkin kelihatan seperti proses ini berjalan pada masa yang sama, tetapi itu tidak begitu benar.

Proses menggunakan CPU untuk sejumlah kecil masa yang dipanggil hirisan masa. Kemudian mereka berhenti seketika selama milisaat dan proses lain mendapat sedikit hirisan masa. Secara lalai, penjadualan proses berlaku dalam fesyen round-robin ini. Setiap proses mendapat hirisan masa yang mencukupi sehingga ia selesai diproses. Kernel mengendalikan semua penukaran proses ini dan ia melakukan kerja yang cukup baik pada kebanyakan masa.

Proses tidak dapat memutuskan bila dan berapa lama mereka mendapat masa CPU, jika semua proses berkelakuan normal mereka masing-masing akan mendapat jumlah masa CPU yang sama (secara kasar). Walau bagaimanapun, terdapat cara untuk mempengaruhi algoritma penjadualan proses kernel dengan nilai nice. Niceness ialah nama yang agak pelik, tetapi apa yang dimaksudkan ialah proses mempunyai nombor untuk menentukan keutamaan mereka untuk CPU. Nombor yang tinggi bermakna proses itu baik dan mempunyai keutamaan yang lebih rendah untuk CPU dan nombor yang rendah atau negatif bermakna proses itu tidak begitu baik dan ia mahu mendapatkan sebanyak mungkin CPU.

<pre>$ top</pre>

Anda boleh melihat lajur untuk NI sekarang, itu ialah tahap niceness sesuatu proses.

Untuk menukar tahap niceness anda boleh menggunakan arahan nice dan renice:

<pre>$ nice -n 5 apt upgrade</pre>

Arahan nice digunakan untuk menetapkan keutamaan untuk proses baharu. Arahan renice digunakan untuk menetapkan keutamaan pada proses sedia ada.

<pre>$ renice 10 -p 3245</pre>

## Latihan

Proses manakah yang tidak begitu baik dan mengapa?

## Soalan Kuiz

Jika saya mahu proses mendapat lebih banyak keutamaan CPU, adakah saya menggunakan nombor nice yang lebih rendah atau lebih tinggi?

## Jawapan Kuiz

lebih rendah
