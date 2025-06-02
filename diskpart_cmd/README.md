# DISKPART
Es una herramienta integrada en Windows , donde podemos gestionar discos duros , particiones y volumes desde la
linea de comados .
<br>

**Funcionamiento**
<br>

- **Accder a Diskpart**

En el menú de busqueda podemos o símbolo de sistemas abrimos la herramienta .

- **Comandos Principales :**

    - *list disk* (listar discos / mostrar discos)
    - *select disck* (seleccionar disco)

- **Tareas :**

    Comandos para crear el tipo de particiones 

    - *create partition primary* (primaria)
    - *create partition extend* (extendida)
    - *create partition logical* (lógica)

    Borrar particiones y vaciar disco duro 

    - *delete partition* (eliminar partición)
    - *celan disk (number)* (vaciar disco completo)

    Especificaciones de las particiones y discos

    - *formart* (formatear partición)
    - *assign letter=X* (asignar leta)
    - *covert gpt* (convertir disco a GPT)



#



## 1. CONFIGURACIÓN DEL VIRTUAL BOX

1.1 Creamos un nuevo disco de 10GB y lo añadimos a nuestra máquina virtual 

![Añadiendo Disco Duro](./img_diskpart/virtualbox1.png)


1.2 Iniciamos Windows , vamos al administrador de discos e inicializamos el disco , a formato **MBR** .

![Inicializando Disco Duro](./img_diskpart/virtualbox2.png)

## 2. PARTICIONANDO DISCO *"MBR"* EN DISKPART

2.1 – Abrimos el terminal (cmd) de Windows y lo ejecutamos como administrador.

![Iniciando Diskpart](./img_diskpart/diskpart_1.png)

Una vez dentro entramos a diskpart una herramienta de Windows para administrar nuestros discos y ejecutamos el siguiente comando 

~~~~~~~~
diskpart
~~~~~~~~

![Listar Discos](./img_diskpart/diskpart_2.png)

2.2 – Primero mostramos los discos con el comando **‘list’** , aquí podemos ver que tenemos dos discos Disco0 y Disco1 .


![Listar Discos](./img_diskpart/diskpart_3.png)

2.3 - Para seleccionar un disco utilizamos el comando **‘select’** y el número del disco , sabes que esta seleccionando es que tiene el **(*)** al principio

![Seleccionamos Disco](./img_diskpart/diskpart_3.png)

2.4 - Para crear una partición primaria se usa create y el tipo de partición con el tamaño que deseas 
~~~~~~~~
 create partition primary size=2000
~~~~~~~~

![Crear Particion Primaria](./img_diskpart/diskpart_4.png)

2.5 - Creamos 3 particiones igual , tenemos que tener 4 particiones primarias y un espacio libre 

![Crear tres Particiones](./img_diskpart/diskpart_5.png)

2.6 - Ahora intentamos crear otra partición primaria , como puedes ver no se puede .

![Intentamos crear la particion 5](./img_diskpart/diskpart_6.png)

2.7 -  Para solucionar el problema borramos la ultima partición creada con el comando **‘delete’** y como puedes ver en vez de formar dos particiones forma una sola que aumenta el espacio.

![Eliminamos particion](./img_diskpart/diskpart_7.png)

2.8 – Creamos una partición extendida con el espacio que queda , utilizando el comando **‘extend’** en ves de **‘primary’** así como se ve en la imagen .

![Crear nueva particion extendida](./img_diskpart/diskpart_8.png)

**‘Las particiones extendidas tienen dentro particiones lógicas , por eso dice que hay un espacio libre , aunque hay una partición creada . Cuando se crean las lógicas se llena la extendida’**


2.9 – Luego creamos dos particiones lógicas con el comando **“logical”** y como podemos ver se ha creado correctamente las particiones .

![Crear nuevas particiones logicas](./img_diskpart/diskpart_9.png)

2.10 – Mostramos todas las particiones como podemos ver se han creado correctamente todos las particiones

![Mostrado resultado complero de disco mbr](./img_diskpart/diskpart_10.png)

