<h1 align="center"> ESQUEMA DE RED </h1>  
<BR>
<BR>
<p align="center">
  <img src="./img/red.png" alt="Red" width="700">
</p>

## DESCRIPCIÓN DEL ESQUEMA  
El servidor está configurado con dos tarjetas de red:  
- La primera (enp0s3) en adaptador puente.
- La segunda (enp0s8) en red interna.
<p align="center">
  <img src="./img/virtual.png" alt="Virtual" width="700">
</p>
<br>

## CONFIGURACIÓN DE LAS REDES  
Para la configuración de las redes hay que modificar el archivo
>/etc/netplan/01-network-manager-all.yaml  
- La enp0s3 estará en DHCP.  
- La enp0s8 será IP estática.
 <br>
<p align="center">
  <img src="./img/lamine-yamal.png" alt="Red" width="600">
</p>
<br>
Una vez hecha la configuración debemos ejecutar el siguiente comando
<br>
<br>

>netplan apply

<p align="center">
  <img src="./img/netplanapply.png" alt="Red" width="600">
</p>

<br>


