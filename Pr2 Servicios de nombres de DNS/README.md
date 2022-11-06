
Volvemos a editar el fichero con:
<pre><code>sudo nano /etc/bind/db.stucomx.net</code></pre>
y añadimos esto:

@        IN       NS       localhost.\
@   IN  MX  1   ASPMX.L.GOOGLE.COM\
@   IN  MX  5   ALT1.ASPMX.L.GOOGLE.COM\
@   IN  MX  5   ALT2.ASPMX.L.GOOGLE.COM\
@   IN  MX  10   ALT3.ASPMX.L.GOOGLE.COM\
@   IN  MX  10   ALT4.ASPMX.L.GOOGLE.COM\
@   IN  TXT "v=sp1 a:mail.google.com -all"\
@ IN  CAA    0   issue "letsencrypt.org"

Db.141.168.192.in-addr.arpa

1   IN  PTR dns
200 IN  PTR printer
42  IN  PTR pc42
43  IN  PTR pc43
44  IN  PTR pc44
45  IN  PTR pc45
46  IN  PTR pc46
47  IN  PTR pc47
48  IN  PTR pc48
49  IN  PTR pc49
50  IN  PTR pc50