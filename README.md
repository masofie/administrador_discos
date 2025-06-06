# 💽 ADMINISTRACIÓN DE DISCOS (Windows y Linux)
<br>

Aprende a gestionar discos en sistemas *Windows* y *Linux*. En esta guía veremos cómo crear, borrar y formatear particiones en discos duros, comprendiendo su funcionamiento básico y las diferencias entre ambos sistemas operativos.
 
📌 **MBR (Master Boot Record)**

- **Límites de partición:**
  - *Máximo de 4 particiones primarias*
  - *3 primarias + 1 extendida (donde puedes crear varias particiones lógicas)*

- **Características:**
  - ✅ *Compatibilidad con sistemas antiguos*  
  - ❌ *Límite de tamaño por partición: 2TB*


📌 **GPT (GUID Partition Table**

- **Límites de partición:**
  - *Hasta 128 particiones primarias*
  - *No requiere particiones extendidas ni lógicas*

- **Características:**
  - ✅ *Soporte para discos de más de 2TB*  
  - ✅ *Más moderno y seguro*  
  - ❌ *Requiere *UEFI* para arrancar en algunos sistemas*


<br>

📚 *Este material forma parte de una serie de guías técnicas.*

*Si te fue útil, no olvides revisar los próximos temas que estaré subiendo ✌️*  
*¡Gracias por tu apoyo! Y recuerda dejar tu ⭐ si te gustó este contenido.*



<br>
📂 Contenido

- [Administrador de Discos en Windows](./admin_disk_windows/README.md)
- [Diskpart (cmd)](./diskpart_cmd/README.md)
- [Admistrador de Discos en Linux/Ubuntu](./admin_disk_linux/README.md)
- [Terminal de Linux/Ubuntu](./cmd.unix/README.md)
