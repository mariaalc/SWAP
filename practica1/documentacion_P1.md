# Práctica 1
### Presentación de las prácticas y preparación de las herramientas

#### Instalación máquinas virtuales
El primer paso de esta práctica se trata de la instalación de VirtualBox y de 2 máquinas virtuales, con Ubuntu 18.04 y las características especificadas en el guión (disco duro, memoria…). A continuación configuramos ambas máquinas e instalamos SSH (automáticamente en la instalación) y LAMP manualmente, ambos para disponer de acceso remoto y servidor web

#### Conectar ambas máquinas entre ellas
Para ellos creamos dos adaptadores, uno de tipo NAT y el siguiente de tipo solo-anfitrión. Tenemos que hacer algunos cambios del archivo 50-cloud-init.yaml para conectar ambas máquinas, quedando de la siguiente forma.

![Archivo 50-cloud-init.yaml](/home/maria/Escritorio/OTROS/Github/SWAP/practica1/imagenes/archivo.png)

#### Acceder a otra máquina mediante SSH
Para ello tenemos que conocer el IP de cada máquina, con ifconfig lo podemos conocer.

**Máquina 1:** cuya IP es 192.168.56.101
![Máquina1](/home/maria/Escritorio/OTROS/Github/SWAP/practica1/imagenes/maquina1.png)

**Máquina 2:** cuya IP es 192.168.56.102
![Máquina1](/home/maria/Escritorio/OTROS/Github/SWAP/practica1/imagenes/maquina2.png)
