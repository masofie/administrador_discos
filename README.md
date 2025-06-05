# 💽 ADMINISTRACIÓN DE DISCOS (Windows y Linux)
<br>

Aprende a gestionar discos en sistemas *Windows* y *Linux*. En esta guía veremos cómo crear, borrar y formatear particiones en discos duros, comprendiendo su funcionamiento básico y las diferencias entre ambos sistemas operativos.
 

<br>

:pushpin: **MBR (Master Boot Record)**

- **Limite de Particiones :**
  - *Máximo 4 particiones primarias*
  - *O 3 particiones primarias y una extendida* 
      
- **Partición Extendida** 

   - *Se crea para poder tener más de 4 particiones*
   - *Dentro de la extendida puedes tener particiones lógicas (varias)*
 
   - :white_check_mark:*Compatibles con sistemas más antiguos*
   - :x:*Límite de tamaño por partición: 2TB*


:pushpin: **GPT (GUID Partition Table)**

- **Límite de Particiones :**

   - *Hasta 128 particiones primarias (no se necesitan ni extendidas ni lógicas )*
   - *No usa particiones extendidas ni lógicas*
   - *Cada partición es primaria* 

   - :white_check_mark: *Soporta discos grandes (más de 2TB)*
   - :white_check_mark:*Más seguro y moderno* 
   - :x: *Requiere **UEFI** para arrancar algunos sistemas*  

<br>

  Este material forma parte de una serie de guías 📃 técnicas . <br> 
  Si te sirvio no olvides checar los proximos temas que estaré subiendo ✌️. <br> 
  Gracias por tu apoyo , recurda dejar tu ⭐

<br>

Contenido 
- [Administrador de Discos en Windows](./disk_w/README.md)
- [Diskpart (cmd)](./diskpart_cmd/README.md)
- [Admistrador de Discos en Windows](./disk_unix/README.md)
- [Terminal de Linux/Ubuntu](./cmd.unix/README.md)
