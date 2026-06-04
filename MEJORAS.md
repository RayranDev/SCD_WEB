# Sunshine Coffee — Documento de Mejoras

> Análisis completo del sitio web. Prioridades, espacios vacíos pendientes de imagen, y mejoras técnicas.
> Última actualización: junio 2026

---

## Estado actual del sitio

El sitio tiene 10 secciones principales bien estructuradas: Hero, Origen (Dinastía), Proceso, Cold Brew, Historia Familiar, Cafetería, Migao, Menú, Eventos, Ubicación, CTA y Footer. El diseño base es sólido. Lo que falta es principalmente **contenido fotográfico real** en 4 secciones clave y algunos ajustes de experiencia móvil.

---

## ✅ Ya hecho

- **Mobile navbar**: Se añadieron íconos de Instagram y WhatsApp entre el logo y el botón de menú. Antes el espacio central estaba completamente vacío en mobile.

---

## 📸 Imágenes pendientes por colocar (orden de impacto)

### 1. MIGAO — sección `#migao` *(ALTA PRIORIDAD)*
**Ubicación en el código:** `<div class="blob-wrapper">[ DROP IMAGE: el Migao terminado ]</div>`

La sección del Migao es una de las más llamativas de la marca pero **no tiene foto del producto**. Es la única sección del menú con descripción visual y la más probable de convertir pedidos.

- **Qué foto poner:** El Migao completo armado — chocolate, galletas Ducales, almojábana y queso. Idealmente una foto de arriba (overhead) o en 3/4 con buena luz natural.
- **Dimensiones ideales:** 500×600 px mínimo, vertical u horizontal.
- **Cómo agregar:** Reemplazar el div `blob-wrapper` con `<img src="TU_IMAGEN" alt="El Migao · Sunshine Coffee" class="special-img">`.

---

### 2. TU MOMENTO — sección clock *(ALTA PRIORIDAD)*
**Ubicación en el código:** `<div class="moment-image-wrapper" ...>[ DROP IMAGE: ambiente cafetería · café al sol ]</div>`

Esta sección tiene el reloj en tiempo real que muestra una recomendación personalizada. Es muy interactiva pero visualmente está vacía del lado izquierdo.

- **Qué foto poner:** Foto de ambiente de la cafetería — una mesa con café al sol de mañana, o una ventana con luz entrando. Que transmita calma y calidez.
- **Dimensiones ideales:** 600×700 px, vertical. Puede tener grano o textura.
- **Cómo agregar:** Reemplazar el contenido del div con `<img src="TU_IMAGEN" alt="Ambiente Sunshine Coffee" class="moment-img">`.

---

### 3. EVENTOS — sección `#eventos` *(MEDIA PRIORIDAD)*
**Ubicación en el código:** `<div class="eventos-visual" ...>[ DROP IMAGE: barra de café · evento privado ]</div>`

La sección de eventos (bodas, corporativos, catering) tiene buen texto pero el visual está vacío. Es la sección de mayor ticket promedio.

- **Qué foto poner:** La barra de café montada en un evento, o una foto de la barista preparando café en un espacio decorado.
- **Dimensiones ideales:** 500×600 px, puede ser horizontal también.
- **Cómo agregar:** Reemplazar el div con `<img src="TU_IMAGEN" alt="Barra de café para eventos · Sunshine Coffee" class="eventos-img">`.

---

### 4. INSTAGRAM GRID — sección feed ✅ COMPLETADO
4 fotos reales embebidas en el bundle. Contador animado de likes y comentarios:
- Al hacer scroll a la sección los números suben de 0 al valor real (900ms)
- En desktop, hover reinicia el contador para volver a animar
- En mobile, overlay siempre visible y grid cambia a 2×2
- Fotos: "Bosa ya estamos aquí", barista en la barra, cold brew con laptop, fundadoras en café de la esquina

---

### 5. HISTORIA FAMILIAR — sección `#historia` *(BAJA PRIORIDAD)*
**Ubicación en el código:** `<div class="family-visual has-seal"><img src="91ed3469..." ...></div>`

