# Frente a la sociedad — blog (prueba UF1846)

Blog personal en Astro. El tema es parar un momento y escribir sobre cosas que a menudo no se dicen en voz alta (emociones, salud mental, pasado, futuro…).

## Qué hace

- Home con presentación del proyecto
- Blog con listado, paginación y página de cada artículo
- Páginas de about y contacto
- Menú y pie comunes
- Panel de admin Decap CMS en `/admin` (para gestionar posts)

## Cómo probarlo

```sh
pnpm install
pnpm dev
```

Build:

```sh
pnpm build
pnpm preview
```

Para el CMS en local (si lo usas):

```sh
pnpm cms
```

Demo: https://hilarious-smakager-4328a2.netlify.app  
Repo: https://github.com/moussijoelle/blog-frente-a-la-sociedad

## Cómo lo construí

- Astro + Tailwind
- Posts en Markdown dentro de content collections (`src/content/`)
- Layout en `src/layouts/Layout.astro`, menú y footer en componentes
- Rutas del blog: listado, paginación (`blog/[page]`) y detalle (`blog/[id]`)
- Utilidades en `src/utils/blog.ts`
- Despliegue en Netlify (`netlify.toml`: `pnpm run build` → carpeta `dist`)
- Decap CMS configurado en `public/admin/`

## Cómo comprobarlo

No hay suite de tests. Reviso la home, el listado del blog, abro un artículo, about y contacto. Si toca el CMS, entro en `/admin` con el flujo que tengas configurado en Netlify Identity.

---

Moussi Joelle · [github.com/moussijoelle](https://github.com/moussijoelle)
