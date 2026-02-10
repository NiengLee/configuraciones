Existen 4 maneras de instalar paquetes en ubuntu linux :

1. Directamente descargando de internet y seguir sus manuales.
2. Por la app store de ubuntu linux, en la central de comandos.
3. Con `sudo snap install <nombre_paquete>`.
4. Con el gestor de paquetes de instalación `sudo apt install <nombre_paquete>`.

## Paso 1.

En la lista anterior, empezaremos con la opción 4, ya que se deben de instalar programas básicos directamente del repositorio de ubuntu linux, en la que los programas esenciales ya estan previamente auditados y revisados por la comunidad de ubuntu.

Se recomienda ejecutar los siguientes comandos cuando recién se instala ubuntu linux desde la terminal de comandos para actualizar todos los programas básicos necesarios para instalar los demás :

```bash
sudo apt update && sudo apt upgrade -y
```

Luego ejecutar el siguiente comando :

```bash
sudo apt install git build-essential curl wget \
unzip zip tree jq \
ca-certificates software-properties-common \
apt-transport-https gnupg lsb-release \
htop net-tools iproute2 dnsutils \
rsync lsof file \
openssh-client
```

Los programas que se descarga en el comando anterior  son : 

|Programa|Descripción|
|---|---|
|git|Sistema de control de versiones distribuido para gestionar código fuente y proyectos de software.|
|build-essential|Conjunto de herramientas básicas de compilación en Linux (gcc, g++, make, libc).|
|curl|Herramienta para transferir datos desde o hacia servidores usando HTTP, HTTPS y otros protocolos.|
|wget|Utilidad para descargar archivos desde la web de forma no interactiva.|
|unzip|Permite descomprimir archivos en formato ZIP.|
|zip|Permite comprimir archivos en formato ZIP.|
|tree|Muestra la estructura de directorios en forma de árbol.|
|jq|Procesador de JSON desde línea de comandos para filtrar y transformar datos.|
|ca-certificates|Certificados raíz necesarios para conexiones TLS/SSL seguras.|
|software-properties-common|Permite gestionar repositorios adicionales (add-apt-repository).|
|apt-transport-https|Habilita el uso de repositorios APT accesibles vía HTTPS.|
|gnupg|Herramienta para cifrado y verificación criptográfica (GPG).|
|lsb-release|Proporciona información sobre la versión y distribución de Linux instalada.|
|htop|Monitor interactivo de procesos y uso de recursos del sistema.|
|net-tools|Utilidades clásicas de red (ifconfig, netstat), hoy en desuso pero aún útiles.|
|iproute2|Herramientas modernas para configuración y diagnóstico de red (ip, ss).|
|dnsutils|Utilidades para diagnóstico DNS (dig, nslookup).|
|rsync|Sincronización eficiente de archivos y directorios, local o remota.|
|lsof|Lista archivos abiertos y procesos que los están utilizando.|
|file|Identifica el tipo real de un archivo según su contenido.|
|openssh-client|Cliente SSH para conexiones seguras a servidores remotos.|
### Ventajas
- ✔ Muy estable
- ✔ Rápido
- ✔ Bien integrado con el sistema
- ✔ Consume menos recursos

### Desventajas
- ✖ Versiones no siempre son las más nuevas
- ✖ Limitado a los repos oficiales

## Paso 2.

Entre la opción 2 y 3 mostrados al inicio de este manual, es importante tener claro lo siguiente:

"Instalar una aplicación desde la Ubuntu Software es, en la mayoría de los casos, equivalente a instalarla mediante snap desde la línea de comandos."

Por tanto, se puede ejecutar el comando `snap install firefox` para instalar el navegador web firefox, o realizarlo directamente del centro de aplicaciones

#### ¿Que descargar por este medio?
- Telegram
-  Spotify
- Postman
- Discord
- Slack

### Ventajas
| Por central de aplicaciones        | Por medio de snap en la terminal |
| ---------------------------------- | -------------------------------- |
| ✔ Muy fácil (no requiere terminal) | ✔ Instalación sencilla           |
| ✔ Instalación segura               | ✔ Funciona en muchas distros     |
| ✔ Actualizaciones automáticas      | ✔ Siempre actualizado            |
|                                    | ✔ No rompe el sistema            |

### Desventajas
| Por central de aplicaciones      | Por medio de snap en la terminal   |
| -------------------------------- | ---------------------------------- |
| ✖ A veces versiones más antiguas | ✖ Ocupa más espacio                |
| ✖ Menos control técnico          | ✖ Menor integración con el sistema |
| ✖ Puede ser más lenta            | ✖ Arranque más lento               |

### Paso 3.

Instalar un programa descargando el instalador desde la página web oficial del software.
Normalmente se descarga un archivo como:

- .deb
- .tar.gz
- .AppImage

Instalar con el siguiente comando para algunos casos :

```bash
sudo dpkg -i <nombre_paquete_software>
```

Si hay errores de dependencias, ejecutar el siguiente comando para actualizar librerías desactualizadas o que no están instaladas y son requeridas :

```bash
sudo apt --fix-broken install
```

Muchas veces en la fuente de descagar dan las indicaciones o paso a paso para instalar el software de manera confiable, se recomienda seguir estos pasos como en el siguiente ejemplo :

[Descarga del navegador Brave en ubuntu linux](https://brave.com/linux/)
### Ventajas
- ✔ Versión oficial del desarrollador
- ✔ A veces más actualizada
- ✔ Funciona incluso sin tienda gráfica
### Desventajas
- ✖ No siempre se actualiza automáticamente
- ✖ Hay que confiar en la fuente
- ✖ Requiere más pasos
