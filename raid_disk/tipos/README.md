# 💽 RAID-0
<br>

**📑 Indice**
- [💽 RAID-0](#-raid-0)
    - [🔧 1.1 Configuración de Discos en VirtualBox](#-11-configuración-de-discos-en-virtualbox)
    - [💽 1.2 Crear RAID-0 (Volumen Distribuido)](#-12-crear-raid-0-volumen-distribuido)

<br>
<br>

### 🔧 1.1 Configuración de Discos en VirtualBox
<br>

💡 En VirtualBox, añade al menos ``2`` discos sin formato desde **“Almacenamiento”** y conéctalos al controlador ``SATA`` antes de iniciar la ``VM`` .

![Nuevos Discos](./img/raid0/virtualbox1.png)
<br>
<br>


### 💽 1.2 Crear RAID-0 (Volumen Distribuido)
<br>

1 - Abre el administrador de discos con ``diskmgmt.msc`` , inicializa los dos discos nuevos como ``mbr`` o ``gpt`` . Dependiendo simpre de tu equipo.

![Inicializar Disco](./img/raid0/raid0.png)
<br>
<br>


2 - Selecciona ``Nuevo volumen distribuido`` para comenzar la creación del ``RAID-0``.

![Nuevo volumen distribuido](./img/raid0/raid1.png)
<br>
<br>



3 - En la ventana que aparece , haz clic en ``siguiente`` para continuar con el asistente.

![Asistente](./img/raid0/raid2.png)
<br>
<br>


4 - Selecciona ``ambos`` discos que quieres incluir en el ``RAID-0`` (mínimo dos discos).

![Seleccionar dos discos](./img/raid0/raid3.png)
<br>
<br>


5 - Asigna una letra de unidad para el nuevo volumen ``(por ejemplo, R:)``.

![Letra de la unidad](./img/raid0/raid4.png)
<br>
<br>


6 - Configura el formato como ``NTFS`` , ponle un nombre al volumen ``(ej. RAID-0)`` , y marca ``Formato rápido`` y opcionalmente ``Habilitar compresión``.

![Formato del disco](./img/raid0/raid5.png)
<br>
<br>


7 - Revisa el resumen de la configuración y haz clic en ``Finalizar``

![Finalizar configuración](./img/raid0/raid6.png)
<br>
<br>


8 - Verifica que el nuevo volumen aparece como un único disco con la letra asignada y el tamaño combinado listo para usar.  

![Verificacion de raid0](./img/raid0/raid7.png)
<br>
<br>


9 - Acepta la ⚠️ advertencia sobre eliminación de datos para crear el volumen.

![Advertencia](./img/raid0/raid8.png)
<br>
<br>


10 - El volumen se ha creado correctamente fijate que los dos tienen el mismo color.

![RAID 0 creado](./img/raid0/raid9.png)

