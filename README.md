# Administración de Discos 
Administrar Discos en Windows y Linux 

# DISKPART

Es una herramienta integrada en Windows , donde podemos gestionar discos duros , particiones y volumes desde la
linea de comados .

## 1. Configuración en Virtual Box

1.1 Creamos un nuevo disco de 10GB y lo añadimos a nuestra máquina virtual 

1.2 Iniciamos Windows , vamos al administrador de discos e inicializamos el disco , a formato **MBR** .

## 2. PARTICIONANDO DISCO MBR EN DISKPART

2.1 – Abrimos el terminal (cmd) de Windows y lo ejecutamos como administrador.

Una vez dentro entramos a diskpart una herramienta de Windows para administrar nuestros discos y ejecutamos el siguiente comando 

~~~~~~~~
diskpart
~~~~~~~~

2.2 – Primero mostramos los discos con el comando **‘list’** , aquí podemos ver que tenemos dos discos Disco0 y Disco1 .

2.3 - Para seleccionar un disco utilizamos el comando **‘select’** y el número del disco , sabes que esta seleccionando es que tiene el **(*)** al principio

2.4 - Para crear una partición primaria se usa create y el tipo de partición con el tamaño que deseas 
~~~~~~~~
 create partition primary size=2000
~~~~~~~~

2.5 - Creamos 3 particiones igual , tenemos que tener 4 particiones primarias y un espacio libre 

2.6 - Ahora intentamos crear otra partición primaria , como puedes ver no se puede .

2.7 -  Para solucionar el problema borramos la ultima partición creada con el comando **‘delete’** y como puedes ver en vez de formar dos particiones forma una sola que aumenta el espacio.

2.8 – Creamos una partición extendida con el espacio que queda , utilizando el comando **‘extend’** en ves de **‘primary’** así como se ve en la imagen .

**‘Las particiones extendidas tienen dentro particiones lógicas , por eso dice que hay un espacio libre , aunque hay una partición creada . Cuando se crean las lógicas se llena la extendida’**


2.9 – Luego creamos dos particiones lógicas con el comando **“logical”** y como podemos ver se ha creado correctamente las particiones .

2.10 – Mostramos todas las particiones como podemos ver se han creado correctamente todos las particiones

