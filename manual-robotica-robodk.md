# 🦾 Manual: Introducción a la Simulación de Robótica Industrial con RoboDK

## 1. Objetivo del Manual
Esta guía práctica tiene como propósito introducir a los participantes de ingeniería y mecatrónica en el uso de **RoboDK**, una herramienta de software avanzada para la simulación y programación sin conexión (OLP) de robots industriales. El enfoque de este laboratorio está diseñado bajo la metodología de formación técnica centrada en el participante.

## 2. Conceptos Clave de la Celda Robótica
Antes de manipular el software, es mandatorio comprender los componentes esenciales en un entorno de simulación:
* **Estación (Station):** El entorno virtual de trabajo completo que contiene el robot, las herramientas y los objetos.
* **TCP (Tool Center Point):** El punto central de la herramienta instalada en la brida del robot (ej: una pinza de agarre, una antorcha de soldadura).
* **Sistemas de Referencia (Frame de Referencia):** Sistemas de coordenadas cartesianas ($X, Y, Z$) que permiten posicionar objetos y definir trayectorias con respecto a la base del robot o al espacio de trabajo.

---

## 3. Secuencia del Laboratorio: Configuración de una Celda Básica

### Paso 3.1: Importación del Robot desde la Librería en la Nube
1. Abre RoboDK y selecciona el icono de la **Librería Web**.
2. Filtra por fabricante (ej: *ABB, Fanuc, KUKA, Universal Robots*).
3. Selecciona un brazo articulado de 6 ejes (ej: **KUKA KR 6 R900**) y haz clic en *Download*. El robot aparecerá automáticamente en el centro de tu estación virtual.

### Paso 3.2: Adición de la Herramienta (End Effector)
1. En la librería local o web, descarga una herramienta de sujeción estándar (*Gripper*).
2. Arrastra el archivo de la herramienta sobre el nombre del robot en el árbol de la izquierda. RoboDK acoplará mecánicamente el TCP a la brida del robot de forma automática.

### Paso 3.3: Programación de Puntos de Trayectoria (Targets)
Para mover el robot de manera segura, utilizaremos comandos de movimiento lineal y articular.

```text
[Posición de Inicio: Home]  --> Movimiento Articular (Joint Move - PTP)
          ⬇️
[Aproximación al Objeto]    --> Movimiento Lineal (Linear Move)
          ⬇️
[Punto de Sujeción / Pick]  --> Activación de la Herramienta (Acción de Agarre)

5. Baja hasta el final de la página, haz clic en el botón verde **`Commit changes...`** y vuelve a confirmar en la ventana emergente. ¡Tu nuevo manual ya está arriba!

---

## 🛠️ PASO 2: Actualizar el Índice en tu `README.md`

Para que este manual aparezca listado en la portada de tu repositorio, debemos editar el archivo principal.

1. En la página de inicio de tu repositorio, haz clic sobre el archivo **`README.md`**.
2. Haz clic en el icono del **lápiz** ✏️ (arriba a la derecha) para entrar al modo de edición.
3. Busca la sección de **`## 🗺️ Índice de Contenidos`** y reemplaza esa lista por esta nueva versión actualizada que incluye el manual de Mecatrónica:

```markdown
## 🗺️ Índice de Contenidos

Haga clic en los enlaces para acceder a los manuales detallados (Archivos en formato Markdown dentro de este repositorio):

1. [📂 Manual 1: Configuración Estándar de Servidores Linux Empresariales](./manual-linux-server.md)
   *Guía paso a paso para el despliegue seguro de sistemas operativos de servidor orientados a pymes.*
2. [📂 Manual 2: Diseño y Auditoría Básica de Redes Alámbricas y Wi-Fi](./manual-redes-pyme.md)
   *Checklist y mejores prácticas para el aprovisionamiento de infraestructura de red local.*
3. [📂 Manual 3: Guía Metodológica para la Virtualización de la Enseñanza Técnica](./guia-andragogia-virtual.md)
   *Estrategias didácticas enfocadas en el participante para entornos de educación técnica y videoconferencia.*
4. [📂 Manual 4: Introducción a la Simulación de Robótica Industrial con RoboDK](./manual-robotica-robodk.md)
   *Guía de laboratorio para el diseño de celdas robóticas, prevención de colisiones y trayectorias industriales.*
- **Mecatrónica:** Simulación robótica (RoboDK), cinemática de brazos de 6 ejes, automatización industrial.
