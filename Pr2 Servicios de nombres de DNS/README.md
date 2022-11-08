
Volvemos a editar el fichero `named.conf.local` con:
<pre><code>sudo nano /etc/bind/named.conf.local</code></pre>
y añadimos de manera que quede así:

//
// Do any local configuration here
//

// Consider adding the 1918 zones here, if they are not used in your
// organization
//include "/etc/bind/zones.rfc1918";

zone "stucomx.net" {
    type master;
    file "/etc/bind/db.stucomx.net";
};

zone "141.168.192.in-addr.arpa"{
    type master;
    file "/etc/bind/db.141.168.192.in-addr.arpa";
};





Volvemos a editar el fichero db.stucomx.net con:
<pre><code>sudo nano /etc/bind/db.stucomx.net</code></pre>
y añadimos de manera que quede así:

@        IN       NS       localhost.\
@   IN  MX  1   ASPMX.L.GOOGLE.COM\
@   IN  MX  5   ALT1.ASPMX.L.GOOGLE.COM\
@   IN  MX  5   ALT2.ASPMX.L.GOOGLE.COM\
@   IN  MX  10   ALT3.ASPMX.L.GOOGLE.COM\
@   IN  MX  10   ALT4.ASPMX.L.GOOGLE.COM\
@   IN  TXT "v=sp1 a:mail.google.com -all"\
@ IN  CAA    0   issue "letsencrypt.org"

Ahora para hacerlo más ágil copiamos la plantilla /etc/bind/db.empty y la pegamos, de esta manera:

<pre><code>sudo cp db.empty db.141.168.192.in-addr.arpa</code></pre>

Ahora con `sudo nano /etc/bind/db.141.168.192.in-addr-arpa` editamos y añadimos de manera que quede así;


1   IN  PTR dns\
200 IN  PTR printer\
42  IN  PTR pc42\
43  IN  PTR pc43\
44  IN  PTR pc44\
45  IN  PTR pc45\
46  IN  PTR pc46\
47  IN  PTR pc47\
48  IN  PTR pc48\
49  IN  PTR pc49\
50  IN  PTR pc50