# 🚀 Guía Rápida - FlixHub

## Inicio Rápido

### 1️⃣ Ver la página ahora
- Abre el archivo `index.html` en tu navegador
- ✅ ¡La página ya está completamente funcional!

### 2️⃣ Si quieres editar los estilos

**Opción A: Sin instalar nada (Recomendado)**
1. Edita cualquier archivo `.scss` en la carpeta `scss/`
2. Usa una herramienta online como: https://jsoncrack.com/editor
3. O compila manualmente en: https://maelics.github.io/SassTranspiler/

**Opción B: Instalar SASS localmente**
```bash
npm install -g sass
sass --watch . --output . --style compressed
```

## 📂 Dónde Editar

| Archivo | Para |
|---------|------|
| `abstracts/variables.scss` | Cambiar colores, fuentes, espacios |
| `components/buttons.scss` | Editar estilos de botones |
| `components/cards.scss` | Editar tarjetas de películas |
| `layout/header.scss` | Editar navegación y encabezado |
| `layout/footer.scss` | Editar pie de página |
| `base/typography.scss` | Editar tipografías y textos |
| `index.html` | Añadir/editar películas y contenido |

## 🎨 Cambios Rápidos

### Cambiar color principal (Rojo Netflix)
```scss
// En: abstracts/variables.scss
$color-primary: #e50914;  // Cambiar por tu color
```

### Cambiar color de fondo
```scss
// En: abstracts/variables.scss
$color-bg: #141414;  // Cambiar por tu color
```

### Añadir película
```html
<!-- En: index.html, copia este bloque en .grid -->
<div class="card">
    <img src="imagen.jpg" alt="Título" class="card__image">
    <div class="card__content">
        <h3 class="card__title">Mi Película</h3>
        <div class="card__rating">
            <i class="fas fa-star"></i>
            <span style="margin-left: 0.5rem;">4.5/5</span>
        </div>
        <p class="card__description">Descripción aquí...</p>
        <div class="card__footer">
            <span class="card__year">2024</span>
            <button class="btn btn--primary">Ver</button>
        </div>
    </div>
</div>
```

## 🔧 Estructura SASS

```
abstracts/
├── variables.scss   → Variables globales
└── mixins.scss      → Funciones y mixins

base/
├── reset.scss       → Reset CSS
└── typography.scss  → Tipografías

components/
├── buttons.scss     → Botones
└── cards.scss       → Tarjetas

layout/
├── header.scss      → Encabezado
├── footer.scss      → Pie
└── main.scss        → Archivo principal (importa todo)
```

## 📝 Compiled CSS

El archivo `styles.css` se genera automáticamente del archivo `layout/main.scss`.

**Para regenerar después de cambios:**
```bash
sass layout/main.scss styles.css
```

## 💡 Tips

- Mantén las variables en `abstracts/variables.scss`
- Usa los mixins para código limpio
- Sigue la estructura BEM para clases CSS
- Los cambios en SCSS requieren compilar a CSS

## 🌐 Colores Disponibles

```
Primario:    #e50914  (Rojo Netflix)
Secundario:  #221f1f  (Negro)
Fondo:       #141414  (Negro profundo)
Texto:       #ffffff  (Blanco)
Acento:      #564d4d  (Gris)
Hover:       #f5531b  (Naranja)
```

## ✨ Características

✅ Responsive (Mobile, Tablet, Desktop)
✅ Dark Mode Netflix-style
✅ Tarjetas con hover effects
✅ Navegación sticky
✅ Botones interactivos
✅ Grid automático
✅ Código modular y escalable

---

**¿Necesitas ayuda?** Revisa `README.md` para documentación completa.
