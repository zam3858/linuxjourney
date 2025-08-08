# direktori /dev

## Kandungan Pelajaran

Apabila anda menyambungkan peranti ke mesin anda, ia biasanya memerlukan pemacu peranti untuk berfungsi dengan betul. Anda boleh berinteraksi dengan pemacu peranti melalui fail peranti atau nod peranti, ini adalah fail khas yang kelihatan seperti fail biasa. Oleh kerana fail peranti ini sama seperti fail biasa, anda boleh menggunakan program seperti ls, cat, dsb untuk berinteraksi dengannya. Fail peranti ini biasanya disimpan dalam direktori /dev. Teruskan dan ls direktori /dev pada sistem anda, anda akan melihat sejumlah besar fail peranti yang ada pada sistem anda.

<pre>$ ls /dev </pre>

Sesetengah peranti ini telah anda gunakan dan berinteraksi dengannya seperti /dev/null. Ingat apabila kita menghantar output ke /dev/null, kernel tahu bahawa peranti ini mengambil semua input kita dan hanya membuangnya, jadi tiada apa yang dikembalikan.

Pada zaman dahulu, jika anda ingin menambah peranti pada sistem anda, anda akan menambah fail peranti dalam /dev dan kemudian mungkin melupakannya. Ulangi itu beberapa kali dan anda boleh lihat di mana masalahnya. Direktori /dev akan menjadi sesak dengan fail peranti statik peranti yang telah lama anda tingkatkan, berhenti menggunakan, dsb. Peranti juga diberikan fail peranti mengikut urutan kernel menemuinya. Jadi jika setiap kali anda but semula sistem anda, peranti boleh mempunyai fail peranti yang berbeza bergantung pada bila ia ditemui.

Syukurlah kita tidak lagi menggunakan kaedah itu, sekarang kita mempunyai sesuatu yang kita gunakan untuk menambah dan mengalih keluar peranti secara dinamik yang sedang digunakan pada sistem dan kita akan membincangkan ini dalam pelajaran yang akan datang.

## Latihan

Semak kandungan direktori /dev, adakah anda mengenali sebarang peranti yang biasa?

## Soalan Kuiz

Di manakah fail peranti disimpan pada sistem?

## Jawapan Kuiz

/dev