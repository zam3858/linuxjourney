# Laluan Paket

## Kandungan Pelajaran

<b>Mari kita lihat bagaimana paket bergerak dalam rangkaian tempatannya</b>

<ol>
<li>Mula-mula mesin tempatan akan membandingkan alamat IP destinasi untuk melihat sama ada ia berada dalam subnet yang sama dengan melihat topeng subnetnya.</li>
<li>Apabila paket dihantar, ia perlu mempunyai alamat MAC sumber, alamat MAC destinasi, alamat IP sumber dan alamat IP destinasi, pada ketika ini kita tidak tahu alamat MAC destinasi.</li>
<li>Untuk sampai ke hos destinasi, kami menggunakan ARP untuk menyiarkan permintaan pada rangkaian tempatan untuk mencari alamat MAC hos destinasi.</li>
<li>Sekarang paket boleh dihantar dengan jayanya!</li>
</ol>

<b>Mari kita lihat bagaimana paket bergerak di luar rangkaiannya</b>

<ol>
<li>Mula-mula mesin tempatan akan membandingkan alamat IP destinasi, kerana ia berada di luar rangkaian kami, ia tidak melihat alamat MAC hos destinasi. Dan kami tidak boleh menggunakan ARP kerana permintaan ARP ialah siaran kepada hos yang disambungkan secara tempatan.</li>
<li>Jadi paket kami sekarang melihat jadual penghalaan, ia tidak tahu alamat IP destinasi, jadi ia menghantarnya ke get laluan lalai (penghala lain). Jadi sekarang paket kami mengandungi IP sumber, IP destinasi dan MAC sumber kami, walau bagaimanapun kami tidak mempunyai MAC destinasi. Ingat alamat MAC hanya dicapai melalui rangkaian yang sama. Jadi apa yang dilakukannya? Ia menghantar permintaan ARP untuk mendapatkan alamat MAC get laluan lalai.</li>
<li>Penghala melihat paket dan mengesahkan alamat MAC destinasi, tetapi ia bukan alamat IP destinasi akhir, jadi ia terus melihat jadual penghalaan untuk memajukan paket ke alamat IP lain yang boleh membantu paket bergerak ke destinasinya. Setiap kali paket bergerak, ia menanggalkan alamat MAC sumber dan destinasi lama dan mengemas kini paket dengan alamat MAC sumber dan destinasi baharu.</li>
<li>Sebaik sahaja paket dimajukan ke rangkaian yang sama, kami menggunakan ARP untuk mencari alamat MAC destinasi akhir</li>
<li>Semasa proses ini, paket kami tidak mengubah alamat IP sumber atau destinasi.</li>
</ol>

## Latihan

Tiada latihan untuk pelajaran ini.

## Soalan Kuiz

Bagaimanakah kita mencari alamat MAC bagi alamat IP?

## Jawapan Kuiz

ARP
