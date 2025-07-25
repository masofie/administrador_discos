# 💽 🧩 RAID-5 – Crear Volumen con Paridad Distribuida
<br>

**📑 Indice**
- [💽 🧩 RAID-5 – Crear Volumen con Paridad Distribuida](#--raid-5--crear-volumen-con-paridad-distribuida)
  - [📋 Pasos para configurar ``RAID-5``](#-pasos-para-configurar-raid-5)

<br>

## 📋 Pasos para configurar ``RAID-5``
<br>

1️⃣ Añadimos un nuevo disco al equipo para alcanzar un mínimo de ``3`` discos, requisito esencial para ``RAID-5``.

![Nuevo disco en Virtualbox](./img/raid5/raid1.png)
<br> <br>


2️⃣ Abrimos el administrador de discos e ``inicializamos`` los discos nuevos si aún no lo están.

![Inicializar nuevo disco](./img/raid5/raid2.png)
<br> <br>


3️⃣ Hacemos clic derecho sobre uno de los discos y seleccionamos ``nuevo volumen`` ``RAID-5``.

![Selecionar raid-5](./img/raid5/raid3.png)
<br> <br>


4️⃣ Se abre el asistente de configuración , avanzamos haciendo clic en ``siguiente``.

![Abrir asistente](./img/raid5/raid4.png)
<br> <br>


5️⃣ Por defecto se selecciona el primer disco ,  añadimos los otros ``dos`` para completar el conjunto ``RAID``.

![Selección de discos](./img/raid5/raid5.png)
<br> <br>


6️⃣ Una vez seleccionados los tres discos , hacemos clic en ``siguiente`` para continuar.

![Seguir con la configuración](./img/raid5/raid6.png)
<br> <br>


7️⃣ Asignamos un ``nombre`` , una ``letra`` de unidad , elegimos formato ``NTFS`` y activamos la ``compresión`` si lo deseamos.

![Formato del raid-5](./img/raid5/raid7.png)
<br> <br>


8️⃣ Revisamos el resumen final para confirmar que todo esté correcto y pulsamos ``finalizar``.

![Revisar configuración](./img/raid5/raid8.png)
<br> <br>


9️⃣ Aparecerá una ⚠️ ``advertencia`` sobre la conversión de los discos a dinámicos; aceptamos para proceder.

![Advertencia de creación](./img/raid5/raid9.png)
<br> <br>


🔟 ¡``RAID-5`` creado con éxito ✅! El volumen aparecerá como una unidad única con paridad distribuida para tolerancia a fallos.

![Raid-5 creado correctamente](./img/raid5/raid10.png)
<br> <br>


**📌 Final del apartado RAID 5**

``RAID-5`` combina rendimiento y seguridad, distribuyendo los datos junto con la información de paridad.
- 🔁 Si un disco falla, el sistema puede reconstruir los datos sin perder información.
- ⚠️ Requiere mínimo tres discos y puede ser más lento en operaciones de escritura y recuperación.