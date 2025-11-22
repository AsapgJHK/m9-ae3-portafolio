## Portafolio Fullstack

Este proyecto es un portafolio personal de desarrollo Fullstack diseñado para destacar habilidades y proyectos de una manera visualmente atractiva, utilizando el estilo de diseño **Frutiger Aero** (o *Data Block*) con un **fondo dinámico en 3D** creado con Three.js.

El objetivo es combinar la estética limpia y pulida de un desarrollador profesional con un toque nostálgico y futurista.

---

### 🌟 Características Principales

El diseño sigue una estética de "Bloques de Datos" y "Cristal Glossy" (**Frutiger Aero**), con énfasis en la transparencia, el brillo y los colores vibrantes (azul y verde).

* **Efecto Cristal Glossy (`.glass-container`):**
    * Utiliza `backdrop-filter: blur(25px)` para un efecto de desenfoque intenso.
    * Un `border` grueso y un `box-shadow` con brillo interno (`inset`) y sombra externa fuerte para simular el cristal pulido y brillante.
* **Fondo Dinámico 3D (Three.js):**
    * Un canvas que genera **100 cubos (píxeles de datos)** flotantes y giratorios.
    * Los cubos utilizan materiales **`MeshPhongMaterial`** con `shininess: 600` y alta transparencia para crear un efecto de **Bloques de Datos de Cristal** altamente reflectantes.
    * El movimiento es **sinusoidal** y orgánico, simulando un flujo constante de datos en 3D.
* **Componentes Icy (Botones y Títulos):**
    * **Botones (`.btn-icy`):** Diseño con degradados blancos (`linear-gradient`) para un *look* de "hielo pulido".
    * **Títulos (`.title-aero`):** Color azul vibrante con `text-shadow` blanco, imitando el efecto de brillo del cristal húmedo o del neón.
* **Estructura del Portafolio:**
    * **Perfil:** Introducción del desarrollador, rol y enlaces a GitHub y LinkedIn.
    * **Stack Tecnológico:** Organizado en una cuadrícula con tarjetas temáticas (Frontend, Backend, Datos & Cloud, DevOps & CI/CD), destacando tecnologías clave.
    * **Proyectos:** Ejemplo de proyectos con tecnologías y enlaces.

---

### ⚙️ Stack Tecnológico (Resumen)

| Área | Tecnologías Destacadas |
| :--- | :--- |
| **Diseño/Estilo** | **Frutiger Aero**, Tailwind CSS, CSS Variables |
| **Frontend** | HTML5, CSS3, JavaScript ES6+ |
| **Backend** | Node.js (Express.js), Python (Django/Flask), RESTful |
| **Base de Datos** | PostgreSQL, SQL |
| **DevOps & Cloud** | Docker, Git/GitHub |

---

### 🚀 Uso y Ejecución

El proyecto es un archivo HTML autocontenido que utiliza CDN para sus dependencias, por lo que su ejecución es inmediata.

1.  **Guardar:** Guarda el contenido del archivo como `index.html` (o usa el nombre `pixelesmod.html`).
2.  **Abrir:** Abre el archivo `index.html` directamente en tu navegador.

#### Dependencias (Cargadas vía CDN)

* **Tailwind CSS:** Para el *styling* y la estructura.
* **Fuente Inter:** Para la tipografía moderna y limpia.
* **Three.js:** Biblioteca 3D para la creación del fondo de "Píxeles de Datos Dinámicos".

---

### 💡 Lógica de Three.js (Fondo Dinámico)

El script de Three.js inicializa una escena con luces de alta intensidad (`directionalLight` con `1.8`) para maximizar el efecto *glossy* en los materiales.

La animación es la siguiente:

1.  **Geometría:** Utiliza `BoxGeometry` para los **Data Blocks** o píxeles.
2.  **Material:** Emplea `THREE.MeshPhongMaterial` con un `shininess` de **600** y `opacity` muy baja (`0.08` a `0.20`) para simular cristal altamente pulido y transparente.
3.  **Movimiento:** Cada cubo se mueve de forma independiente mediante funciones **seno y coseno** basadas en el tiempo transcurrido (`clock.getElapsedTime()`), creando un efecto de flotación orgánico y no lineal.
4.  **Rotación:** Los cubos giran constantemente en sus ejes X e Y (`cube.rotation.x += ...`), proporcionando una sensación de flujo de datos continuo en 3D.

---
