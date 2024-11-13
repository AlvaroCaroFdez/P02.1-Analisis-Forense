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


Aquí adjunto el enlace al .html completo, donde se encuentran todos los datos del triaje, como la dirección IP y MAC asociadas, Kernel, procesos, ficheros LOGS.

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