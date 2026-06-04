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

### 4. INSTAGRAM GRID — sección feed *(MEDIA PRIORIDAD)*
**Ubicación en el código:** Los 4 divs `.insta-post` con fondos de degradado de colores.

El grid de Instagram muestra placeholders animados. Lo ideal es reemplazarlos con fotos reales del Instagram de la marca, o con las mejores fotos del catálogo.

- **Qué fotos poner:** Las 4 mejores fotos del Instagram `@sunshinecoffee11`. Idealmente: Cold Brew, el Migao, los empaques de café, una de ambiente.
- **Dimensiones:** Cuadradas, mínimo 400×400 px cada una.
- **Cómo agregar:** Reemplazar el `style="background:..."` de cada `.insta-post` con `<img src="TU_IMAGEN" alt="...">` dentro del div.

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
