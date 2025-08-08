# Repositori Pakej

## Kandungan Pelajaran

Bagaimanakah pakej yang dimuat naik ke internet entah bagaimana berakhir di komputer kita? Adakah anda pergi ke halaman muat turun setiap pakej yang anda mahu dan klik muat turun dan pasang? Sebenarnya, anda boleh melakukannya, tetapi ada sesuatu yang lebih baik yang dipanggil repositori pakej. Repositori hanyalah lokasi storan pusat untuk pakej. Terdapat banyak repositori yang menyimpan banyak pakej dan yang terbaik ialah semuanya terdapat di internet, tiada cakera pemasangan yang tidak masuk akal. Mesin anda tidak tahu di mana hendak mencari repositori ini melainkan anda memberitahunya secara eksplisit di mana hendak mencari.

Sebagai contoh, katakan saya mahu Perisian WackyWidgets pada mesin saya. WackyWidgets menguruskan repositori mereka sendiri untuk pakej widget mereka, di dalam repositori ini terdapat 10 pakej, pakej CoolWidget, pakej SuperWidget, dsb. WackyWidgets mengehoskan repositori ini pada pautan sumber yang dipanggil: http://download.widgets/linux/deb/

Sekarang daripada pergi ke laman web mereka untuk memuat turun pakej secara terus, anda boleh memberitahu mesin anda untuk mencari perisian WackyWidgets dari pautan sumber.

Distribusi anda sudah dilengkapi dengan sumber yang telah diluluskan untuk mendapatkan pakej dan inilah cara ia memasang semua pakej asas yang anda lihat pada sistem anda. Pada sistem Debian, fail sumber ini ialah fail <b>/etc/apt/sources.list</b>. Mesin anda akan tahu untuk mencari di sana dan memeriksa sebarang repositori sumber yang anda tambahkan.

## Latihan

Tiada latihan untuk pelajaran ini.

## Soalan Kuiz

Di manakah fail sumber dalam sistem Debian?

## Jawapan Kuiz

/etc/apt/sources.list