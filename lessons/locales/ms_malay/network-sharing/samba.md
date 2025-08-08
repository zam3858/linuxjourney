# Samba

## Kandungan Pelajaran

Pada zaman awal pengkomputeran, menjadi perlu bagi mesin Windows untuk berkongsi fail dengan mesin Linux, maka lahirlah protokol Server Message Block (SMB). SMB digunakan untuk berkongsi fail antara sistem pengendalian Windows (Mac juga mempunyai perkongsian fail dengan SMB) dan kemudian ia dibersihkan dan dioptimumkan dalam bentuk protokol Common Internet File System (CIFS).

Samba ialah apa yang kita panggil utiliti Linux untuk berfungsi dengan CIFS pada Linux. Selain perkongsian fail, anda juga boleh berkongsi sumber seperti pencetak.

<b>Cipta perkongsian rangkaian dengan Samba</b>

Mari kita lalui langkah asas untuk mencipta perkongsian rangkaian yang boleh diakses oleh mesin Windows:

<b>Pasang Samba</b>

<pre>$ sudo apt update
$ sudo apt install samba</pre>

<b>Sediakan smb.conf</b>

Fail konfigurasi untuk Samba terdapat di /etc/samba/smb.conf, fail ini harus memberitahu sistem direktori mana yang harus dikongsi, kebenaran aksesnya dan pilihan lain. smb.conf lalai dilengkapi dengan banyak kod yang telah dikomen dan anda boleh menggunakannya sebagai contoh untuk menulis konfigurasi anda sendiri.

<pre>$ sudo vi /etc/samba/smb.conf</pre>

<b>Sediakan kata laluan untuk Samba</b>

<pre>$ sudo smbpasswd -a [username]</pre>

<b>Cipta direktori kongsi</b>

<pre>$ mkdir /my/directory/to/share</pre>

<b>Mulakan semula perkhidmatan Samba</b>

<pre>$ sudo service smbd restart</pre>

<b>Mengakses perkongsian Samba melalui Windows</b>

Dalam Windows, hanya taip sambungan rangkaian dalam gesaan larian: \\HOST\sharename.

<b>Mengakses perkongsian Samba/Windows melalui Linux</b>

<pre>$ smbclient //HOST/directory -U user</pre>

Pakej Samba termasuk alat baris perintah yang dipanggil <b>smbclient</b> yang boleh anda gunakan untuk mengakses mana-mana pelayan Windows atau Samba. Sebaik sahaja anda disambungkan ke perkongsian, anda boleh menavigasi dan memindahkan fail.

<b>Lampirkan perkongsian Samba pada sistem anda</b>

Daripada memindahkan fail satu persatu, anda hanya boleh melekapkan perkongsian rangkaian pada sistem anda.

<pre>$ sudo mount -t cifs servername:directory mountpount -o user=username,pass=password</pre>

## Latihan

Sediakan perkongsian Samba, jika anda tidak mempunyainya, buka smb.conf dan biasakan diri anda dengan pilihan dalam fail konfigurasi.

## Soalan Kuiz

Apakah protokol terkini yang digunakan untuk pemindahan fail antara Windows dan Linux?

## Jawapan Kuiz

CIFS
