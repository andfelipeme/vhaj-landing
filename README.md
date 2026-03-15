# VHAJ — Landing Page

Sitio web oficial de **VHAJ**, empresa de desarrollo de software con sede en Popayán, Colombia.

Construido con **Astro 6** aplicando las nuevas features de la versión: Fonts API, Live Content Collections, Content Security Policy y el adaptador de Cloudflare.

---

## 🚀 Stack tecnológico

| Tecnología       | Versión | Uso                          |
| ---------------- | ------- | ---------------------------- |
| Astro            | 6.x     | Framework principal          |
| Tailwind CSS     | 4.x     | Estilos (vía plugin de Vite) |
| TypeScript       | 5.x     | Tipado estricto              |
| Cloudflare Pages | —       | Deploy y hosting             |
| Bun              | 1.x     | Gestor de paquetes y runtime |

---

## 📁 Estructura del proyecto

```
vhaj-landing/
├── public/
│   └── favicon.svg              # Logo SVG de VHAJ
├── src/
│   ├── assets/
│   │   └── images/              # Imágenes del proyecto
│   ├── components/
│   │   ├── layout/
│   │   │   ├── Navbar.astro     # Barra de navegación global
│   │   │   └── Footer.astro     # Footer global
│   │   └── sections/
│   │       ├── Hero.astro       # Sección principal del inicio
│   │       ├── Services.astro   # Servicios que ofrece VHAJ
│   │       ├── Products.astro   # Productos propios de VHAJ
│   │       └── About.astro      # Equipo, misión y visión
│   ├── layouts/
│   │   └── BaseLayout.astro     # Layout base — incluye Navbar y Footer
│   ├── pages/
│   │   ├── index.astro          # / → Inicio
│   │   ├── services.astro       # /services → Servicios
│   │   ├── productos.astro      # /productos → Productos
│   │   └── nosotros.astro       # /nosotros → Nosotros
│   └── styles/
│       └── global.css           # Variables CSS + estilos globales
├── .env                         # Variables de entorno (no commitear)
├── .env.example                 # Plantilla de variables de entorno
├── astro.config.mjs             # Configuración de Astro
├── tsconfig.json                # Configuración de TypeScript
└── README.md                    # Este archivo
```

---

## 🎨 Sistema de diseño

### Paleta de colores

```css
--violet: #a78bfa /* Color primario — violeta */ --sky: #38bdf8
  /* Color secundario — celeste */ --dark: #07070f /* Fondo principal */
  --dark2: #0d0d1c /* Fondo cards */ --dark3: #13132a
  /* Fondo inputs y métricas */ --text: #f1f5f9 /* Texto principal */
  --muted: #8892a4 /* Texto secundario */ --border: rgba(167, 139, 250, 0.12)
  /* Bordes */;
```

### Tipografía

| Fuente  | Uso                                        |
| ------- | ------------------------------------------ |
| Syne    | Títulos, headings, logo, métricas          |
| DM Sans | Cuerpo de texto, descripciones, navegación |

### Regla de estilos

> **Tailwind para todo.** CSS en `<style>` solo para lo que Tailwind no puede hacer: `-webkit-background-clip` para gradientes en texto, `::after` / `::before` para pseudoelementos y `@keyframes` para animaciones.

---

## 🖥️ Páginas

| Ruta         | Componente       | Descripción                                |
| ------------ | ---------------- | ------------------------------------------ |
| `/`          | `Hero.astro`     | Presentación de VHAJ con card de métricas  |
| `/services`  | `Services.astro` | Los 4 servicios que ofrece la empresa      |
| `/productos` | `Products.astro` | VHAJ POS System y Mapi Ant                 |
| `/nosotros`  | `About.astro`    | Equipo, misión, visión y stack tecnológico |

---

## ⚙️ Instalación y desarrollo

### Requisitos

- [Bun](https://bun.sh) >= 1.0
- Node.js >= 22.12.0

### Instalar dependencias

```bash
bun install
```

### Variables de entorno

```bash
cp .env.example .env
```

### Correr en desarrollo

```bash
bun run dev
```

Abre [http://localhost:4321](http://localhost:4321) en tu navegador.

### Build de producción

```bash
bun run build
```

### Preview del build

```bash
bun run preview
```

---

## 🚀 Deploy en Cloudflare Pages

### Primera vez

1. Conecta el repositorio en [Cloudflare Pages](https://pages.cloudflare.com)
2. Configura el build:

```
Framework preset:  Astro
Build command:     bun run build
Build output:      dist/
```

3. Agrega las variables de entorno desde `.env.example`
4. Deploy 🚀

### Deploys automáticos

Cada `push` a `main` dispara un deploy automático en Cloudflare Pages.

---

## 📐 Convenciones del proyecto

### Nomenclatura de archivos

```
PascalCase   → componentes Astro     (Navbar.astro, Hero.astro)
camelCase    → variables y funciones (navLinks, currentPath)
kebab-case   → páginas y rutas       (nosotros.astro → /nosotros)
```

### Estructura de un componente

```astro
---
// src/components/sections/Ejemplo.astro
// Descripción breve del componente

// 1. Imports
// 2. Props con interface
// 3. Datos y lógica
---

<!-- HTML con clases Tailwind -->

<style>
  /* Solo lo que Tailwind no puede hacer */
</style>

<script is:inline>
  /* Solo interactividad simple del lado del cliente */
</script>
```

### Commits

```
feat:     nueva funcionalidad
fix:      corrección de bug
style:    cambios de estilos
refactor: refactorización de código
docs:     cambios en documentación
chore:    tareas de mantenimiento
```

---

## 📬 Contacto

- **WhatsApp:** [+57 333 238 2830](https://wa.me/573332382830)
- **Email:** devvhaj@gmail.com
- **Ubicación:** Popayán, Cauca 🇨🇴

---

## 📄 Licencia

© 2026 VHAJ. Todos los derechos reservados.
