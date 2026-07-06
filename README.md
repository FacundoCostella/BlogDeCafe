# BlogDeCafé

Blog de café de especialidad con consejos, recetas y cursos para entusiastas del café.

## Estructura del proyecto

```
blogCafe/
├── index.html          # Página principal — blog + fichas de cata
├── nosotros.html       # Sobre nosotros
├── cursos.html         # Cursos y talleres disponibles
├── contacto.html       # Formulario de contacto funcional
├── entrada.html        # Página de artículo individual
├── css/
│   ├── normalize.css   # Reset cross-browser
│   └── style.css       # Estilos completos del sitio
└── img/
    ├── banner.jpg      # Hero principal
    ├── blog1.jpg       # Entrada: tipos de grano
    ├── blog2.jpg       # Entrada: recetas de café
    ├── blog3.jpg       # Entrada: beneficios del café
    ├── curso1.jpg      # Curso: técnicas de extracción
    ├── curso2.jpg      # Curso: recetas para principiantes
    ├── curso3.jpg      # Curso: cata y perfiles de sabor
    └── nosotros.jpg    # Foto del equipo
```

## Tecnologías

- **HTML5** — estructura semántica
- **CSS3** — custom properties, grid, flexbox, animaciones
- **JavaScript** — IntersectionObserver (scroll reveal), Fetch API (formulario)
- **Google Fonts** — DM Serif Display, Inter, IBM Plex Mono

## Diseño

El sitio usa un sistema de diseño con tokens de color y tipografía:

| Token | Hex | Uso |
|---|---|---|
| `espresso` | `#1C1410` | Texto principal, fondos oscuros |
| `copper` | `#B87333` | Acento — botones, hover, líneas |
| `parchment` | `#F5F0E8` | Fondo de página |
| `burlap` | `#D4C5A9` | Barras de progreso, bordes |
| `smoke` | `#6B5E54` | Texto secundario |
| `steam` | `#FAFAF7` | Cards, fondos claros |

### Fuentes

- **DM Serif Display** — títulos (display)
- **Inter** — cuerpo (body)
- **IBM Plex Mono** — etiquetas, datos, fichas de cata (utility)

## Formulario de contacto

El formulario usa [Web3Forms](https://web3forms.com/) para enviar mensajes por email sin backend.

### Configuración

1. Ir a https://web3forms.com/
2. Ingresar tu email y obtener el access key
3. Reemplazar `TU_ACCESS_KEY_AQUI` en `contacto.html` línea 44:

```html
<input type="hidden" name="access_key" value="TU_ACCESS_KEY_AQUI">
```

## Características

- **Responsive** — diseño adaptable desde mobile hasta desktop
- **Scroll reveal** — animaciones al hacer scroll con IntersectionObserver
- **Fichas de cata** — sidebar con tarjetas de profiling de café (barras de atributos, tags de sabor)
- **Accesibilidad** — focus visible en elementos interactivos, `prefers-reduced-motion` respetado
- **Anti-spam** — honeypot field en el formulario

## Cómo usar

Abrir `index.html` en un navegador. No requiere servidor de desarrollo ni build tools.

```bash
# Opcional: usar un servidor local
npx serve .
# o
python -m http.server 8000
```
