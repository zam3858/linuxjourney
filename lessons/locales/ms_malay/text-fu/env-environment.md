# env (Persekitaran)

## Kandungan Pelajaran

Jalankan arahan berikut:

<pre>$ echo $HOME</pre>

Anda akan melihat laluan ke direktori rumah anda, saya kelihatan seperti /home/pete.

Bagaimana pula dengan arahan ini?

<pre>$ echo $USER </pre>

Anda akan melihat nama pengguna anda!

Dari manakah maklumat ini datang? Ia datang dari pembolehubah persekitaran anda. Anda boleh melihatnya dengan menaip

<pre>$ env </pre>

Ini mengeluarkan banyak maklumat tentang pembolehubah persekitaran yang sedang anda tetapkan. Pembolehubah ini mengandungi maklumat berguna yang boleh digunakan oleh shell dan proses lain.

Berikut ialah contoh ringkas:

<pre>
PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/bin
PWD=/home/user
USER=pete
</pre>


Satu pembolehubah yang sangat penting ialah Pembolehubah PATH. Anda boleh mengakses pembolehubah ini dengan meletakkan $ di hadapan nama pembolehubah seperti ini:

<pre>
$ echo $PATH
/usr/local/sbin:/usr/local/bin:/usr/sbin:/bin
</pre>

Ini mengembalikan senarai laluan yang dipisahkan oleh titik bertindih yang dicari oleh sistem anda apabila ia menjalankan arahan. Katakan anda memuat turun dan memasang pakej secara manual dari internet dan meletakkannya dalam direktori bukan standard dan ingin menjalankan arahan itu, anda menaip $ coolcommand dan gesaan mengatakan arahan tidak ditemui. Itu tidak masuk akal kerana anda melihat binari dalam folder dan tahu ia wujud. Apa yang berlaku ialah pembolehubah $PATH tidak memeriksa direktori itu untuk binari ini jadi ia memaparkan ralat.

Katakan anda mempunyai banyak binari yang ingin anda jalankan dari direktori itu, anda hanya boleh mengubah suai pembolehubah PATH untuk memasukkan direktori itu dalam pembolehubah persekitaran PATH anda.


## Latihan

Apakah output berikut? Mengapa?
<pre>$ echo $HOME</pre>

## Soalan Kuiz

Bagaimanakah anda melihat pembolehubah persekitaran anda?

## Jawapan Kuiz

env