Actualmente muestra el **sello de Dinastía** como imagen principal de la sección "Detrás de cada taza, hay tres generaciones." Sería mucho más emotivo con una foto real de la familia o la finca.

- **Qué foto poner:** Una foto de los abuelos, la finca en Boyacá, o los cultivos de café. Cualquier imagen que transmita historia y raíces campesinas.
- **Cómo agregar:** Reemplazar el `src` de la imagen existente con la nueva foto. El marco (`has-seal`) ya está estilizado.

---

### 6. TARJETAS DE PRODUCTO — sección origen *(BAJA PRIORIDAD)*
**Ubicación en el código:** Los divs `.product-visual.is-bag` muestran texto `"CAFÉ DE ORIGEN EN GRANO"` como placeholder visual.

Las tres tarjetas de producto (250g, 500g, Cold Brew) tienen placeholders estilizados en lugar de fotos de los empaques reales.

- **Qué foto poner:** Los empaques reales de Dinastía 250g, 500g y la botella de Cold Brew.
- **Cómo agregar:** Reemplazar el div `.product-visual` con una etiqueta `<img>` usando la clase `product-img`.

---

## 🛠 Mejoras técnicas / UX

### Prioridad Alta

| # | Mejora | Por qué |
|---|--------|---------|
| 1 | **Añadir `rel="noopener noreferrer"`** a todos los `target="_blank"` | Seguridad básica. Actualmente falta en varios enlaces de Instagram y WhatsApp. |
| 2 | **Meta OG tags** (Open Graph) | Al compartir el link en WhatsApp o redes sociales sale el texto del `<title>` genérico. Con `og:image`, `og:description` y `og:title` correctos, se mostraría la imagen del logo y el eslogan de la marca. |
| 3 | **Favicon real** | No hay favicon configurado. En la pestaña del navegador aparece el ícono genérico. Poner el logo circular de Sunshine Coffee como favicon `.ico` o `.png`. |

### Prioridad Media

| # | Mejora | Por qué |
|---|--------|---------|
| 4 | **Sección de reseñas / testimonios** | No hay ninguna sección de testimonios de clientes. Para una marca joven, esto construye confianza. Se puede añadir entre el Migao y el Menú, con 3-4 reseñas reales de Google o Instagram. |
| 5 | **Número de teléfono clickeable en mobile** | En el footer aparece `+57 300 371 4694` como texto plano. En mobile debería ser `<a href="tel:+573003714694">`. |
| 6 | **Lazy loading en imágenes** | Las imágenes grandes (menú, Cold Brew) deberían tener `loading="lazy"`. El mapa ya lo tiene, pero las imágenes no. |
| 7 | **Sección de suscripción mensual** | El texto de los productos menciona "suscribirte mensualmente" pero no hay ningún call-to-action específico para eso. Puede ser solo un formulario de WhatsApp. |

### Prioridad Baja

| # | Mejora | Por qué |
|---|--------|---------|
| 8 | **Galería de la finca / proceso** | La sección Proceso tiene 5 pasos textuales pero cero fotos del proceso real (cosecha, secado, tostión). Unas fotos de Boyacá harían la historia mucho más creíble. |
| 9 | **Botón "Subir arriba"** | En mobile, cuando el usuario llega al footer, no hay forma rápida de volver arriba. Un botón flotante o flecha mejoraría la navegación. |
| 10 | **Precio del Migao** | El Migao tiene toda su sección pero no muestra precio. Los usuarios tienen que preguntar por WhatsApp sin saber qué esperar. |

---

## 📋 Checklist rápido — imágenes por conseguir

```
[ ] Foto del Migao armado (overhead o 3/4)
[ ] Foto de ambiente cafetería (luz natural, mesa, ventana)
[ ] Foto de barra de café en evento montado
[ ] 4 fotos del Instagram para el grid del feed
[ ] Foto de la finca o abuelos para Historia Familiar
[ ] Foto de los empaques físicos de Dinastía 250g y 500g
[ ] Foto de la botella de Cold Brew real
[ ] Logo de Sunshine Coffee en formato .png fondo transparente (para favicon y OG)
```

