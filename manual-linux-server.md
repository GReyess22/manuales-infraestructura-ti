# 🐧 Manual: Configuración Estándar y Aseguramiento de Servidores Linux

## 1. Introducción
Este manual técnico proporciona las directrices base para la instalación, actualización y aseguramiento inicial de un servidor basado en distribuciones empresariales Linux (Debian/Ubuntu Server/CentOS), optimizado para servicios pyme.

## 2. Requerimientos Previos
- Acceso SSH al servidor con privilegios de `root` o mediante directiva `sudo`.
- Conectividad a la red configurada con IP estática.

## 3. Secuencia de Despliegue Técnico

### Paso 3.1: Actualización Inicial del Sistema
Antes de instalar cualquier servicio, es mandatorio actualizar los repositorios y los paquetes del sistema base para mitigar vulnerabilidades de seguridad.

```bash
sudo apt update && sudo apt upgrade -y
# Permitir SSH de manera segura
sudo ufw allow 22/tcp

# Activar el cortafuegos
sudo ufw enable

# Verificar el estado
sudo ufw status verbose
