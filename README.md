# Es la Hora de Aprender - Podcast Tech

> Tecnologías, IA y el futuro del ecosistema digital analizado semanalmente por quienes están en la cancha.

[![YouTube](https://img.shields.io/badge/YouTube-FF0000?style=for-the-badge&logo=youtube&logoColor=white)](https://www.youtube.com/@EsLaHoraDeAprender_com?sub_confirmation=1)
[![Spotify](https://img.shields.io/badge/Spotify-1ED760?style=for-the-badge&logo=spotify&logoColor=white)](https://open.spotify.com/show/7o7JR0Un1jc6wev0VjNm0C)

**🌐 Live:** [eslahoradeaprender.com](https://eslahoradeaprender.com) | **v3.18.1**

![Performance](https://img.shields.io/badge/Performance-99-brightgreen?style=flat-square)
![Accessibility](https://img.shields.io/badge/Accessibility-97-brightgreen?style=flat-square)
![Best Practices](https://img.shields.io/badge/Best_Practices-98-brightgreen?style=flat-square)
![SEO](https://img.shields.io/badge/SEO-96-brightgreen?style=flat-square)

---

## 🎤 Anfitriones

- **[Salvador Arturo Ortiz Gonzalez](https://www.ortizgonzalez.salvadorarturo.com)** — Inversionista y emprendedor (Startup|VC|SAOG AI)
- **[Salvador Ortiz Torres](https://www ortiztorres.salvador.com)** — Experto en educación y talento digital
- **[Frank Ortiz Gonzalez](https://www.ortizgonzalez.frank.me)** — Estratega en IA y curador de tendencias

---

## 🚀 Stack

- **[Astro 5](https://astro.build)** — Content Collections + SSG
- **Tailwind CSS v4** — `@theme` con colores custom
- **TypeScript + Zod** — Schema tipado
- **Cloudflare Pages** — Deploy automático on push
- **Neo-Brutalismo** — Acid Green `#ccff00` + Electric Blue `#2d5bff`

---

## 📺 Episodios

9 episodios publicados. Ver todos: [eslahoradeaprender.com/episodios](https://eslahoradeaprender.com/episodios).

### Agregar un episodio

Crear `src/content/episodes/XX-slug.md` con frontmatter → push. Se genera automáticamente: página, sitemap, video-sitemap, RSS, navegación prev/next.

Workflow completo: [`docs/agent-add-new-episode.md`](docs/agent-add-new-episode.md) (también disponible como slash command `/new-episode` en Claude Code).

---

## 📂 Estructura

```
src/
├── content.config.ts              # Schema Zod (Content Collections)
├── content/episodes/              # Un .md por episodio
├── components/
│   ├── SiteHeader.astro
│   └── SiteFooter.astro
├── layouts/BaseLayout.astro       # SEO, schemas, fonts
├── pages/
│   ├── index.astro                # Homepage (YouTube facade pattern)
│   ├── episodios/[...slug].astro  # Ruta dinámica
│   ├── feed.xml.ts                # RSS dinámico
│   ├── video-sitemap.xml.ts       # Video sitemap dinámico
│   └── 404.astro
└── styles/global.css

public/
├── thumbnails/                    # WebP self-hosted (sm + full)
├── robots.txt
├── manifest.json
├── sw.js
└── og-image.jpg
```

---

## 🛠️ Comandos

```bash
npm install          # Instalar dependencias
npm run dev          # Dev server en localhost:4321
npm run build        # Build producción → ./dist/
npm run preview      # Preview local del build
npm run validate     # Validar build pre-deploy
```

---

## ⚡ Performance

| Métrica | Valor | Porcentaje |
|---------|-------|-----------|
| FCP | 2.5s | 95-100% |
| LCP | 2.5s | 75-89% |
| TBT | 0ms | 90-100% |
| CLS | 0.001 | 0-0.1 |
| PSI | 85-91 | 80-100% |

**Optimizaciones:**
- YouTube facade pattern (0 iframes en carga inicial, click-to-play)
- Google Fonts async (preload + onload, non-render-blocking)
- Thumbnails self-hosted WebP (29-33KB por card)
- Zero JavaScript bundle (solo facade script inline)

---

## 🌐 SEO

**Features:**
- Schema markup: PodcastSeries (global), PodcastEpisode + VideoObject + BreadcrumbList (por episodio)
- hreflang: es, x-default
- Geo tags: TIJUANA, BAJA CALIFORNIA, MEXICO
- Meta robots: `index, follow, max-image-preview:large, max-snippet:-1`
- RSS feed: [/feed.xml](https://eslahoradeaprender.com/feed.xml)
- Sitemaps: [index](https://eslahoradeaprender.com/sitemap-index.xml) · [video](https://eslahoradeaprender.com/video-sitemap.xml)
- Open Graph + Twitter Cards
- Canonical URLs por página
- Body Markdown de cada episodio indexable (renderizado via `<Content />`)

Roadmap público: [`ROADMAP.md`](ROADMAP.md).

---

## 📄 Licencia

MIT — Ver [LICENSE](LICENSE).
SAOG [LICENSE].

---

<p align="center">
  <strong>Hecho con ⚡️ desde Tijuana, Baja California, México, SAOG AI</strong>
</p>
