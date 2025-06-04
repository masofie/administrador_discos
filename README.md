# ADMINISTRACIÓN DE DISCOS 
<br>

Administrar Discos en Windows y Linux . En este tema vamos a preder a gestionar , crear , borrar particiones en los fiscos duros 
dandole formato a cada una de ellas y entendido muy bien su funcionamiento básico tanto en **Linux** como en **Windows**. 

<br>

**MBR (Master Boot Record)**

- **Limite de Particiones :**
  - *Máximo 4 particiones primarias*
  - *O 3 particiones primarias y una extendida* 
      
- **Partición Extendida** 

   - *Se crea para poder tener más de 4 particiones*
   - *Dentro de la extendida puedes tener particiones lógicas (varias)*
 
   - :white_check_mark:*Compatibles con sistemas más antiguos*
   - :x:*Requiere*Límite de tamaño por partición:2TB*


**GPT (GUID Partition Table)**

- **Límite de Particiones :**

   - *Hasta 128 particiones primarias (no se necesitan ni extendidas ni lógicas )*

   - *No usa particiones extendidas ni lógicas*

   - *Cada partición es primaria* 

   - :white_check_mark: *Soporta discos grandes (más de 2TB)*
   - :white_check_mark:*Más seguro y moderno* 
   - :x:*Requiere **UEFI** para arrancar algunos sistemas*  

<br>

Espero que esto te sirva de guia para tus proyectos :+1: . Recuerda seguirme , para subir más contenido :ok_hand:

<br>

Contenido 
- [Administrador de Discos en Windows](./disk_w/README.md)
- [Diskpart (cmd)](./diskpart_cmd/README.md)
- [Admistrador de Discos en Windows](./disk_unix/README.md)
- [Terminal de Linux/Ubuntu](./cmd.unix/README.md)
