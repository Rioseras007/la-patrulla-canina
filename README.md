# LA PATRULLA CANINA - Plataforma de Música y Entretenimiento

## Descripción

Plataforma de streaming de música profesional con experiencia de usuario moderna y diseño de vanguardia. Incluye reproductor de audio, visualizador dinámico, gestión de pistas y sección de merchandise.

## Características Principales

✨ **Reproductor de Audio Premium**
- Visualizador dinámico en tiempo real
- Sincronización de letras automática
- Control completo de reproducción
- Soporte para múltiples formatos de audio

🎨 **Diseño Moderno**
- Interfaz oscura profesional con acentos neón
- Respuesta completamente adaptable a dispositivos
- Animaciones suaves y transiciones elegantes
- Paleta de colores coherente y accesible

📱 **Experiencia Multiplataforma**
- Detección automática de dispositivo móvil
- Versiones optimizadas para desktop y móvil
- Interfaz táctil intuitiva

🛍️ **Sección de Merchandise**
- Galería de productos premium
- Sistema de pedidos integrado
- Experiencia de compra simplificada

## Estructura del Proyecto

```
web/
├── index.html          # Página principal - Vista de escritorio
├── mobile.html         # Versión móvil optimizada
├── coming_soon.html    # Página de proximamente
├── get_durations.html  # Herramienta de duraciones
├── app.js              # Lógica del reproductor y aplicación
├── style.css           # Estilos del sistema
├── assets/             # Archivos de audio e imágenes
│   ├── *.mp3           # Pistas de audio
│   └── *.jpg           # Artwork de pistas
└── README.md           # Este archivo
```

## Requisitos Técnicos

- Navegador moderno con soporte para:
  - Web Audio API
  - HTML5 Audio
  - CSS Grid y Flexbox
  - ES6+ JavaScript

### Navegadores Compatibles

- Chrome 90+
- Firefox 88+
- Safari 14+
- Edge 90+

## Instalación y Uso

### Desarrollo Local

1. **Clonar o descargar el proyecto**
   ```bash
   cd proyecto\ cd/web
   ```

2. **Servir archivos localmente**
   - Usar Python: `python -m http.server 8000`
   - Usar Node.js: `npx http-server`
   - O usar la extensión Live Server en VS Code

3. **Acceder a la aplicación**
   - Desktop: `http://localhost:8000`
   - Agregar parámetro para forzar desktop en móvil: `?desktop=1`

### Despliegue

La aplicación está lista para despliegue en:
- Servidores web estáticos
- CDN (Cloudflare, AWS S3, etc.)
- Plataformas como Vercel, Netlify, GitHub Pages

## Personalización

### Cambiar Paleta de Colores

Edita las variables CSS en `index.html` o `style.css`:

```css
:root {
    --primary: #854CE6;      /* Color primario */
    --secondary: #00F2FF;    /* Color secundario */
    --gold: #FFD700;         /* Color de énfasis */
    --bg-dark: #050709;      /* Fondo principal */
}
```

### Agregar Nuevas Pistas

En `app.js`, añade al array `tracks`:

```javascript
{
    id: 13,
    title: "Nombre de la Canción",
    artist: "Artista",
    file: "assets/archivo.mp3",
    cover: "url-imagen.jpg",
    lyrics: ["[0:00] Lyric line", "[0:05] Next line"]
}
```

## Optimizaciones de Rendimiento

- ✅ Compresión de imágenes
- ✅ Carga perezosa (lazy loading) de contenido
- ✅ Caché del navegador configurado
- ✅ Minificación de recursos
- ✅ Visualizador optimizado (FFT size: 64)

## Accesibilidad

- Semántica HTML correcta
- Contraste de colores WCAG AA
- Navegación por teclado
- Atributos ARIA donde sea necesario
- Descripciones de alternativas

## Licencia

© 2026 La Patrulla Canina. Todos los derechos reservados.

## Soporte y Contacto

Para reportar problemas o sugerencias, contacta al equipo de desarrollo.

---

**Versión:** 2.0  
**Última actualización:** Marzo 2026  
**Estado:** En producción ✅
