# Guía de Estilo Zoopa.es

## 1. Paleta de Colores

### Colores Primarios
- **Negro**: `#000000` - Textos principales, fondos de contraste
- **Blanco**: `#ffffff` - Fondos principales, textos sobre oscuro

### Colores Secundarios
- **Gris Azulado**: `#abb8c3` - Textos secundarios, elementos sutiles
- **Gris Oscuro**: `#32373c` - Fondos de botones, elementos UI

### Colores de Acento
- **Rojo Vivo**: `#cf2e2e` - CTAs principales, elementos importantes
- **Naranja**: `#ff6900` - Hover states, elementos interactivos
- **Verde**: `#00d084` - Estados positivos, confirmaciones

## 2. Tipografía

### Familia de Fuentes
```css
font-family: 'Barlow', -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif;
```

### Escala Tipográfica
- **Small**: `13px` - Metadatos, labels pequeños
- **Base**: `16px` - Texto de párrafo
- **Medium**: `20px` - Subtítulos
- **Large**: `36px` - Títulos de sección
- **X-Large**: `42px` - Títulos principales/hero

### Pesos de Fuente
- **Regular**: `400` - Texto de cuerpo
- **Bold**: `700` - Títulos, énfasis
- **Extra Bold**: `800` - CTAs, elementos destacados

## 3. Espaciado

### Sistema de Espaciado (basado en rem)
```css
--spacing-xs: 0.44rem;    /* 7px */
--spacing-sm: 0.88rem;    /* 14px */
--spacing-md: 1.5rem;     /* 24px */
--spacing-lg: 2.5rem;     /* 40px */
--spacing-xl: 3.75rem;    /* 60px */
--spacing-xxl: 5.06rem;   /* 81px */
```

### Layout
- **Block Gap**: `24px` entre elementos consecutivos
- **Content Width**: `800px` para contenido normal
- **Wide Width**: `1200px` para secciones amplias
- **Padding Contenedores**: `2rem` en móvil, `4rem` en desktop

## 4. Componentes UI

### Botones
```css
.btn-primary {
  background: #32373c;
  color: #ffffff;
  border: none;
  padding: 12px 24px;
  font-weight: 800;
  transition: all 0.3s ease;
}

.btn-primary:hover {
  background: #cf2e2e;
  transform: translateY(-2px);
}
```

### Cards de Proyecto
- Imagen de fondo: `1200x630px`
- Overlay semi-transparente sobre hover
- Título aparece/desaparece con transición de 0.5s
- Efecto scale en imagen al hover (1.05x)

### Navegación
- Header transparente inicial, sólido al scroll
- Adaptación dinámica de color (dark/light) según fondo
- Menú dropdown con transición suave
- Logo: versión blanco/negro según contexto

## 5. Breakpoints Responsivos

```css
/* Mobile First */
@media (min-width: 480px)  { /* Mobile Large */ }
@media (min-width: 768px)  { /* Tablet */ }
@media (min-width: 1024px) { /* Desktop */ }
@media (min-width: 1440px) { /* Large Desktop */ }
```

## 6. Patrones de Diseño de Landing Pages

### Estructura Típica de Página de Proyecto

1. **Hero Section**
   - Imagen de fondo full-width (1920x1080px)
   - Overlay con información del cliente
   - Servicios listados en pills/tags
   - Descripción breve del proyecto

2. **Contenido Descriptivo**
   - Bloques alternados de texto e imagen
   - Imágenes: ~1024x577px
   - GIFs animados para demostrar funcionalidad
   - Narrativa que contextualiza la solución

3. **Sección de Características**
   - Grid de 2-3 columnas
   - Iconos SVG personalizados
   - Títulos cortos + descripción breve

4. **Proyectos Relacionados**
   - Grid de 2-3 proyectos
   - Cards con imagen de fondo
   - Overlay con título y categoría
   - Hover effect que revela más información

5. **Footer con CTA**
   - Formulario de contacto/newsletter
   - Links de navegación
   - Social media icons

### Estructura de Página de Servicios

1. **Hero con Value Proposition**
   - Título principal grande
   - Subtítulo explicativo
   - CTA principal visible

2. **Grid de Servicios**
   - Layout de cards en 2-3 columnas
   - Icono/imagen a la izquierda
   - Título + descripción + link a la derecha
   - Hover: background scale (150%)

3. **Detalle de Servicio** (páginas individuales)
   - Video/imagen destacada
   - Metodología en pasos numerados
   - Testimonios/casos de uso
   - FAQs
   - CTA de contacto

## 7. Animaciones y Transiciones

### Tiempos de Animación
```css
--transition-fast: 0.2s;
--transition-normal: 0.3s;
--transition-slow: 0.5s;
--transition-carousel: 1s;
```

### Efectos Comunes
- **Hover en links**: Color change + font-weight increase
- **Card hover**: Scale image (1.05), fade in overlay
- **Scroll reveal**: Elements fade in from bottom
- **Header transition**: Transparent to solid background

### Lazy Loading
```css
img {
  contain-intrinsic-size: auto 300px;
  loading: lazy;
}
```

## 8. Imágenes y Media

### Tamaños Recomendados
- **Hero backgrounds**: 1920x1080px
- **Project cards**: 1200x630px
- **Content images**: 1024x577px
- **Service icons**: 3000x1500px (optimizados)
- **Logos**: 150x150px (GIF o PNG)

### Optimización
- Formato WebP con fallback a JPG
- Lazy loading habilitado
- Aspect ratio definido para evitar layout shift
- Overlays semi-transparentes para mejorar legibilidad de texto

## 9. Accesibilidad

- Contraste mínimo 4.5:1 para textos
- Focus states visibles en elementos interactivos
- Alt text descriptivo en imágenes
- Headings jerárquicos (H1 → H2 → H3)
- Skip links para navegación por teclado

## 10. Características Distintivas de Zoopa

- **Sistema de tono dinámico**: Header adapta colores según fondo de sección activa
- **Parallax sutil**: Elementos se mueven a diferentes velocidades al scroll
- **Carousel de proyectos**: Transiciones suaves entre items
- **Footer flotante**: Toggle de visibilidad con animación bottom
- **Modal de credenciales**: PDF download con formulario inline
- **Newsletter integrado**: Input simple + botón en footer
