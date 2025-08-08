# rpm dan dpkg

## Kandungan Pelajaran

Walaupun kebanyakan kursus ini adalah mengenai sistem pengurusan pakej (Batman pengurusan pakej), kita tidak boleh melupakan Robin. Walaupun sangat berguna dan boleh dipercayai, mereka tidak datang dengan batmobile dan tali pinggang utiliti yang manis itu.

Sama seperti .exe ialah fail boleh laksana tunggal, begitu juga .deb dan .rpm. Anda biasanya tidak akan melihat ini jika anda menggunakan repositori pakej, tetapi jika anda memuat turun pakej secara terus, kemungkinan besar anda akan mendapatkannya dalam format popular ini. Jelas sekali, ia adalah eksklusif untuk distribusi mereka, .deb untuk berasaskan Debian dan .rpm untuk berasaskan Red Hat.

Untuk memasang pakej terus ini, anda boleh menggunakan arahan pengurusan pakej: rpm dan dpkg. Alat ini digunakan untuk memasang fail pakej, walau bagaimanapun ia tidak akan memasang kebergantungan pakej, jadi jika pakej anda mempunyai 10 kebergantungan, anda perlu memasang pakej tersebut secara berasingan dan kemudian kebergantungannya dan seterusnya. Seperti yang anda lihat, itu adalah salah satu sebab yang melahirkan sistem pengurusan penuh yang akan kita bincangkan kemudian.

Perlu diingat bahawa akan ada banyak kali apabila anda perlu memasang, menanyakan atau mengesahkan pakej dengan salah satu alat ini, jadi ingatlah arahan ini.

<b>Pasang pakej</b>

<pre>
Debian: $ dpkg -i some_deb_package.deb
RPM: $ rpm -i some_rpm_package.rpm
</pre>

<b>i</b> bermaksud pasang. Anda juga boleh menggunakan format yang lebih panjang --install.

<b>Alih keluar pakej</b>

<pre>
Debian: $ dpkg -r some_deb_package.deb
RPM: $ rpm -e some_rpm_package.rpm
</pre>

Debian: <b>r</b> untuk alih keluar
RPM: <b>e</b> untuk padam

<b>Senaraikan pakej yang dipasang</b>

<pre>
Debian: $ dpkg -l
RPM: $ rpm -qa
</pre>

Debian: <b>l</b> untuk senarai
RPM: <b>q</b> untuk pertanyaan dan <b>a</b> untuk semua

## Latihan

Cari program yang ingin anda pasang pada sistem anda seperti Google Chrome dan pasangkannya menggunakan salah satu arahan ini.

## Soalan Kuiz

Apakah alat pengurusan pakej untuk fail .deb?

## Jawapan Kuiz

dpkg
