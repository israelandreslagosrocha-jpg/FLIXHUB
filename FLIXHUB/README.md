# 🎬 FlixHub - Plataforma de Películas con SASS

Una página moderna de streaming de películas construida con SASS/SCSS.

## 📁 Estructura del Proyecto

```
scss/
├── abstracts/
│   ├── variables.scss      # Colores, fuentes y espaciados
│   └── mixins.scss         # Funciones y mixins reutilizables
├── base/
│   ├── reset.scss          # Reset y normalizaciones
│   └── typography.scss     # Tipografías y textos
├── components/
│   ├── buttons.scss        # Estilos de botones
│   └── cards.scss          # Estilos de tarjetas de películas
├── layout/
│   ├── header.scss         # Encabezado y navegación
│   ├── footer.scss         # Pie de página
│   └── main.scss           # Archivo principal que importa todo
├── index.html              # Página HTML
├── styles.css              # CSS compilado (genérado)
└── README.md              # Este archivo
```

## 🎨 Características

✨ **Sistema de Variables SASS**
- Paleta de colores cinético (rojo Netflix)
- Variables de espaciado escalables
- Tipografías modernas

🔄 **Mixins Reutilizables**
- Flexbox para centrado y alineación
- Transiciones suaves
- Media queries responsive
- Sombras y efectos visuales

📱 **Diseño Responsive**
- Mobile First
- Breakpoints: Mobile (480px), Tablet (768px), Desktop (1024px)
- Grid automático para tarjetas

🎯 **Componentes**
- Botones (primario, secundario, outline)
- Tarjetas de películas con hover effects
- Header sticky con navegación
- Footer con secciones

## 🚀 Cómo Usar

### Opción 1: Compilar localmente (Node.js + SASS)

1. **Instala Node.js** si no lo tienes: https://nodejs.org/

2. **Instala SASS globalmente:**
```bash
npm install -g sass
```

3. **Compila SCSS a CSS** (desde la carpeta del proyecto):
```bash
sass layout/main.scss styles.css
```

4. **Modo watch (para desarrollo):**
```bash
sass --watch . --output . --style compressed
```

### Opción 2: Usar Visual Studio Code

1. Instala la extensión **Live Sass Compiler** en VS Code
2. Haz clic en "Watch Sass" en la parte inferior
3. Los cambios se compilarán automáticamente

### Opción 3: Usar una herramienta online

- **SassTranspiler**: https://maelics.github.io/SassTranspiler/
- Copia el contenido de `layout/main.scss` y pega en la herramienta

## 📝 Variables Disponibles

### Colores
```scss
$color-primary: #e50914;      // Rojo Netflix
$color-secondary: #221f1f;    // Negro profundo
$color-bg: #141414;           // Fondo oscuro
$color-text: #ffffff;         // Texto blanco
$color-accent: #564d4d;       // Gris oscuro
$color-hover: #f5531b;        // Naranja hover
```

### Espaciados
```scss
$space-xs: 0.25rem;
$space-sm: 0.5rem;
$space-md: 1rem;
$space-lg: 2rem;
$space-xl: 3rem;
```

### Tipografías
```scss
$font-base: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
$font-title: 'Playfair Display', serif;
```

## 🔧 Mixins Disponibles

```scss
// Flexbox centrado
@include m.flex-center

// Flexbox con espacio entre
@include m.flex-between

// Transiciones
@include m.transition($prop, $time)

// Media queries
@include m.responsive('mobile') { }
@include m.responsive('tablet') { }
@include m.responsive('desktop') { }

// Sombras
@include m.box-shadow

// Hover para botones
@include m.button-hover
```

## 🎬 Customización

### Cambiar los colores de la página

En `abstracts/variables.scss`:
```scss
$color-primary: #tu-color;      // Cambiar color principal
$color-secondary: #otro-color;  // Cambiar color secundario
```

### Añadir nuevas películas

En `index.html`, duplica un bloque `.card`:
```html
<div class="card">
    <img src="tu-imagen.jpg" alt="Nombre" class="card__image">
    <div class="card__content">
        <h3 class="card__title">Nombre Película</h3>
        <!-- ... resto del contenido -->
    </div>
</div>
```

### Crear nuevos componentes

1. Crea un nuevo archivo en `components/` (ej: `components/modals.scss`)
2. Define los estilos usando las variables y mixins
3. Importa en `layout/main.scss`:
```scss
@use "components/modals";
```

## 📊 Archivos Compilados

El archivo `styles.css` es el resultado de compilar `layout/main.scss`.

Para regenerarlo:
```bash
sass layout/main.scss styles.css
```

## 🌟 Tips de Desarrollo

- Usa las variables en lugar de valores hardcodeados
- Aprovecha los mixins para código DRY (Don't Repeat Yourself)
- Mantén la estructura de carpetas organizada
- Usa BEM para nombres de clases (`card__title`, `btn--primary`)

## 📄 Licencia

Libre para usar y modificar. 🎉

---

**Creado con ❤️ usando SASS**
