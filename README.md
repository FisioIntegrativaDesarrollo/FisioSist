# Simuladores interactivos de Fisiología

Colección de simulaciones interactivas para la docencia de fisiología, desarrolladas por **FisioIntegrativaDesarrollo**. Cada simulación es una página web independiente que se abre en el navegador, sin instalar nada.

**Sitio web:** https://fisiointegrativadesarrollo.github.io/FisioSist/

## Simulaciones

### Fisiología cardiovascular

| Simulación | Archivo |
|---|---|
| Potencial de acción del nodo sinusal (modelo de Fabbri 2017) | `potencial_nodo_sinusal_fabbri2017.html` |
| Potencial de acción ventricular humano (modelo de O'Hara-Rudy 2011) | `potencial_ventricular_ord2011.html` |
| ECG y bucle presión-volumen | `ecg_bucle_presion_volumen.html` |
| Frank-Starling y asa presión-volumen | `modelo_frank_starling.html` |
| Simulador circulatorio | `simulador_circulatorio.html` |
| Física de fluidos y hemodinámica del sistema circulatorio | `fisica_fluidos_hemodinamica_circulatorio.html` |

### Microcirculación

| Simulación | Archivo |
|---|---|
| Intercambio capilar | `intercambio_capilar.html` |

### Fisiología respiratoria

| Simulación | Archivo |
|---|---|
| Intercambio de O₂ y CO₂ en el capilar pulmonar | `intercambio_o2_co2_capilar_pulmonar.html` |
| Dinámica respiratoria: presiones, diafragma y difusión de gases | `dinamica_respiratoria_presiones_difusion.html` |
| Física de fluidos en el sistema respiratorio (8 módulos con definiciones) | `fisica_fluidos_sistema_respiratorio.html` |

### Fisiología renal

| Simulación | Archivo |
|---|---|
| Modelo integrado de fisiología glomerular | `modelo_integrado_fisiologia_glomerular.html` |

## Destacados de la simulación ECG y bucle presión-volumen

- Las gráficas se recalculan al instante al cambiar precarga, poscarga, contractilidad o frecuencia. La casilla **Actualizar al instante** permite en cambio ver la transición gradual latido a latido.
- **Restablecer parámetros** devuelve todos los controles y el ritmo a sus valores iniciales.
- **Inducir fibrilación auricular**: sin onda P ni sístole auricular, con intervalos RR irregulares.
- **Inducir fibrilación ventricular**: ECG caótico, sin eyección y con caída progresiva de la presión arterial. Se revierte con **Desfibrilar**.

## Estructura del repositorio

```
FisioSist/
├── index.html          # Página de inicio con las tarjetas de cada simulación
├── README.md
└── simulaciones/
    ├── ecg_bucle_presion_volumen.html
    ├── intercambio_capilar.html
    └── ...             # una página HTML por simulación
```

Cada simulación es un único archivo HTML con su propio código y estilos.

## Uso

**En línea:** abre el sitio web indicado arriba y elige una simulación desde la página de inicio.

**En tu computador:** descarga el repositorio y abre `index.html` con cualquier navegador moderno (Chrome, Firefox, Edge o Safari). No requiere servidor ni instalación.

## Publicación en GitHub Pages

1. En el repositorio, ve a **Settings → Pages**.
2. En **Source**, elige **Deploy from a branch**.
3. Selecciona la rama `main` y la carpeta `/ (root)`, y presiona **Save**.
4. Tras 1 o 2 minutos el sitio queda disponible. Para ver cambios recientes, recarga con Ctrl+F5.

## Agregar una nueva simulación

1. Copia el archivo `.html` a la carpeta `simulaciones/`. Usa nombres en minúsculas, sin tildes ni espacios (por ejemplo, `mi_simulacion.html`).
2. En `index.html`, dentro del bloque `<div class="grid">` de la sección que corresponda, agrega:

```html
<a class="card" href="simulaciones/mi_simulacion.html">
  <h3>Título de la simulación</h3>
  <p>Descripción breve.</p>
  <span>Abrir simulación →</span>
</a>
```

3. Si pertenece a un tema nuevo, agrega antes un encabezado `<h2>Nombre de la sección</h2>` y un nuevo `<div class="grid">`.
4. Sube los cambios al repositorio.

## Dependencias externas

Casi todas las simulaciones funcionan sin conexión. Algunas cargan recursos desde internet:

- **Chart.js** (cdnjs.cloudflare.com): lo usa `modelo_frank_starling.html` para los gráficos. Sin conexión esa simulación no muestra sus gráficos.
- **Google Fonts**: tipografías de varias páginas. Sin conexión se usan tipografías del sistema y todo sigue funcionando.

## Referencias de los modelos

- Fabbri A, et al. (2017). Computational analysis of the human sinus node action potential. *eLife*.
- O'Hara T, Virág L, Varró A, Rudy Y (2011). Simulation of the undiseased human cardiac ventricular action potential. *PLoS Computational Biology*.
- Weibel ER (1963). *Morphometry of the Human Lung*. Springer.

## Aviso

Estas simulaciones son modelos simplificados con fines **educativos**. Los valores corresponden a situaciones típicas de adulto sano o son ilustrativos, y no deben usarse para tomar decisiones clínicas.

## Licencia

Pendiente de definir por los autores. Mientras no se indique una licencia, todos los derechos quedan reservados.
