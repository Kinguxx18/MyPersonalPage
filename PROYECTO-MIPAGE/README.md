# Kinguxx Portfolio - Estructura del Proyecto

## Organización de Archivos

### CSS Modular
```
assets/css/
├── base/                    # Estilos fundamentales
│   ├── variables.css        # Variables CSS (colores, spacing, etc.)
│   └── reset.css            # Reset y estilos base
│
├── components/              # Componentes reutilizables
│   ├── sidebar.css          # Sidebar y navegación
│   ├── cards.css            # Tarjetas y badges
│   ├── buttons.css          # Botones
│   └── forms.css            # Formularios
│
├── sections/                # Estilos por sección
│   ├── hero.css             # Panel hero/dashboard
│   ├── projects.css         # Grid de proyectos
│   ├── skills.css           # Sección de habilidades
│   ├── about.css            # Sección about
│   └── contact.css          # Sección de contacto
│
├── utils/                   # Utilidades
│   ├── animations.css       # Animaciones y keyframes
│   └── responsive.css       # Media queries responsive
│
└── style.css                # Archivo principal (importa todo)
```

### JavaScript Modular (ES6 Modules)
```
assets/js/
├── modules/
│   ├── theme.js             # Toggle dark/light mode
│   ├── navigation.js        # Navegación y menú móvil
│   ├── form.js              # Validación y WhatsApp
│   ├── projects.js          # Interacciones de proyectos
│   └── scroll.js            # Efectos de scroll
│
├── main.js                  # Punto de entrada principal
└── preloader.js             # Animación de carga inicial
```

## Cómo Agregar Nuevas Funcionalidades

### Agregar un nuevo componente CSS
1. Crea el archivo en `components/nuevo-componente.css`
2. Importa en `style.css`:
   ```css
   @import url('./components/nuevo-componente.css');
   ```

### Agregar un nuevo módulo JavaScript
1. Crea el archivo en `modules/nuevo-modulo.js`
2. Exporta el módulo:
   ```js
   export const NuevoManager = {
       init() { /* ... */ }
   };
   ```
3. Importa en `main.js`:
   ```js
   import { NuevoManager } from './modules/nuevo-modulo.js';
   ```

## Estructura HTML
```
assets/
├── index.html               # Página principal
├── css/                     # Todos los archivos CSS
├── js/                      # Todos los archivos JavaScript
└── img/                     # Imágenes y assets
```

## Características

### Navegación Móvil
- Botón hamburguesa visible en pantallas < 768px
- Menú lateral deslizante
- Overlay oscuro al abrir menú
- Cierre automático al navegar

### Temas
- Modo oscuro/claro con persistencia en localStorage
- Toggle en la barra superior

### Formulario de Contacto
- Validación en tiempo real
- Envío por WhatsApp
- Soporte para EmailJS (opcional)

## Comandos Útiles

### Ver el sitio
Abre `assets/index.html` en un navegador o usa un servidor local:
```bash
npx serve assets
```

## Tecnologías
- HTML5 semántico
- CSS3 con variables y Grid/Flexbox
- JavaScript ES6+ (módulos nativos)
- Sin dependencias externas (excepto EmailJS opcional)
