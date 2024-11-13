author: Álvaro Caro Fernández
summary: Incident Investigation
id: Proyecto 2.1
categories: codelab,markdown
environments: Web
status: Publicado

## Introducción
En este proyecto, como miembros del equipo de respuesta a incidentes (CSIRT) de la empresa, se nos ha asignaod la investigación de un incidente de seguridad que ha comprometido una de las máquinas del departamento de IT. La tarea consistirá en aplicar la metodología de análisis forense para recopilar, almacenar y analizar evidencias de forma que se conserve su integridad y se mantenga una trazabilidad completa del proceso. La finalidad es proporcionar un informe técnico detallado sobre las conclusiones del análisis, que sirva tanto para la resolución del incidente como para la mejora continua de las medidas de seguridad de la organización.

Cada evidencia estará dividida en diferentes partes:
- Descripción herramienta utilizada.
- Captura de la evidencia.
- Acta de adquisición forense.

<br>

## Triaje
### Descripción herramienta utilizada
**WinAuditor** es una herramienta de auditoría diseñada para analizar y evaluar la seguridad y configuración de sistemas Windows. Proporciona un análisis exhaustivo de los aspectos críticos de los equipos, incluyendo el software instalado, la configuración de red, las políticas de seguridad, los permisos de usuario y los servicios en ejecución. Su objetivo es ayudar a administradores de sistemas y profesionales de seguridad a identificar vulnerabilidades, configuraciones inadecuadas y posibles problemas de rendimiento que puedan comprometer la seguridad de una red.

He decidido usar WinAuditor para realizar el triaje en esta adquisición porque me proporciona un análisis completo y rápido del estado de seguridad y configuración de la máquina, lo cual es crucial en la fase inicial de una investigación forense.

### Captura de la evidencia
La herramienta utilizada nos genera un archivo .html. El archivo generado se muestra como en la siguiente captura:

![triaje-1](/img/Triaje.png)


Aquí adjunto el enlace al .html completo, donde se encuentran todos los datos del triaje, como la dirección IP y MAC asociadas, Kernel, procesos, ficheros LOGS:

