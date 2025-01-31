<h1 align="center"> CASOS PRÁCTICOS </h1>  
<BR>
<BR>

## ENUNCIADO  
Acabamos de terminar el CFGS ASIR y encuentramos trabajo en la empresa Servicios Web RC, SA en Huelva. Anteriormente utilzaban Apache como servidor web y quiere migrar a `Nginx`. Una vez instalado y configurado procedemos a realizar todos los casos prácticos solicitados.  
<br>
<br>

### 1) VERSIÓN DE NGINX QUE USAMOS 
Para ver la versión de Nginx hay que ejecutar en un terminal el siguiente comando
>nginx -v
<br>

![Version](./img/versionnginx.png)

### 2) COMPROBAR SERVICIO
Para ver si nuestro servicio esta en ejecución debemos usar le siguiente comando
>systemctl status nginx
<br>

![Servicio](./img/servicionginx.png)

### 3) FICHEROS DE CONFIGURACIÓN
El directorio donde podmeos encontrar el fichero de nginx esta situado en 
> /etc/nginx
<br>

![conf](./img/ficherosconfig.png)

El archivo de configuración de nginx es 
>nginx.conf
<br>

![Conf2](./img/nginx.conf.png)

### 4) CAMBIAR HTML DE LA PAGINA WEB PRINCIPAL
Para ello debemos modificar el archivo
>/var/www/html/index.nginx-debian.html
<br>

![Html](./img/html.png)

### 5) VIRTUAL HOSTING
Crearemos dos sitios webs llamados `web1` y `web2`
- Debemos crear primero los directorios
<br>

![Mkdir](./img/mkdir.png)

- Conceder permisos
<br>

![Permisos](./img/permisos.png)

- Crear `index.html` de `web1` y `web2`
<br>

![Index](./img/indexweb1.png)
![Index](./img/indexweb2.png)

- Creación de los `sites-available` para cada web
<br>

![Sites](./img/availableweb1.png)
![Sites](./img/availableweb2.png)

- Configuración del archivo hosts para las webs
<br>

![hosts](./img/hosts.png)

- Verificación de entrada en las webs
<br>

![Mozilla](./img/mozillaweb1.png)
![Mozilla](./img/mozillaweb2.png)

### 6) AUTENTICACIÓN, AUTORIZACIÓN Y CONTROL DE ACCESO
Mientras que la `web1` puede acceder por la red externa como por la interna, la `web2` solo puede por la interna, arreglemos esto con unos sencillos pasos

- Modificar los `sites-available` de cada web
<br>

![Sites2](./img/modificaravailableweb1.png)
![Sites2](./img/modificaravailableweb2.png)
<br>

- Modificar el archivo `hosts` con las ips de ambas web
<br>

![MHosts](./img/modificarhosts.png)

- Comprobemos la red interna usando el comando
>curl
<br>

![Curl](./img/curlweb1.png)  
![Curl](./img/curlweb2.png)

- Comprobemos ahora la red
<br>

![Comprobar](./img/mozillaweb1.png) 
![Comprobar](./img/comprobar.png)

### 7) AUTENTICACIÓN, AUTORIZACIÓN Y CONTROL DE ACCESO
Vamos a restringir Web1.org de tal forma que solo puedan acceder a la web usuarios con su contraseña

- Creamos el `usuario1` con su respectiva contraseña para poder entrar en la `web1`
- Modificaremos el archivo `sites-available`
<br>

![Privado](./img/privadoavailableweb1.png)

- Verificamos que web1 ahora es privado y solo podemos acceder a el mediante el `usuario1` que hemos creado antes y su contraseña
<br>

![Verificar](./img/usuario1.png)
![Entrada](./img/acceso.png)

### 8) AUTENTICACIÓN, AUTORIZACIÓN Y CONTROL DE ACCESO
La web1 contiene un directorio creado llamado `privada` donde la red externa pide autorización y desde la red interna no.

- Debemos volver a modificar el archivo `sites-available`
<br>

![Permitir](./img/permitiracceso.png)

### 9) SEGURIDAD
Configuremos `web1` para que el acceso sea seguro, para ello debemos crear una `key` privada mediante el siguiente comando

>openssl req -x509 -nodes -days 365 -newkey rsa:2048 -keyout /etc/ssl/private/selfigned.key -out /etc/ssl/certs/selfsigned.crt
<br>

![Key1](./img/key1.png)
![Key2](./img/key2.png)

- Para acabar debemos volver a modificar el archivo `sites-available`
<br>

![Ultima](./img/ultima.png)





