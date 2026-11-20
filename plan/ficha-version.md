
# Ficha de verificación de versión - Grupo 02

## Información general

- Universidad del Valle - Sede Yumbo
- Asignatura: Sistemas Operativos
- Semestre: 2026-2
- Fecha de consulta: 19 de noviembre de 2026

## Distribuciones asignadas

| Componente | Distribución | Versión seleccionada |
|---|---|---|
| Máquina virtual gráfica | Linux Mint | 22.3 Cinnamon |
| Máquina virtual de consola | Rocky Linux | 10.3 |
| Imagen base del Dockerfile | Debian | 13 Trixie |

## 1. Linux Mint - Máquina virtual gráfica

| Pregunta | Respuesta | Fuente oficial |
|---|---|---|
| Versión y fecha de lanzamiento | Linux Mint 22.3 Cinnamon (Zena), publicada el 13 de enero de 2026. | [Lanzamiento](https://blog.linuxmint.com/?p=4981) |
| Actualizaciones de seguridad | Cuenta con soporte a largo plazo (LTS) hasta abril de 2029. | [Versiones](https://www.linuxmint.com/download_all.php) |
| Requisitos de hardware y VirtualBox | Requiere 2 GB de RAM como mínimo, recomienda 4 GB y necesita 20 GB de almacenamiento como mínimo. Presenta posibles problemas de compatibilidad con VirtualBox debido al kernel 6.14. | [Requisitos](https://blog.linuxmint.com/?p=4981) - [Notas de versión](https://www.linuxmint.com/rel_zena.php) |
| Particionado manual | Sí. El instalador permite seleccionar la opción Something else para crear las particiones manualmente. | [Guía de instalación](https://linuxmint-installation-guide.readthedocs.io/en/latest/install.html) |
| Guía oficial de Docker Engine | Existe una guía oficial para Ubuntu, distribución en la que se basa Linux Mint. Docker no garantiza oficialmente su funcionamiento en Linux Mint. | [Docker para Ubuntu](https://docs.docker.com/engine/install/ubuntu/) |
| Imagen base en Docker Hub | No se identificó una imagen oficial de Linux Mint 22.3 en Docker Hub. Para el proyecto utilizaremos Debian como imagen base asignada al grupo. | [Docker Hub](https://hub.docker.com/search?q=linuxmint) |

### Configuración propuesta

- Nombre: g02-grafica.
- Memoria RAM: 4 GB, para facilitar el funcionamiento del escritorio Cinnamon.
- Disco virtual: 25 GB.
- Procesadores: 2.
- Particiones: /, swap y /home.

## 2. Rocky Linux - Máquina virtual de consola

| Pregunta | Respuesta | Fuente oficial |
|---|---|---|
| Versión y fecha de lanzamiento | Rocky Linux 10.3, publicada el 16 de noviembre de 2026. | [Lanzamiento](https://rockylinux.org/news/rocky-linux-10-3-ga-release) |
| Actualizaciones de seguridad | La serie Rocky Linux 10 cuenta con soporte de seguridad hasta el 31 de mayo de 2035, manteniendo actualizadas sus versiones menores. | [Ciclo de soporte](https://docs.rockylinux.org/releases/) |
| Requisitos de hardware y VirtualBox | Requiere un procesador compatible con x86-64-v3, 2 GB de RAM para instalación en modo texto y un mínimo de 10 GB de almacenamiento. Es compatible con VirtualBox si se cumplen los requisitos de hardware. | [Requisitos](https://docs.rockylinux.org/guides/minimum_hardware_requirements/) - [VirtualBox](https://docs.rockylinux.org/guides/virtualization/vbox-rocky/) |
| Particionado manual | Sí. El instalador permite configurar las particiones manualmente desde Installation Destination. | [Instalación](https://docs.rockylinux.org/10/guides/installation/) |
| Guía oficial de Docker Engine | Sí. Docker dispone de documentación oficial para Rocky Linux, incluyendo la versión 10. | [Docker para Rocky Linux](https://docs.docker.com/engine/install/rockylinux/) |
| Imagen base en Docker Hub | Sí. Existe la imagen oficial rockylinux:10.3, aunque para nuestro proyecto utilizaremos Debian. | [Rocky Linux en Docker Hub](https://hub.docker.com/_/rockylinux/tags) |

### Configuración propuesta

- Nombre: g02-consola.
- Memoria RAM: 2 GB durante la instalación y 3 GB para el Sprint 3.
- Disco virtual: 25 GB.
- Procesadores: 2.
- Instalación mínima, sin escritorio.
- Particiones: /, swap, /home y /var.

## 3. Debian - Imagen base del Dockerfile

| Pregunta | Respuesta | Fuente oficial |
|---|---|---|
| Versión y fecha de lanzamiento | Debian 13 (Trixie), publicada inicialmente el 9 de agosto de 2025. La actualización 13.7 fue publicada el 12 de septiembre de 2026. | [Información de la versión](https://www.debian.org/releases/trixie/) |
| Actualizaciones de seguridad | Soporte completo hasta el 9 de agosto de 2028 y soporte LTS hasta el 30 de junio de 2030. | [Ciclo de soporte](https://www.debian.org/releases/) |
| Requisitos de hardware y VirtualBox | Es compatible con equipos de arquitectura amd64. En este proyecto se ejecutará como contenedor en Rocky Linux, por lo que no necesita una máquina virtual independiente. | [Información de Debian](https://www.debian.org/releases/trixie/) |
| Particionado manual | Debian permite el particionado manual durante su instalación. En este proyecto no será necesario porque se utilizará como imagen de contenedor. | [Guía de instalación](https://www.debian.org/releases/trixie/amd64/) |
| Guía oficial de Docker Engine | Sí. Docker cuenta con una guía oficial de instalación para Debian. | [Docker para Debian](https://docs.docker.com/engine/install/debian/) |
| Imagen base en Docker Hub | Sí. Debian dispone de una imagen oficial con la etiqueta debian:13, que corresponde a Trixie. | [Imagen oficial de Debian](https://hub.docker.com/_/debian/) |
