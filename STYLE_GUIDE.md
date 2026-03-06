# Guía de Estilo y Convenciones

## Principios de Diseño

### Paleta de Colores Oficial

```
Primario:     #854CE6 (Púrpura Neón)
Secundario:   #00F2FF (Cyan Neón)
Énfasis:      #FFD700 (Oro)
Fondo:        #050709 (Negro Profundo)
Tarjeta:      #0f1219 (Gris Muy Oscuro)
Texto:        #FFFFFF (Blanco)
Texto Tenue:  #70757a (Gris Medio)
```

### Tipografía

- **Títulos:** Bebas Neue (display, decorativa)
- **Contenido:** Outfit (sans-serif elegante)
- **Pesos activos:** 300, 400, 600, 700, 900

## Convenciones de Código

### HTML

- Usar semantic HTML5 tags cuando sea apropiado
- Atributos alt en todas las imágenes
- IDs descriptivos en minúsculas con guiones
- Indentar con 4 espacios

```html
<!-- ✅ Correcto -->
<div id="track-list" class="list-container">
    <button id="play-button" class="btn btn-primary">
        Reproducir
    </button>
</div>

<!-- ❌ Incorrecto -->
<div id="TL" class="list">
    <button onclick="play()">Play</button>
</div>
```

### CSS

- Variables CSS para valores reutilizables
- Clases en minúsculas con guiones o camelCase
- Especificidad mínima necesaria
- Media queries al final o usando mobile-first

```css
/* ✅ Correcto */
.btn-primary {
    background: var(--primary);
    padding: 1.5rem 4rem;
    border-radius: 50px;
    transition: all 0.3s ease;
}

.btn-primary:hover {
    transform: scale(1.05);
    box-shadow: 0 10px 30px rgba(133, 76, 230, 0.5);
}

/* ❌ Incorrecto */
.button {
    background: #854CE6;
    border-radius: 50px;
}
```

### JavaScript

- camelCase para variables y funciones
- UPPERCASE para constantes
- Comentarios descriptivos en español
- Funciones con propósito único

```javascript
// ✅ Correcto
async function playTrack(track, element) {
    // Cambiar a la vista del reproductor
    switchView('view-player');
    
    // Inicializar contexto de audio
    setupAudioCore();
}

const MAX_VOLUME = 1.0;

// ❌ Incorrecto
async function pt(t, e) {
    switchView('view-player');
    setupAudioCore();
}
```

## Componentes Reutilizables

### Botones

```html
<!-- Primario -->
<button class="btn btn-primary">Reproducir</button>

<!-- Secundario -->
<button class="btn btn-secondary">Descargar</button>

<!-- Actualizado -->
<button class="btn btn-highlight">Especial</button>
```

### Tarjetas

```html
<div class="card">
    <div class="card-header">Título</div>
    <div class="card-body">Contenido</div>
    <div class="card-footer">Pie</div>
</div>
```

### Formularios

```html
<form class="form-group">
    <label for="nombre">Nombre</label>
    <input type="text" id="nombre" class="form-control">
    <input type="email" id="email" class="form-control">
</form>
```

## Performance

### Optimizaciones Recomendadas

✅ **Hacer:**
- Usar variables CSS para colores
- Minificar CSS y JS en producción
- Lazy loading para imágenes grandes
- Debounce en event listeners frecuentes
- Caché del navegador (META tags)

❌ **Evitar:**
- Estilos inline
- !important innecesarios
- Animaciones sin límite de FPS
- Consultas DOM repetidas sin caché
- Cargar todas las fuentes simultáneamente

### Benchmarks

- Tiempo de carga inicial: < 2s
- Time to Interactive: < 3s
- Lighthouse Score: > 80

## Accesibilidad

### Requisitos Mínimos

- Contraste WCAG AA en textos
- Navegación completa por teclado
- Atributos ARIA cuando sea necesario
- Alt text en todas las imágenes
- Focus visible en elementos interactivos

```html
<!-- ✅ Accesible -->
<button aria-label="Reproducir pista">
    <i class="fas fa-play"></i>
</button>

<!-- ❌ Inaccesible -->
<div onclick="play()">▶️</div>
```

## Versionado

Seguir Semantic Versioning (SemVer):
- **MAJOR:** Cambios incompatibles
- **MINOR:** Nuevas funcionalidades compatibles
- **PATCH:** Correcciones de bugs

Ejemplo: `v2.0.1`

## Proceso de Review

1. ✅ Validar HTML/CSS
2. ✅ Verificar accesibilidad
3. ✅ Testear en navegadores principales
4. ✅ Revisar performance
5. ✅ Documentar cambios

---

**Última actualización:** Marzo 2026
