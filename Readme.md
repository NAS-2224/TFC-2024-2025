# MV - Virtualbox. Proyecto sobre la construcción de un CTF y una plataforma para registrar banderas

Este repositorio contiene dos máquinas virtuales en formato `.ova`, diseñadas para un entorno de ciberseguridad, como parte de un proyecto tipo Capture The Flag (CTF).

## Contenido

- `MV1`: Máquina objetivo (Ubuntu server vulnerable) 
- `MV2`: Máquina registro banderas (Windows 10) 
- `Enlace`: https://mega.nz/folder/pMwUWRIT#tepNb0a1e8tDmzWcikITCg 

## Requisitos

- [VirtualBox](https://www.virtualbox.org/)
- Al menos 30 GB de espacio libre en disco
- Git LFS instalado (para archivos grandes)
- WinRAR para descomprimir las máquinas
- Una máquina atacante (se recomienda Kali Linux)

## Instalación

1. Clona el repositorio:
   ```bash
   git clone https://github.com/tu-usuario/mi-repo-vms.git
   cd mi-repo-vms

2. Abre VirtualBox > Archivo > Importar servicio virtualizado
   Selecciona mv-vulnerable.ova y después plataforma-bandera.ova


# VM1 - Ubuntu Vulnerable (Máquina objetivo)

## Descripción

Máquina Ubuntu server con aplicaciones y configuraciones vulnerables intencionadamente para retos de ciberseguridad con formato CTF.

## Especificaciones

- **SO**: Ubuntu Server 20.04
- **RAM**: 4 GB
- **Disco**: 10 GB
- **Usuario**: `avatar`
- **Contraseña**: `avatar123`
- **Red**: Red NAT (`NatNetwork`)
- **IP esperada**: `10.0.2.15`

## Servicios expuestos

- HTTP (puerto 80)
- SSH (puerto 22)
- FTP (puerto 20)

## Vulnerabilidades intencionadas

- FTP con acceso anonimo
- Página web con usuarios y claves en el código
- Imagen con  metadatos que incluyen super usuario y contraseña

## Notas

- Web vulnerable disponible en: `10.0.2.15`
- Pensada para ser atacada desde `Kali Linux`


# VM2 - Windows 10 (Máquina para comprobar banderas)

## Descripción

Máquina basada en Windows 10 que incluye un formulario PHP y una base de datos con XAMPP. Sirve para simular una competición por equipos que registran sus banderas (`VM2`).

## Especificaciones

- **SO**: Windows 10
- **RAM**: 4 GB
- **Disco**: 25 GB
- **Usuario**: `avatar`
- **Contraseña**: `Ninguna`
- **Red**: Red NAT (`NatNetwork`)
- **IP esperada**: `10.0.2.13`

## Herramientas instaladas

- XAMPP con Apache y MySQL