---

## 🗂 Estructura de secciones del sitio

```
index.html
├── Navbar (sticky)
│   └── Mobile: logo | [IG + WA icons] ← recién añadido | hamburger
├── Hero · "Dos almas, una misma tradición"
├── Origen · Dinastía (productos + trust band)
├── Proceso · 5 pasos
├── Cold Brew · spotlight
├── Historia Familiar · 50 años + timeline
├── Café Divider · transición
├── Cafetería · Angie & Greyssi
├── Migao ← falta imagen
├── Menú · carta ilustrada (modal)
├── Tu Momento · reloj interactivo ← falta imagen
├── Eventos · catering ← falta imagen
├── Ubicación · mapa Google + horarios
├── CTA WhatsApp
├── Instagram Grid ← 4 placeholders
└── Footer
```

---

## 🔍 Auditoría SEO Completa · Junio 2026

### Estado actual implementado ✅

| Item | Estado | Detalle |
|------|--------|---------|
| `<meta name="description">` | ✅ | "Sunshine Coffee · Dos almas, una marca. Café de origen 100%..." |
| `<link rel="canonical">` | ✅ | `https://sunshine-dinastia.vercel.app/` |
| `<link rel="icon">` | ✅ | Logo circular del perro (UUID del bundle) |
| Open Graph (og:title, og:image...) | ✅ | Completo con imagen, descripción, locale es_CO |
| Twitter Cards | ✅ | summary_large_image configurado |
| JSON-LD LocalBusiness Schema | ✅ | CafeOrCoffeeShop con dirección, teléfono, horarios, coords |
| `<html lang="es">` | ✅ | Correcto |
| `<main>` semántico | ✅ | Envuelve todas las secciones de contenido |
| `.sr-only` + texto SEO en H1 | ✅ | Keywords ocultas para Google: "Café de Origen Colombiano, Boyacá, Bosa, Bogotá..." |
| Jerarquía H1→H2→H3 | ✅ | Path-titles cambiados de H3 a H2 |
| `rel="noopener noreferrer"` | ✅ | Los 15 enlaces externos corregidos |
| `href="tel:+573003714694"` | ✅ | Teléfono clickeable en footer |
| `loading="lazy"` en imágenes | ✅ | 13/15 imágenes (las 2 restantes son above-fold ✓) |
| Viewport meta | ✅ | width=device-width, initial-scale=1.0 |

---

### 🔴 Problemas técnicos pendientes

| # | Problema | Impacto | Acción |
|---|----------|---------|--------|
| 1 | **Dominio personalizado no configurado** | Alto | El sitio está en `sunshine-dinastia.vercel.app`. Registrar un dominio propio (`sunshinecoffee.com.co` o similar) mejora el branding y el SEO local de forma significativa. |
| 2 | **Sin sitemap.xml** | Alto | Google no tiene un mapa de todas las páginas. Para un sitio de una sola página con secciones tipo `#origen`, `#menu`, `#eventos`, agregar un sitemap con estas URLs de ancla ayuda a indexarlas. |
| 3 | **Sin robots.txt** | Medio | Vercel sirve uno genérico, pero tener uno propio permite controlar el crawl y declarar el sitemap. |
| 4 | **Sin Google Search Console configurado** | Alto | Sin GSC no hay datos de qué palabras generan impresiones, errores de rastreo, ni estado de indexación. Registrar el sitio es el primer paso real de SEO. |
| 5 | **Sin Google Analytics / GA4** | Medio | No hay medición de visitas, fuentes de tráfico ni comportamiento de usuario. |
| 6 | **Imágenes sin dimensiones declaradas** | Bajo | Las `<img>` sin `width` y `height` causan Layout Shift (CLS) — métrica de Core Web Vitals. |
| 7 | **Bundle de 24 MB** | Medio | El archivo único con todas las imágenes en base64 es pesado para la carga inicial. Impacta el LCP (Largest Contentful Paint). Considerar hospedar imágenes en Cloudinary o Vercel Image Optimization cuando se migre a un proyecto multi-archivo. |

---

