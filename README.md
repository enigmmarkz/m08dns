# m08dns
# Instalar bind9
Ejecutar `en una terminal:`
<pre><code>sudo apt-get install bind9
</code></pre>

# Configurar bind
Hay que editar el fichero `/etc/bind/named.conf.local` y añadir al final de éste:
<pre><code>zone "stucomx.net" {
        type master;
        file "/etc/bind/db.stucomx.net";
        }
<code></pre>

Ahora copiamos el fichero con: 

`cp /etc/bind/db.empty /etc/bind/db.stucomx.net`

Y lo tenemos que editar con:
<pre><code>nano /etc/bind/db.stucomx.net<code></pre>
