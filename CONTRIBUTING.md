# Guía de Contribución

Gracias por tu interés en contribuir a **La Patrulla Canina**. Este documento proporciona directrices para contribuir al proyecto.

## Código de Conducta

Todos los contribuyentes deben respetar y mantener un ambiente profesional, inclusivo y respetuoso.

## ¿Cómo Contribuir?

### 1. Reportar Errores (Bugs)

Para reportar un bug, crea un issue en el repositorio con:

- **Título claro:** Descripción breve del problema
- **Descripción detallada:** Qué esperabas y qué sucedió
- **Pasos para reproducir:** Instrucciones paso a paso
- **Navegador/Device:** Donde ocurre el error
- **Screenshots:** Si es aplicable

**Plantilla:**
```markdown
## Descripción
[Descripción breve del bug]

## Paso para Reproducir
1. Ir a...
2. Hacer clic en...
3. Observar error

## Comportamiento Esperado
[Qué debería suceder]

## Comportamiento Actual
[Qué sucede realmente]

## Información del Sistema
- Navegador: Chrome 90
- OS: Windows 10
- Resolución: 1920x1080
```

### 2. Sugerir Mejoras (Features)

Para sugerir una nueva característica:

- Describe el caso de uso
- Explica la solución propuesta
- Menciona alternativas consideradas
- Proporciona ejemplos si es posible

### 3. Hacer Pull Requests

#### Preparación

```bash
# Clona el repositorio
git clone https://github.com/usuario/proyecto.git
cd proyecto

# Crea una rama para tu feature
git checkout -b feature/nombre-descriptivo

# O para bugs
git checkout -b bugfix/descripcion-bug
```

#### Desarrollo

1. **Cumple con la Guía de Estilo** (`STYLE_GUIDE.md`)
2. **Mantén commits limpios:**
   ```bash
   git commit -m "feat: Agregar nueva funcionalidad"
   # Otros prefijos: fix, docs, style, refactor, test, chore
   ```

3. **Prueba tu código:**
   - Testea en Chrome, Firefox, Safari, Edge
   - Verifica responsive design
   - Revisa accesibilidad

#### Enviando PR

```bash
# Haz push de tu rama
git push origin feature/nombre-descriptivo

# Crea Pull Request en GitHub
```

**En la descripción del PR incluye:**

- Qué cambios realizas
- Porqué los realizas
- Cómo probar los cambios
- Checklist de verificación:
  ```markdown
  - [ ] Mi código sigue el STYLE_GUIDE
  - [ ] He probado en múltiples navegadores
  - [ ] Actualicé la documentación
  - [ ] Agregué cambios al CHANGELOG
  ```

## Convenciones de Commits

Usa el formato Conventional Commits:

```
<tipo>(<alcance>): <descripción>

<cuerpo>

<pie>
```

### Tipos de Commit

- **feat:** Nueva característica
- **fix:** Corrección de bug
- **docs:** Cambios en documentación
- **style:** Cambios de formato (no lógica)
- **refactor:** Cambio de código sin cambiar función
- **test:** Agregar o actualizar tests
- **chore:** Cambios en herramientas/dependencies

### Ejemplos

```
feat(player): Agregar control de volumen
fix(mobile): Corregir zoom en iOS
docs: Actualizar instrucciones de instalación
style(css): Mejorar consistencia de transiciones
```

## Checklist de Calidad

Antes de enviar un PR, verifica:

### Código
- ✅ No hay código duplicado
- ✅ Nombres de variables significativos
- ✅ Funciones con propósito único
- ✅ Sin `console.log()` en producción
- ✅ Manejo de errores apropiado

### Estilos
- ✅ Sigue STYLE_GUIDE.md
- ✅ Indentación consistente
- ✅ Sin !important innecesarios
- ✅ Variables CSS para colores

### Accesibilidad
- ✅ Contraste WCAG AA
- ✅ Navegación por teclado funcional
- ✅ Alt text en imágenes
- ✅ Labels en formularios

### Rendimiento
- ✅ Imágenes optimizadas
- ✅ Sin memory leaks
- ✅ Lazy loading implementado
- ✅ Transiciones suaves (60 FPS)

## Proceso de Review

1. **Revisión de Código:** Verifica estilo y lógica
2. **Pruebas:** Valida funcionamiento
3. **Sugerencias:** Se realizan cambios si es necesario
4. **Aprobación:** Se da merge cuando está listo

## Pedir Ayuda

- 💬 Crea una Discussion para preguntas generales
- 🐛 Abre un Issue para reportar problemas
- 📧 Contacta al equipo para cuestiones privadas

## Licencia

Al contribuir, aceptas que tu código se publica bajo la misma licencia del proyecto.

## Recursos Útiles

- [STYLE_GUIDE.md](./STYLE_GUIDE.md) - Convenciones de código
- [README.md](./README.md) - Información del proyecto
- [CHANGELOG.md](./CHANGELOG.md) - Historial de cambios

---

**¡Gracias por contribuir!** 🎉

Tu ayuda hace que este proyecto sea mejor para todos.
