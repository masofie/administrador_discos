# 🐧💽 **Administrador de Discos en Linux/Ubuntu**
<br>

En esta sección veremos cómo utilizar la herramienta gráfica Discos (gnome-disks) incluida en la mayoría de entornos de escritorio en Linux/Ubuntu.
Aprenderemos a:

  - 🖱️ Ver información detallada de discos y particiones

  - ➕ Crear y formatear nuevas particiones
  - 🗑️ Eliminar o modificar particiones existentes

  - 🔄 Montar, desmontar y cambiar opciones de arranque

Esta herramienta es ideal para quienes prefieren una interfaz visual sencilla, pero poderosa, para gestionar sus discos en Linux.

<br>

## 1. Gestor de Discos (GPARTED)
<br>


Descargamos el gestor desde la la página oficial de Linux , usando el siguiente enlaces te lleva a esta ventana ,a ahí puedes descargar el paquete o solo copiar el comando en el terminal y descargarlo . Nosotros utilizaremos el comando 

~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
https://gparted.org/download.php
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

![Enlace de Download](./img_gparted/1_enlace_dowload.png)


En el terminal ejecutamos el comando y dejamos que se descargue nuestro gestor . Como se muestra en la imagen 


~~~~~~~~~~~~~~~~~~~~~~~~~~~~
sudo apt-get install gparted
~~~~~~~~~~~~~~~~~~~~~~~~~~~~

![Desde el cmd Download](./img_gparted/2_cmd_dowload.png)


Después buscamos nuestro disco en el terminal y eliminamos todo con el siguiente comando , esto para que nos quede libre . Ten encuentra que esto solo son pruebas y este disco es secundario .

~~~~~~~~~~~~~~~~~~~~~~~
sudo wipefs -a /dev/sdb
~~~~~~~~~~~~~~~~~~~~~~~

![Desde el cmd delete](./img_gparted/3_cmd_delete.png)


## 2. Inicializando Disco
<br>


Entramos en Gparted y seleccionamos el disco nuevo y creamos una nueva partición . Con clic derecho a **“NUEVA”** , así como en la imagen .


![Error al Inicializar 1](./img_gparted/4_inicializando_disco_error.png)


Como podemos ver no nos deja , *¿por qué?* . Esto pasa porque no elegimos la tabla de particiones en en el disco , esto viene siendo **“INICIALIZAR EL DISCO EN WINDOWS”** , aquí se le conoce como tabla de particiones .


![Error al Inicializar 2 ](./img_gparted/5_inicializando_disco_error.png)


Nos fijamos en el error y hacemos lo que nos dice ir a , **“DISPOSITIVO”** **→ “CREAR TABLA DE PARTICIONES”** . 

![Correcto inicalizacion 1 ](./img_gparted/6_inicializando_disco_correct.png)


Nos da distintos tipos pero vamos ha escoger **“GPT”** y aplicamos los cambios de la siguiente manera 

![Correcto inicalizacion 2 ](./img_gparted/7_inicializando_disco_correct.png)




🧠 **Consejo Final:**

> Aunque la herramienta gráfica Discos es muy intuitiva, haz siempre una copia de seguridad antes de modificar particiones. 💾
>  - 🔐 Algunas funciones requieren privilegios de administrador (te pedirá tu contraseña).
>  - ⚠️ Verifica bien el disco o partición antes de borrar o formatear.
>  - 🧪 Practica en un disco externo o máquina virtual si estás empezando.
> ¡Una buena gestión de discos mantiene tu sistema limpio y funcionando al 100%! 🐧🚀 

