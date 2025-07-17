# 💽📟🛠️ Intérprete de Comandos DISKPART
<br>

**📑 Indice**
- [💽📟🛠️ Intérprete de Comandos DISKPART](#️-intérprete-de-comandos-diskpart)
  - [1. Configuración del Virtual-Box](#1-configuración-del-virtual-box)
  - [2. Particionando Disco *``mbr``* con DISKPART](#2-particionando-disco-mbr-con-diskpart)

<br>

*``DISKPART``* es una herramienta integrada en Windows que se utiliza desde la línea de comandos. Permite administrar discos duros, memorias *``USB``* y otras unidades de almacenamiento.
Con *``diskpart``* puedes crear, eliminar o modificar particiones (las divisiones internas de un disco).

⚠️ ¡Importante! Hay que tener mucho cuidado al usarla, ya que un mal comando puede borrar toda la información de un disco.

<br>

⚙️ **Funcionamiento de `diskpart`**
<br>

- 🧭 **Acceder a `diskpart`**

Puedes abrir *``diskpart``* desde el menú de búsqueda de *Windows*.  Escribe **"Símbolo del sistema"** o **"cmd"**, haz clic derecho y selecciona **"Ejecutar como administrador"**.  Luego, escribe diskpart y presiona *Enter* para iniciar la herramienta.


- 💡 **Comandos Principales :**

  ~~~
  list disk           # Listar todos los discos disponibles
  select disk X       # Seleccionar disco (reemplaza X por el número del disco)

  list partition      # Mostrar particiones del disco seleccionado
  select partition X  # Seleccionar partición

  list volume         # Mostrar volúmenes
  select volume X     # Seleccionar volumen
  ~~~

- 🛠️ **Tareas Comunes**

  - 🪚 Crear Particiones
  
  ~~~
  create partition primary     # Crear partición primaria
  create partition extended    # Crear partición extendida
  create partition logical     # Crear partición lógica
  ~~~
  

  - 🧹 Eliminar y limpiar

  ~~~
  delete partition           # Eliminar la partición seleccionada
  clean                      # Borrar todo el contenido del disco seleccionado
  clean all                  # Borrado completo (más profundo)
  ~~~

  - ⚙️ Configurar particiones/discos
    
  ~~~
  format fs=ntfs quick         # Formatear partición como NTFS (rápido)
  format fs=fat32 quick        # Formatear como FAT32 (rápido)
  assign letter=X              # Asignar letra de unidad (reemplaza X)
  label=Nombre                 # Establecer nombre de la partición
  convert gpt                  # Convertir disco a GPT
  detail disk                  # Ver información detallada del disco
  ~~~
  <br>
  <br>

## 1. Configuración del Virtual-Box

1.1 Creamos un nuevo disco de *``10GB``* y lo añadimos a nuestra máquina virtual 

![Añadiendo Disco Duro](./img_diskpart/virtualbox1.png)
<br>
<br>


1.2 Iniciamos Windows , vamos al administrador de discos e inicializamos el disco , a formato *``MBR``* . Esto te lo muestra desde que entras en la herramienta .

![Inicializando Disco Duro](./img_diskpart/virtualbox2.png)
<br>
<br>

## 2. Particionando Disco *``mbr``* con DISKPART

2.1 – Entramos en el terminal *``(cmd)``* y lo ejecutamos como administrador.

![Iniciando Diskpart](./img_diskpart/diskpart_1.png)
<br>
<br>

Una vez dentro entramos a *``diskpart``* una herramienta de Windows para administrar nuestros discos y ejecutamos el siguiente comando 

~~~~~~~~
diskpart
~~~~~~~~

![Listar Discos](./img_diskpart/diskpart_2.png)
<br>
<br>

2.2 – Primero mostramos los discos con el comando *``list``* , aquí podemos ver que tenemos dos discos *``Disco0``* y *``Disco1``* .


![Listar Discos](./img_diskpart/diskpart_3.png)
<br>
<br>

2.3 - Para seleccionar un disco utilizamos el comando *``select``* y el número del disco , sabes que esta seleccionando es que tiene el *``(*)``* al principio

![Seleccionamos Disco](./img_diskpart/diskpart_3.png)
<br>
<br>

2.4 - Para crear una partición primaria se usa create y el tipo de partición con el tamaño que deseas 
~~~~~~~~
 create partition primary size=2000
~~~~~~~~

![Crear Particion Primaria](./img_diskpart/diskpart_4.png)
<br>
<br>

2.5 - Creamos *``3``* particiones igual , tenemos que tener *``4``* particiones primarias y un espacio libre 

![Crear tres Particiones](./img_diskpart/diskpart_5.png)
<br>
<br>

2.6 - Ahora intentamos crear otra partición primaria , como puedes ver no se puede .

![Intentamos crear la particion 5](./img_diskpart/diskpart_6.png)
<br>
<br>


2.7 -  Para solucionar el problema borramos la ultima partición creada con el comando *``delete``* y como puedes ver en vez de formar dos particiones forma una sola que aumenta el espacio.

![Eliminamos particion](./img_diskpart/diskpart_7.png)
<br>
<br>


2.8 – Creamos una partición extendida con el espacio que queda , utilizando el comando *``extend``* en ves de *``primary``* así como se ve en la imagen .

![Crear nueva particion extendida](./img_diskpart/diskpart_8.png)
<br>
<br>


*``Las particiones extendidas tienen dentro particiones lógicas , por eso dice que hay un espacio libre , aunque hay una partición creada . Cuando se crean las lógicas se llena la extendida``*

<br>
<br>

2.9 – Luego creamos dos particiones lógicas con el comando *``logical``* y como podemos ver se ha creado correctamente las particiones .

![Crear nuevas particiones logicas](./img_diskpart/diskpart_9.png)
<br>
<br>


2.10 – Mostramos todas las particiones como podemos ver se han creado correctamente todos las particiones

![Mostrado resultado complero de disco mbr](./img_diskpart/diskpart_10.png)
<br>
<br>


2.11 -  También para añadirle una letra a una partición podemos ejecutar el comando *``'assign letter=X'``* , para identificar la unidad

![Añadiendo letra a la partición](./img_diskpart/diskpart_11.png)
<br>
<br>


Para que se vea en el terminal podemos ejecutar el comando *``volume``* ahí se muestra todas las particiones de todos los discos , y ademas las demás características 

![Añadiendo letra a la partición 2](./img_diskpart/diskpart_12.png)
<br>
<br>



2.12 - Si queremos darle nombre la partición utilizamos el comando *``format``* y el tipo de formato que queremos . Si añadimos *``quick``* es para dar formato rápido 

![Formato de una partición](./img_diskpart/diskpart_13.png)
<br>
<br>


2.13 Para ver la información completa de un disco utilizamos el comando *``detail``* y ahí podemos ver toda la infomación 

![Información del disco](./img_diskpart/diskpart_14.png)
<br>
<br>


2.14 Para dejar el disco limpio como en el principio usamos *``clean all``* así como se muestra en aquí debajo 

![Lipiar Disco](./img_diskpart/diskpart_15.png)
<br>
<br>

> **¡Último consejo!** 🤓  
> 🔐 Ejecuta `diskpart` como *``Administrador``* para evitar restricciones de permisos.  
> ⚠️ Verifica siempre el *``número de disco``* antes de aplicar cambios irreversibles.  
> 💻 Practica en una *``VM``* y repite los comandos para ganar confianza. 💪
