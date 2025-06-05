# 📁 **Administrador de discos en Windows**

<br>
En esta sección aprenderemos a utilizar la herramienta gráfica Administrador de discos que viene integrada en Windows. Veremos cómo:

  - 💻 Visualizar discos y particiones existentes

  - 🆕 Crear, formatear y eliminar particiones fácilmente

  - 🔄 Cambiar letras de unidad y gestionar volúmenes

  - 📊 Interpretar la información básica del disco y solucionar problemas comunes

Esta herramienta es ideal para quienes prefieren una interfaz visual en lugar de usar comandos, facilitando la gestión segura de los discos en Windows.

<br>

##
## 📀🧱 PARTICIONANDO DISCOS MBR


1 - Añadimos un disco nuevo y lo inicializamos el el administrador de discos le damos formato MBR

![Inicializando Disco](./img/admin_disk_1.png)


2 - Damos clic derecho en el disco y creamos una nueva partición simple 

![Nueva Partición](./img/admin_disk_2.png)


3 - Damos tamaño a la partición de 2000MB y le damos a siguiente  

![Tamaño de Partición](./img/admin_disk_3.png)

4 - Asignamos una letra y le damos a siguiente . Esto es para identificarla mejor a la hora de alguna búsqueda 

![Asignación de Letra](./img/admin_disk_4.png)


5 - Formateamos la partición con tipo de NTFS y el nombre que le queremos asignar . Marcamos la casilla de ‘dar formato rápido’ esto es para que no tarde en crear la partición y hacemos clic en siguiente 

![Tipo de Formato](./img/admin_disk_5.png)

6 - Como podemos ver la partición se ha creado correctamente en el disco 

![Partición Creada](./img/admin_disk_6.png)


7 - Creamos tres particiones más del mismo tamaño . Ahora  creamos una nueva partición , como podemos ver nos crea una partición extendida y luego la lógica .

Esto pasa porque en un disco MBR no pueden haber mas de 3 particiones primarias 


<br>

⚠️ **Consejo importante:**
> Antes de modificar particiones en discos MBR, asegúrate de hacer una copia de seguridad de tus datos. Recuerda que MBR tiene un límite de 4 particiones primarias, así que planifica bien tu esquema para evitar problemas. ¡Practica en discos de prueba si es posible! 💾🔧