### 🟡 Optimización de contenido

| # | Punto | Recomendación |
|---|-------|---------------|
| 1 | **Descripción meta poco específica** | Agregar palabras clave locales: "Bosa, Bogotá, Cundinamarca, café de especialidad" a la meta description. |
| 2 | **Textos alt en imágenes sin acento** | Algunas imágenes tienen alt con caracteres especiales mal codificados en el bundle. Verificar que sean legibles para lectores de pantalla. |
| 3 | **Contenido del Blog/Historias ausente** | Google premia el contenido fresco. Un blog simple con notas sobre el café de Boyacá, recetas de Cold Brew o la historia de la familia generaría tráfico orgánico. |
| 4 | **Reviews / Reseñas en la página** | No hay reseñas de clientes. Agregar 3-4 testimonios reales con marcado Schema `Review` ayuda al CTR en resultados de búsqueda. |
| 5 | **Precios en Schema** | Los productos (250g $28.000, 500g $52.000, Cold Brew $14.000) podrían marcarse con Schema `Product` + `Offer` para aparecer en Google Shopping. |

---

### 🟢 Sugerencias de mejora SEO · Siguiente nivel

| # | Mejora | Dificultad | Impacto |
|---|--------|------------|---------|
| 1 | Registrar en **Google Business Profile** | Baja | Muy Alto — aparece en Google Maps y "café en Bosa" locales |
| 2 | Registrar en **Google Search Console** | Baja | Muy Alto — monitoreo real de posicionamiento |
| 3 | Crear página en **Rappi / iFood** con descripción | Baja | Alto — fuente de tráfico y reseñas |
| 4 | Publicar el sitio en **directorios locales** (páginas amarillas, dónde comer Bogotá) | Baja | Medio |
| 5 | Agregar **Schema Product** para los productos de café | Medio | Alto |
| 6 | Crear una **landing page separada para Dinastía** | Alta | Medio-alto |
| 7 | Integrar **Instagram API** para mostrar posts reales en lugar de fotos estáticas | Alta | Medio |

---

### 🎯 Palabras clave recomendadas

#### Primarias (alta intención de compra)
```
café colombiano en grano Bogotá
café de origen Boyacá
café para regalo Bogotá
cold brew Bogotá domicilio
cafetería Bosa Bogotá
domicilio café Bosa
```

#### Secundarias (marca + producto)
```
Sunshine Coffee Bosa
Dinastía café Boyacá
café lavado quinta selección
cold brew flor de Jamaica
café artesanal Bogotá
barra de café eventos Bogotá
catering café corporativo Bogotá
```

#### Long tail (específicas, menos competencia)
```
café en grano de Boyacá para comprar online
cafetería con domicilio en Bosa Bogotá
barra de café para bodas Bogotá
café especial colombiano 250g regalo empresa
el Migao desayuno Bogotá
```

---

### 📋 Plan de acción SEO — Priorizado

#### Semana 1 (sin costo, alto impacto)
- [ ] **Crear cuenta en Google Search Console** y verificar el dominio de Vercel
- [ ] **Crear / completar Google Business Profile** con fotos, horarios y dirección exacta
- [ ] **Pedir reseñas** a los primeros clientes en Google Maps

#### Semana 2
- [ ] **Registrar dominio** personalizado (ej. `sunshinecoffee.co` o `sunshinecoffee.com.co`, ~$30.000 COP/año)
- [ ] Actualizar canonical y og:url al nuevo dominio
- [ ] Crear **sitemap.xml** básico con las secciones del sitio

#### Mes 1
- [ ] Subir el sitio a **Rappi** y directorios locales de Bogotá
- [ ] Agregar primeras **3-4 reseñas** de clientes en la sección de testimonios
- [ ] Instalar **Google Analytics 4** (gratuito) para medir tráfico

#### Mes 2-3
- [ ] Agregar Schema `Product` a los 3 productos del catálogo
- [ ] Publicar el primer **artículo de blog** (ej. "¿Qué es el café de quinta selección?")
- [ ] Evaluar migrar a un proyecto multi-archivo para separar imágenes del bundle
