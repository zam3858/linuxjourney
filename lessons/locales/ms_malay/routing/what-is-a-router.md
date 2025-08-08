# Apakah itu penghala?

## Kandungan Pelajaran

Kami telah menggunakan istilah penghala ini sebelum ini, semoga anda tahu apa itu, kerana anda mungkin mempunyainya di rumah anda. Penghala membolehkan mesin pada rangkaian berkomunikasi antara satu sama lain serta rangkaian lain. Pada penghala biasa, anda akan mempunyai port LAN, yang membolehkan mesin anda menyambung ke rangkaian kawasan tempatan yang sama dan anda juga akan mempunyai port pautan naik Internet yang menyambungkan anda ke Internet, kadang-kadang anda akan melihat port ini dilabelkan sebagai WAN, kerana ia pada asasnya menyambungkan anda ke rangkaian yang lebih luas. Apabila kita melakukan sebarang aktiviti rangkaian, ia perlu melalui penghala. Penghala memutuskan ke mana paket rangkaian kami pergi dan yang mana masuk. Ia menghalakan paket kami antara beberapa rangkaian untuk sampai dari hos sumbernya ke hos destinasinya.

<b>Bagaimanakah penghala berfungsi?</b>

Fikirkan tentang penghalaan dengan cara yang sama seperti penghantaran mel, kami mempunyai alamat yang kami ingin hantar surat, apabila kami menghantarnya ke pejabat pos, mereka mendapat surat itu dan melihat, oh ini akan ke California, saya akan meletakkannya di atas trak yang akan ke California (sejujurnya saya tidak tahu bagaimana sistem pos berfungsi). Surat itu kemudiannya dihantar ke San Francisco, di dalam San Francisco terdapat kod pos yang berbeza, dan kemudian dalam kod pos tersebut terdapat kod alamat yang lebih kecil, sehingga akhirnya seseorang dapat menghantar surat anda ke alamat yang anda mahu. Sebaliknya, jika anda sudah tinggal di San Francisco dan dalam kod pos yang sama, penghantar mel mungkin akan tahu dengan tepat ke mana surat itu perlu pergi tanpa menyerahkannya kepada orang lain.

Apabila kita menghalakan paket, ia menggunakan "laluan" alamat yang serupa, seperti untuk sampai ke rangkaian A, hantar paket ini ke rangkaian B. Apabila kita tidak mempunyai laluan yang ditetapkan untuk itu, kita mempunyai laluan lalai yang akan digunakan oleh paket kita. Laluan ini ditetapkan pada jadual penghalaan yang digunakan oleh sistem kita untuk menavigasi kita merentasi rangkaian.

<b>Lompatan</b>

Apabila paket bergerak merentasi rangkaian, ia bergerak dalam lompatan, lompatan ialah cara kita mengukur secara kasar jarak yang perlu dilalui oleh paket untuk sampai dari sumber ke destinasi. Katakan saya mempunyai dua penghala yang menyambungkan hos A ke hos B, jadi oleh itu kita katakan terdapat dua lompatan antara hos A dan hos B. Setiap lompatan ialah peranti perantaraan seperti penghala yang perlu kita lalui.

<b>Memahami perbezaan asas antara Penukaran, Penghalaan & Banjir?</b>
PENUKARAN paket pada asasnya menerima, memproses dan memajukan data ke peranti destinasi.
PENGHALAAN ialah proses mencipta jadual penghalaan, supaya kita boleh melakukan PENUKARAN dengan lebih baik.
Sebelum penghalaan, BANJIR digunakan. Jika penghala tidak tahu ke mana hendak menghantar paket, maka setiap paket yang masuk dihantar melalui setiap pautan keluar kecuali yang ia tiba.

## Latihan

Tiada latihan untuk pelajaran ini.

## Soalan Kuiz

Bagaimanakah paket mengukur jarak?

## Jawapan Kuiz

lompatan
