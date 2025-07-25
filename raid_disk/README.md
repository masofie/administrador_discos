# 💽 RAID en Windows 
<br>

**📑 Indice**
- [💽 RAID en Windows](#-raid-en-windows)
  - [🛡️ ¿Qué es ``RAID``?](#️-qué-es-raid)
  - [🧱 Tipos de ``RAID`` Explicados](#-tipos-de-raid-explicados)
  - [🖥️ 1. Windows Server](#️-1-windows-server)
    - [🔘 1.1 Tipos de ``RAID`` :](#-11-tipos-de-raid-)
  - [💻 2. Windows Cliente (Windows 10/11)](#-2-windows-cliente-windows-1011)

<br>

## 🛡️ ¿Qué es ``RAID``?
<br>

🛡️ **¿Qué es RAID?**

``RAID (Redundant Array of Independent Disks)`` es una tecnología que combina múltiples discos duros en una sola unidad lógica con el fin de :

- 💨 Mejorar el rendimiento de lectura/escritura.
- 🔐 Aumentar la disponibilidad y seguridad de los datos.
- 🧱 Incrementar la tolerancia a fallos en sistemas críticos.
<br> <br>


## 🧱 Tipos de ``RAID`` Explicados
<br>

| Nivel RAID | ¿Cómo funciona? 📚                                                                 | Ventajas ✅                              | Desventajas ⚠️                         |
|------------|-------------------------------------------------------------------------------------|------------------------------------------|-----------------------------------------|
| **RAID 0** | Divide los datos entre dos o más discos (striping). Sin redundancia.               | Máximo rendimiento ⚡                     | Si un disco falla, se pierde todo ❌     |
| **RAID 1** | Copia exacta de los datos en dos discos (mirroring).                               | Alta seguridad 🛡️                        | Solo se usa el 50% del total del espacio 💾 |
| **RAID 5** | Datos + paridad distribuidos en 3 o más discos.                                    | Buen balance entre rendimiento y seguridad 🔁 | Más lento en escrituras y recuperación ⚠️ |
| **RAID 10**| Combina RAID 1 (espejo) y RAID 0 (rendimiento). Requiere mínimo 4 discos.          | Redundancia + velocidad 💪               | Coste elevado en hardware 💰             |

<br> <br>

## 🖥️ 1. Windows Server
<br>

**✅ Recomendado para ``RAID ``:**

- Soporta RAID por software desde el Administrador de discos o Storage Spaces.
- Permite gestionar RAID por hardware si el servidor cuenta con controlador RAID.
- Soporta varios niveles RAID (0, 1, 5, 10, etc.).
- Ideal para entornos profesionales o empresariales.

<br><br>


### 🔘 1.1 Tipos de ``RAID`` :
<br>

> - Como crearlos? 
>   - [⚡ RAID-0 (Striping)](./tipos/RAID0.md)
>   - [🛡️ RAID-1 (Mirroring)](./tipos/RAID-1.md)
>   - [🔄 RAID-5 (Paridad distribuida)](./tipos/RAID-5.md)
>

<br> <br>



## 💻 2. Windows Cliente (Windows 10/11)

🔧 *Limitado, pero posible :*

- Permite configurar RAID básicos con Espacios de almacenamiento (Storage Spaces).
- Puedes crear configuraciones similares a RAID 0, 1 o Mirror, pero con menor fiabilidad y sin tantas opciones avanzadas.
- No es adecuado para producción crítica.

<br> <br>

💡 Recomendación:

>Para ``RAID`` serio y confiable, lo mejor es usar Windows Server o bien un sistema Linux especializado.
>Si es solo para pruebas o uso doméstico , **Windows 10/11** con Storage Spaces puede servir.
