# Isyarat

## Kandungan Pelajaran

Isyarat ialah pemberitahuan kepada proses bahawa sesuatu telah berlaku.

<b>Mengapa kita mempunyai isyarat</b>

Ia adalah sampukan perisian dan ia mempunyai banyak kegunaan:

<ul>
<li>Pengguna boleh menaip salah satu aksara terminal khas (Ctrl-C) atau (Ctrl-Z) untuk membunuh, mengganggu atau menggantung proses</li>
<li>Isu perkakasan boleh berlaku dan kernel ingin memberitahu proses</li>
<li>Isu perisian boleh berlaku dan kernel ingin memberitahu proses</li>
<li>Ia pada asasnya cara proses boleh berkomunikasi</li>
</ul>

<b>Proses isyarat</b>

Apabila isyarat dijana oleh beberapa peristiwa, ia kemudiannya dihantar ke proses, ia dianggap dalam keadaan belum selesai sehingga ia dihantar. Apabila proses dijalankan, isyarat akan dihantar. Walau bagaimanapun, proses mempunyai topeng isyarat dan ia boleh menetapkan penghantaran isyarat untuk disekat jika dinyatakan. Apabila isyarat dihantar, proses boleh melakukan pelbagai perkara:

<ul>
<li>Abaikan isyarat</li>
<li>"Tangkap" isyarat dan lakukan rutin pengendali tertentu</li>
<li>Proses boleh ditamatkan, berbanding dengan panggilan sistem keluar biasa</li>
<li>Sekat isyarat, bergantung pada topeng isyarat</li>
</ul>

<b>Isyarat biasa</b>

Setiap isyarat ditakrifkan oleh integer dengan nama simbolik yang dalam bentuk SIGxxx. Beberapa isyarat yang paling biasa ialah:

<ul>
<li>SIGHUP atau HUP atau 1: Gantung</li>
<li>SIGINT atau INT atau 2: Sampukan</li>
<li>SIGKILL atau KILL atau 9: Bunuh</li>
<li>SIGSEGV atau SEGV atau 11: Kesalahan segmentasi</li>
<li>SIGTERM atau TERM atau 15: Penamatan perisian</li>
<li>SIGSTOP atau STOP: Henti</li>
</ul>

Nombor boleh berbeza-beza dengan isyarat jadi ia biasanya dirujuk dengan nama mereka.

Sesetengah isyarat tidak boleh disekat, satu contoh ialah isyarat SIGKILL. Isyarat KILL memusnahkan proses.

## Latihan

Tiada latihan untuk pelajaran ini.

## Soalan Kuiz

Isyarat manakah yang tidak boleh disekat?

## Jawapan Kuiz

SIGKILL