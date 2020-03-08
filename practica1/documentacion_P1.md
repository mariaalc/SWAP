# Práctica 1
## Presentación de las prácticas y preparación de las herramientas

#### Instalación máquinas virtuales
El primer paso de esta práctica se trata de la instalación de VirtualBox y de 2 máquinas virtuales, con Ubuntu Server y las características especificadas en el guión (disco duro, memoria…). A continuación configuramos ambas máquinas e instalamos SSH (automáticamente en la instalación) y LAMP (Linux Apache, MySQL, PHP) manualmente, ambos para disponer de acceso remoto y servidor web.

#### Conectar ambas máquinas entre ellas
Para comunicar las máquinas entre un mismo anfitrión y entre ellaas, creamos dos adaptadores, uno de tipo NAT y el siguiente de tipo solo-anfitrión, para crear una red local entre las máquinas virtuales y el antfitrión. Para ello, tenemos que hacer algunos cambios del archivo 50-cloud-init.yaml, quedando este de la siguiente forma.

![Archivo 50-cloud-init.yaml](https://raw.githubusercontent.com/mariaalc/SWAP/master/practica1/imagenes/archivo.png)

#### Acceder a otra máquina mediante SSH
En primer lugar tenemos que conocer el IP de cada máquina, con ifconfig lo podemos saber, en mi caso, es:

**Máquina 1:** IP es 192.168.56.101
![Máquina1](https://raw.githubusercontent.com/mariaalc/SWAP/master/practica1/imagenes/maquina1.png)

**Máquina 2:** IP es 192.168.56.102
![Máquina2](https://raw.githubusercontent.com/mariaalc/SWAP/master/practica1/imagenes/maquina2.png)

Accedemos de una máquina a otra de la siguiente forma: ssh root@IPserver
**Acceso desde máquina1 a máquina2** 
![m1_a_m2](https://raw.githubusercontent.com/mariaalc/SWAP/master/practica1/imagenes/m1_conectada_a_m2.png)
**Acceso desde máquina2 a máquina1** 
![m2_a_m1](https://raw.githubusercontent.com/mariaalc/SWAP/master/practica1/imagenes/m2_conectada_a_m1.png)

#### Acceder de una máquina a otra mediante la herramienta curl
cURL es una librería de funciones para conectar con servidores para trabajar con ellos. El trabajo se realiza con formato URL, es decir, sirve para realizar acciones sobre archivos que hay en URLs de Internet, para ello creamos en cada máquina un archivo HTML y vamos a acceder a este entre máquinas.
Accedemos de una máquina a otra con curl de la siguiente forma: curl http://direccionIPserver/ejemplo.html://
**Acceso desde máquina1 a máquina2 con cURL** 
![m1_a_m2](https://raw.githubusercontent.com/mariaalc/SWAP/master/practica1/imagenes/m1_a_m2_curl.png)
**Acceso desde máquina1 a máquina2 con cURL** 
![m1_a_m2](https://raw.githubusercontent.com/mariaalc/SWAP/master/practica1/imagenes/m2_a_m1_curl.png)



