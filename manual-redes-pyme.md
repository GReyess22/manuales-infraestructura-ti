# Permitir SSH de manera segura
sudo ufw allow 22/tcp

# Activar el cortafuegos
sudo ufw enable

# Verificar el estado
sudo ufw status verbose

### Archivo 2: `manual-redes-pyme.md`
*(Este manual valida tu experiencia en Consultoría, Redes Alámbricas y Wi-Fi)*

```markdown
# 🌐 Manual: Buenas Prácticas para el Despliegue de Redes LAN y Wi-Fi en PYMEs

## 1. Objetivo
Establecer un flujo de trabajo estructurado para el diagnóstico, instalación y configuración de redes cableadas e inalámbricas en entornos corporativos de pequeña y mediana escala.

## 2. Fase de Diagnóstico y Levantamiento de Información
Antes de realizar cualquier instalación de hardware técnico, se debe completar la siguiente lista de verificación:
- [ ] Evaluar interferencias de canales de radiofrecuencia (2.4 GHz y 5 GHz) en el área circundante.
- [ ] Verificar la calidad del cableado estructurado existente (Categoría 5e o superior recomendada para Gigabit Ethernet).
- [ ] Dimensionar el número total de hosts simultáneos (Estaciones de trabajo, laptops, móviles, impresoras de red).

## 3. Segmentación del Direccionamiento IP (Esquema Sugerido)
Para optimizar el tráfico de red, se recomienda la segmentación mediante máscaras de subred estándar de clase C:

| Segmento / VLAN | Rango de IP | Propósito |
| :--- | :--- | :--- |
| **VLAN 10: Administración** | `192.168.10.X` | Servidores, Switches, Routers |
| **VLAN 20: Datos** | `192.168.20.X` | Estaciones de Trabajo y Laptops |
| **VLAN 30: Invitados (Wi-Fi)**| `192.168.30.X` | Dispositivos móviles de visitantes (Aislados) |

## 4. Mantenimiento Preventivo
Se deben programar auditorías semestrales para medir la atenuación de la señal inalámbrica
