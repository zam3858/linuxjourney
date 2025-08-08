# bunuh (Tamatkan)

## Kandungan Pelajaran

Anda boleh menghantar isyarat yang menamatkan proses, arahan sedemikian dinamakan dengan tepat sebagai arahan bunuh.

<pre>$ kill 12445</pre>

12445 ialah PID proses yang ingin anda bunuh. Secara lalai ia menghantar isyarat TERM. Isyarat SIGTERM dihantar ke proses untuk meminta penamatannya dengan membenarkannya melepaskan sumbernya dengan bersih dan menyimpan keadaannya.

Anda juga boleh menentukan isyarat dengan arahan bunuh:

<pre>$ kill -9 12445</pre>

Ini akan menjalankan isyarat SIGKILL dan membunuh proses itu.

<b>Perbezaan antara SIGHUP, SIGINT, SIGTERM, SIGKILL, SIGSTOP?</b>

Isyarat ini semuanya kedengaran agak serupa, tetapi ia mempunyai perbezaan.

<ul>
<li>SIGHUP - Gantung, dihantar ke proses apabila terminal kawalan ditutup. Sebagai contoh, jika anda menutup tetingkap terminal yang mempunyai proses yang berjalan di dalamnya, anda akan mendapat isyarat SIGHUP. Jadi pada asasnya anda telah digantung</li>
<li>SIGINT - Adalah isyarat sampukan, jadi anda boleh menggunakan Ctrl-C dan sistem akan cuba membunuh proses itu dengan anggun</li>
<li>SIGTERM - Bunuh proses, tetapi benarkan ia melakukan beberapa pembersihan terlebih dahulu</li>
<li>SIGKILL - Bunuh proses, bunuh dengan api, tidak melakukan sebarang pembersihan</li>
<li>SIGSTOP - Hentikan/gantung proses</li>
</ul>

## Latihan

Bunuh beberapa proses menggunakan isyarat yang berbeza.

## Soalan Kuiz

Apakah nama isyarat untuk arahan bunuh lalai?

## Jawapan Kuiz

SIGTERM