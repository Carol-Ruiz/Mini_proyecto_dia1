# Mini_proyecto_dia1

Este archivo es un **landing page personal** sobre la experiencia que tengo esta organizada por secciones estructuradas con HTML semántico y enlazada con un archivo CSS externo.
#  Archivo HTML (`index.html`)



## 1. Estructura General del Documento

```html
<!DOCTYPE html>
<html lang="es">
<head>...</head>
<body>...</body>
</html>
```

- `<!DOCTYPE html>`: Define el tipo de documento como HTML5.
- `<html lang="es">`: Indica que el idioma del contenido es español.

---

## 2. `<head>`

Contiene metadatos y enlaces externos necesarios.

```html
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<meta name="description" content="...">
<title>Carol Andrea Ruiz Castañeda...</title>
<link rel="stylesheet" href="./_css/style.css">
```

- Define la codificación de caracteres, diseño responsivo y SEO.
- Vincula el archivo de estilos CSS.

---

## 3. `<header>` – Encabezado y Navegación

```html
<header class="header">...</header>
```

Contiene:
- `logo`: Título con el nombre de la persona.
- `nav.nav`: Navegación con enlaces internos a las secciones del sitio (Inicio, Sobre mí, Habilidades, Contacto).

---

## 4. Sección Hero (`#home`)

```html
<section id="home" class="hero">...</section>
```

Incluye:
- Un título principal.
- Descripción corta sobre el perfil profesional.
- Dos botones de acción: **Contactar** y **Ver Más**.

---

## 5. `<main>` – Contenido Principal

### Sección Sobre Mí (`#about`)

```html
<section id="about" class="about">...</section>
```

- Contenido textual con una presentación personal.
- Una imagen o espacio reservado con clase `placeholder-image` y una imagen `carol.png`.

### Sección Habilidades (`#skills`)

```html
<section id="skills" class="skills">...</section>
```

Incluye una grilla de tarjetas que describen habilidades técnicas:
- PHP
- HTML y CSS
- Bases de Datos
- Diseño Web

Cada tarjeta contiene:
- Título (`h3.skills-card__title`)
- Descripción (`p.skills-card__description`)

---

## 6. `<footer>` – Pie de Página (`#contact`)

```html
<footer id="contact" class="footer">...</footer>
```

Contiene:
- Título: “¿Trabajamos juntos?”
- Breve mensaje de disponibilidad.
- Enlace al perfil de GitHub como botón.

---

## Conclusión

El archivo HTML está  estructurado con etiquetas semánticas (`header`, `main`, `section`, `footer`)..


# CSS (`style.css`)

Este archivo define los estilos para la landing page personal, utilizando variables CSS (`:root`), diseño responsive, y clases organizadas por sección.

---

## 1. `:root` – Variables Globales

```css
:root {
    --color-primary: #6a25eb;
    --font-primary: system-ui, ...
    --space-sm: 1rem;
    ...
}
```

Define variables reutilizables:
- **Colores primarios**, de texto y fondo.
- **Tipografía**, pesos de fuente.
- **Espaciado**, tamaños responsivos.
- **Breakpoints** para media queries.

---

## 2. Reset y Base

```css
*, *::before, *::after {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
}
```

- Se eliminan márgenes y paddings por defecto.
- Se configura `box-sizing` para facilitar el diseño.

---

## 3. Tipografía y Layout

```css
html { font-size: 100%; scroll-behavior: smooth; }
body { font-family: var(--font-primary); ... }
.container { max-width: 1200px; margin: auto; padding: ... }
```

- Define estilos básicos y contenedor centrado y adaptable.

---

## 4. Títulos de Secciones

```css
.section__title {
    font-size: clamp(1.75rem, 4vw, 2.5rem);
    text-align: center;
}
```

- Tipografía adaptable para títulos como “Sobre mí” y “Habilidades”.

---

## 5. Header y Navegación

```css
.header { background-color: var(--color-primary); position: sticky; ... }
.nav__list { display: flex; gap: 2rem; }
.nav__link:hover { color: var(--color-primary); }
```

- Fondo fijo en la parte superior.
- Navegación horizontal con efecto hover.

---

### Responsive Navigation (móvil)

```css
@media (max-width: 767px) {
    .nav__list { flex-direction: column; }
}
```

---

## 6. Sección Hero

```css
.hero { background: linear-gradient(...); text-align: center; }
.hero__highlight { color: var(--color-primary); }
.hero__actions { display: flex; justify-content: center; }
```

- Fondo degradado.
- Botones con clases `.btn--primary` y `.btn--secondary`.

---

### Botones Responsivos

```css
.btn { padding: var(--space-sm) var(--space-lg); ... }
.btn--primary:hover { transform: translateY(-2px); }
```

- Botones con efectos de hover.
- Adaptados para móvil.

---

## 7. Sección “Sobre Mí”

```css
.about { background-color: #e9d8fd; }
.about__text p { font-size: 1.2rem; }
.placeholder-image { border: dashed; display: flex; }
```

- Fondo lila claro.
- Imagen de presentación con borde decorativo.

---

### Responsive Sobre Mí

```css
@media (max-width: 767px) {
    .about__content { flex-direction: column; }
}
```

---

## 8. Sección “Habilidades”

```css
.skills { background-color: #d7dae0; }
.skills__grid { display: grid; grid-template-columns: repeat(...); }
.skills-card { box-shadow: ...; transition: transform ... }
```

- Tarjetas con sombra, título y descripción.
- Grilla responsive (1, 2 o 4 columnas según ancho).

---

## 9. Footer

```css
.footer { background-color: var(--color-bg-dark); color: white; }
.footer__contact { display: flex; justify-content: center; }
.contact-link:hover { transform: translateY(-2px); }
```

- Fondo oscuro.
- Botón de contacto con animaciones.

---

## Conclusión

El CSS se le aplico un diseño moderno, responsivo y modular.El cual utiliza variables para facilitar el mantenimiento y media queries para adaptarse a diferentes dispositivos.