[Enlace a documento de triaje](https://drive.google.com/file/d/1CSjlRRftBKXiW_6bxatyTF9ngxTMeUE7/view?usp=drive_link)

<br>

### Acta de adquisición forense

| Número de caso | 01 | Fecha | 13/11/2024 |
| :---- | :---- | :---- | :---- |
| **Hora de inicio** | 10:22 | **Lugar** | Departamento IT |
| **Investigador responsable** | Álvaro Caro Fernández |  |  |

<br>

**1.- Identificación del dispositivo**

| Tipo de dispositivo | Máquina comprometida departamento IT |
| :---- | :---- |

<br>

**2.- Método de adquisición**

| Herramienta utilizada | WinAuditor |
| :---- | :---- |
| **Tipo de adquisición** | Triaje máquina |

<br>

**3.- Detalles de la evidencia adquirida**

| Nombre del archivo | FORENSE-06.html |
| :---- | :---- |
| **Tamaño del archivo** | 574 KB |

<br>

**4.- Hash de la evidencia**

| Algoritmo | MD5 |
| :---- | :---- |
| **Valor** | 598632472c70dae7bcba2bdf994dc243 |
| **Algoritmo** | **SHA-1** |
| **Valor** | b7740b3375178a4787985bb86a8ba13baf2ac870 |

<br>

**5.- Observaciones**

| Hora de finalización | 10:37 |
| :---- | :---- |
| Nombre del perito | Álvaro Caro Fernández |

<br>


## Tabla de enrutamiento
### Descripción
La tabla de enrutamiento es una estructura clave en redes que guía cómo y hacia dónde deben dirigirse los paquetes de datos. Es una lista organizada que contiene rutas de red específicas, cada una con información sobre destinos de red y las rutas para alcanzarlos. Esta tabla es utilizada por dispositivos como routers y sistemas operativos para decidir el mejor camino que un paquete de datos debe seguir desde su origen hasta su destino final en la red.

Para obtener detalles de la tabla de enrutamiento usaré el comando:

```bash
route print
```


### Captura de la evidencia
El comando nos genera lo siguiente:

![routeprint-1](/img/route-print.png)

Aquí adjunto un enlace al documento de texto:

[Enlace a documento de texto de la adquisición](https://drive.google.com/file/d/1NtS4rU002crAAefDoJwkhFxgkmgiM8Fi/view?usp=drive_link)


<br>

### Acta de adquisición forense

| Número de caso | 01 | Fecha | 13/11/2024 |
| :---- | :---- | :---- | :---- |
| **Hora de inicio** | 10:37 | **Lugar** | Departamento IT |
| **Investigador responsable** | Álvaro Caro Fernández |  |  |

**1.- Identificación del dispositivo**

| Tipo de dispositivo | Máquina comprometida departamento IT |
| :---- | :---- |

**2.- Método de adquisición**

| Herramienta utilizada | route print |
| :---- | :---- |
| **Tipo de adquisición** | Obtener información tabla de enrutamiento |

**3.- Detalles de la evidencia adquirida**

| Nombre del archivo | routeprint.txt |
| :---- | :---- |
| **Tamaño del archivo** | 3 KB |

**4.- Hash de la evidencia**

| Algoritmo | MD5 |
| :---- | :---- |
| **Valor** | 78c3648c94e7c07b8db3baee237de21c |
| **Algoritmo** | **SHA-1** |
| **Valor** | d9ff7f3d8f71716382f664916ecaceace588a3b5 |

**5.- Observaciones**

| Hora de finalización | 10:38 |
| :---- | :---- |
| Nombre del perito | Álvaro Caro Fernández |


<br>


## Tabla de caché ARP
### Descripción
La caché ARP (Address Resolution Protocol) es una tabla que almacena temporalmente las asociaciones entre las direcciones IP y las direcciones MAC en una red local. Este almacenamiento permite a los dispositivos en una red localizar rápidamente otros dispositivos dentro de la misma subred, lo que agiliza la comunicación.

Para obtener detalles de la tabla de cache ARP usaré el comando:

```bash
arp -a
```


### Captura de la evidencia
El comando nos genera lo siguiente:

![arp-1](/img/cache-arp.png)

Aquí adjunto un enlace al documento de texto:

[Enlace a documento de texto de la adquisición](https://drive.google.com/file/d/1clPpD4wp_c6mVveCODcFW-bZfBOE80C2/view?usp=drive_link)


<br>

### Acta de adquisición forense

| Número de caso | 01 | Fecha | 13/11/2024 |
| :---- | :---- | :---- | :---- |
| **Hora de inicio** | 10:38 | **Lugar** | Departamento IT |
| **Investigador responsable** | Álvaro Caro Fernández |  |  |

**1.- Identificación del dispositivo**

| Tipo de dispositivo | Máquina comprometida departamento IT |
| :---- | :---- |

**2.- Método de adquisición**

| Herramienta utilizada | arp -a |
| :---- | :---- |
| **Tipo de adquisición** | Obtener información tabla de caché |

**3.- Detalles de la evidencia adquirida**

| Nombre del archivo | cache-arp.txt |
| :---- | :---- |
| **Tamaño del archivo** | 1 KB |

**4.- Hash de la evidencia**

| Algoritmo | MD5 |
| :---- | :---- |
| **Valor** | 0fbd85d9c80a0d59b0a5116e9ff9ebb0 |
| **Algoritmo** | **SHA-1** |
| **Valor** | 99cf2171ce8e564527f3bd6b6c0862a1cab4ca95 |

**5.- Observaciones**

| Hora de finalización | 10:39 |
| :---- | :---- |
| Nombre del perito | Álvaro Caro Fernández |

<br>

## Procesos
### Descripción
El comando tasklist en Windows permite ver una lista de todos los procesos en ejecución en el sistema, proporcionando información básica sobre cada uno. Es similar al administrador de tareas, pero en formato de línea de comandos, lo que lo hace útil para automatización y gestión de procesos en sistemas remotos o sin interfaz gráfica.

Para obtener detalles de la tabla que genera, usaré el comando:

```bash
tasklist
```


### Captura de la evidencia
El comando nos genera lo siguiente:

![procesos-1](/img/tasklist.png)

Aquí adjunto un enlace al documento de texto:

[Enlace a documento de texto de la adquisición](https://drive.google.com/file/d/198paUGDh2FVhgG77flJrCqp5TLQvQxNA/view?usp=drive_link)


<br>

### Acta de adquisición forense

| Número de caso | 01 | Fecha | 13/11/2024 |
| :---- | :---- | :---- | :---- |
| **Hora de inicio** | 10:39 | **Lugar** | Departamento IT |
| **Investigador responsable** | Álvaro Caro Fernández |  |  |

**1.- Identificación del dispositivo**

| Tipo de dispositivo | Máquina comprometida departamento IT |
| :---- | :---- |

**2.- Método de adquisición**

| Herramienta utilizada | tasklist |
| :---- | :---- |
| **Tipo de adquisición** | Obtener información procesos en el sistema |

**3.- Detalles de la evidencia adquirida**

| Nombre del archivo | procesos.txt |
| :---- | :---- |
| **Tamaño del archivo** | 4 KB |

**4.- Hash de la evidencia**

| Algoritmo | MD5 |
| :---- | :---- |
| **Valor** | 1624e797148807ac723ebb8389773fde |
| **Algoritmo** | **SHA-1** |
| **Valor** | 66d21cd60ef48b9efa87354e56bc69709690e0df |

**5.- Observaciones**

| Hora de finalización | 10:40 |
| :---- | :---- |
| Nombre del perito | Álvaro Caro Fernández |

<br>

## Disco duro
### Descripción herramienta utilizada
**FTK Imager** es una herramienta forense utilizada para la adquisición y preservación de evidencia digital en investigaciones de ciberseguridad. Permite crear imágenes exactas bit a bit de discos duros, unidades de almacenamiento y otros dispositivos, asegurando que los datos no se alteren durante el proceso de captura. FTK Imager soporta varios formatos de imagen forense estándar, como E01 y AFF, y ofrece opciones para ver el contenido de un dispositivo sin necesidad de crear una imagen completa de inmediato. Es ampliamente utilizada en investigaciones forenses debido a su fiabilidad y capacidad para mantener la integridad de la evidencia.

He decidido usar FTK Imager para la adquisición del disco en esta investigación forense porque es una herramienta confiable y ampliamente utilizada en el campo de la ciberseguridad para crear imágenes forenses de discos duros. Como he mencionado anteriormente, permite crear imágenes bit a bit.


### Captura de la evidencia
La herramienta utilizada nos genera una serie de archivos, uno de ellos en formato E01, que sería la imagen del disco, y un fichero .txt, con toda la información. Una vez se ha realizado la adquisición nos muestra un mensaje como el siguiente:

![adquisiciondisco-1](/img/adquisicion-disco.png)

Aquí adjunto un enlace al documento de texto:

[Enlace a documento de texto de la adquisición](https://drive.google.com/file/d/1SMXNL6gENe0KiHqHwjHQavzbVz-wZMfL/view?usp=drive_link)


<br>

### Acta de adquisición forense

| Número de caso | 01 | Fecha | 13/11/2024 |
| :---- | :---- | :---- | :---- |
| **Hora de inicio** | 10:42 | **Lugar** | Departamento IT |
| **Investigador responsable** | Álvaro Caro Fernández |  |  |

**1.- Identificación del dispositivo**

| Tipo de dispositivo | Disco duro máquina comprometida departamento IT |
| :---- | :---- |

**2.- Método de adquisición**

| Herramienta utilizada | FTK Imager |
| :---- | :---- |
| **Tipo de adquisición** | Adquisición imagen disco duro |

**3.- Detalles de la evidencia adquirida**

| Nombre del archivo | adquisicion-disco-duro.E01 adquisicion-disco-duro.E02 adquisicion-disco-duro.E03 adquisicion-disco-duro.E04 |
| :---- | :---- |
| **Tamaño del archivo** | 1.535 MB |

**4.- Hash de la evidencia**

| Algoritmo | MD5 |
| :---- | :---- |
| **Valor** | f4974335070bd9bb776687f6c128dbcc |
| **Algoritmo** | **SHA-1** |
| **Valor** | 518b44435dc6569336992f1fc5dd4438ef932d24 |

**5.- Observaciones**

| Hora de finalización | 11:16 |
| :---- | :---- |
| Nombre del perito | Álvaro Caro Fernández |

<br>

