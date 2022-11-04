
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












