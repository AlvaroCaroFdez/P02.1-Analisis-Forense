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