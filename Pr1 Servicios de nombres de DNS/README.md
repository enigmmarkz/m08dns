# m08dns
## Enunciado
Configura un dominio "stucomx.net" que contenga los siguientes registros (unicamente se especifica la parte del nombre delante del dominio):

server = 192.168.1.1\
www = server\
ns = server\
printer = 192.168.1.200\
pc42 = 192.168.1.42\
pc43 = 192.168.1.43\
pc44 = 192.168.1.44\
pc45 = 192.168.1.45\
...\
pc50 = 192.168.1.50\
Crea un repositorio de GitHub que inlcuya una wiki con explicaciones sobre los pasos para conseguir esta configuración (comandos de consola a ejecutar, ficheros modificados...) y que incluya copia de esos ficheros.

Haz el repositorio privado. Incluye a @pablo-molins como cuenta con permisos de lectura. Como entrega, sube la URL de tu repositorio en GitHub.

# Instalar bind9
Ejecutar `en una terminal:`
<pre><code>sudo apt-get install bind9
sudo apt-get install dnsutils
</code></pre>

# Configurar bind
Hay que editar el fichero `/etc/bind/named.conf.local` y añadir al final de éste:
<pre><code>zone "stucomx.net" {
        type master;
        file "/etc/bind/db.stucomx.net";
        }
</code></pre>

Ahora copiamos el fichero con: 

`cp /etc/bind/db.empty /etc/bind/db.stucomx.net`

Y lo tenemos que editar con:
<pre><code>nano /etc/bind/db.stucomx.net</code></pre>
