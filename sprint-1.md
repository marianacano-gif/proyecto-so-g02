---
layout: default
---

[Volver al inicio](index.html)

# Sprint 1 - Montaje

**Grupo 02 - Sistemas Operativos**

**Fecha de entrega:** 27 de noviembre de 2026.

## Objetivo

Instalar las dos máquinas virtuales, configurar la comunicación entre ellas, comprobar el acceso por SSH y crear las instantáneas.

## 1. Máquina virtual gráfica - Linux Mint

- Distribución: Linux Mint 22.3 Cinnamon.
- Nombre de la máquina: g02-grafica.

### Procedimiento
Primero descargamos virtual box y creamos una maquina virtual. También descargamos la imagen ISO de linuxMint 22.3 CINNAMON y la montamos en la maquina virtual. A la maquina virtual le asignamos memoria RAM, núcleos del procesador y espacio de disco. Ya creada con un usuario y contraseña la iniciamos: 
<img width="975" height="911" alt="image" src="https://github.com/user-attachments/assets/7d59f7a1-7574-4ae5-8637-6de899125771" />
<img width="975" height="958" alt="image" src="https://github.com/user-attachments/assets/c464c2ec-cfd1-4529-9284-a407d0fa162c" />

### Particionado manual

| Partición | Tamaño | Justificación |
|---|---|---|
| / | 20000 | Asigno 20gb porque pensamos esta maquina virtual para guardar archivos, o guardar proyectos y no para una exalabilidad. |
| swap | 2047 | Como no es una maquina virtual donde se hagan tareas tan pesadas, este respaldo es suficiente para su uso pensado |
| /home | 4794 | el resto del espacio, no hay más opción  |
<img width="1275" height="898" alt="image" src="https://github.com/user-attachments/assets/3e413742-c03f-4f03-b2f1-0e66f62b7226" />



### Programas instalados

- Navegador 1: FireFox
- <img width="975" height="537" alt="image" src="https://github.com/user-attachments/assets/34b881d3-145e-4f17-8720-32368f510da8" />

- Navegador 2: Opera
- <img width="975" height="622" alt="image" src="https://github.com/user-attachments/assets/854dc38b-2aab-4708-97b5-8653c4cd8c14" />

- Editor 1: Mousepad
- <img width="975" height="636" alt="image" src="https://github.com/user-attachments/assets/e782b466-af3c-4920-b5fa-9321b703551c" />
<img width="975" height="646" alt="image" src="https://github.com/user-attachments/assets/9399549b-77cb-4835-9056-db5ec93843cb" />


### Comandos utilizados
sudo apt install firefox -y
sudo apt install mousepad -y

### Evidencias

- Editor de particiones.
- <img width="975" height="977" alt="image" src="https://github.com/user-attachments/assets/d14de5b8-4e71-48bf-921d-cd11acd4d3a5" />

- Comando `lsblk`.
- Comando `df -h`.
- Comando `cat /etc/fstab`.
- <img width="1275" height="898" alt="image" src="https://github.com/user-attachments/assets/9f5bff4f-2fad-49bd-a6e8-68dad32172fe" />

- Navegadores y editores.

### Explicación de los resultados

Pendiente.

---

## 2. Máquina virtual de consola - Rocky Linux

- Distribución: Rocky Linux 10.3.
- Nombre de la máquina: g02-consola.

### Procedimiento

Descargamos la imagen ISO y la montamos en una nueva maquina virtual.

### Particionado manual

| Partición | Tamaño | Justificación |
|---|---|---|
| / | 16Gb | es donde se encuentran los componentes principales del sistema operativo y los programas necesarios para el funcionamiento del servidor |
| swap | 2Gb | proporcionar memoria de intercambio adicional a los 8 GB de RAM asignados a la máquina virtual. |
| /home | 7Gb | para mantener separados los archivos personales de los usuarios respecto a los archivos del sistema. |

### Herramientas requeridas

- make
- rsync
- curl
- git
- wget

### Comandos utilizados
sudo dnf update -y
sudo dnf install -y make rsync curl git wget

### Evidencias

- Comando `lsblk`.
- Comando `df -h`.
- <img width="1280" height="512" alt="Captura de pantalla 2026-11-27 203754" src="https://github.com/user-attachments/assets/b10dc830-2175-41d4-a24f-fd9036500310" />

- Comando `cat /etc/fstab`.
- <img width="812" height="345" alt="Captura de pantalla 2026-11-27 203832" src="https://github.com/user-attachments/assets/bdcd4a07-282c-4bec-8bef-40eca1127013" />

- Verificación de las herramientas instaladas.
- <img width="1133" height="857" alt="image" src="https://github.com/user-attachments/assets/90cc0112-ecea-4211-ab62-458536052d95" />


### Explicación de los resultados

después de instalar RockyLinux y de distribuir el disco instalamos sus herramientas. Previo a ello usamos sudo dnf update -y para actualizar las dependencias del OS, así después de usar el comando sudo dnf install todo funcionara en la versión más reciente

## 3. Configuración de red

### Procedimiento

Pendiente.

### Direcciones IP

| Máquina virtual | Dirección IP |
|---|---|
| g02-grafica | Pendiente |
| g02-consola | Pendiente |

### Comandos utilizados

Pendiente.

### Evidencias

- Comando `ip a` en ambas máquinas.
- Ping desde la máquina gráfica a la consola.
- Ping desde la máquina consola a la gráfica.

### Explicación de los resultados

Pendiente.

---

## 4. Conexión SSH

### Procedimiento

Pendiente.

### Comandos utilizados

Pendiente.

### Evidencias

Sesión SSH desde la máquina gráfica hacia la máquina de consola.

### Explicación de los resultados

Pendiente.

---

## 5. Instantáneas

Nombre de las instantáneas: `instalacion-limpia`.

### Procedimiento

Pendiente.

### Evidencias

- Instantánea de la máquina gráfica.
- Instantánea de la máquina de consola.

### Explicación de los resultados

Pendiente.

---

## Código del Sprint 1

Pendiente de registrar el código publicado por el docente en el archivo `codigo_sprint1.txt` de ambas máquinas virtuales.

## Video del Sprint 1

Pendiente de grabar y publicar en YouTube.

Duración máxima: 3 minutos.

## Participación de los integrantes

| Integrante | Actividades realizadas | Commits |
|---|---|---|
| Mariana Buitrago Cano | Configuración de GitHub Pages, creación de la página principal, páginas de los sprints y glosario. | 9 commits |
| Jean Carlos Quintero Urriago | Pendiente | 0 commits |
| Thevinson Velásquez | Pendiente | 0 commits |

## Errores y soluciones

Pendiente.

## Fuentes consultadas

Pendiente.

---

[Volver al inicio](index.html)
