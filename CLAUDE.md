# TW Tools — Total War Companion

Static companion app for Total War games. Built with Astro (SSG), vanilla JS, and CSS BEM.

## Commands

- `npm run dev` — dev server (localhost:4321)
- `npm run build` — production build to `dist/`
- `npm run preview` — preview production build

## Project structure

```
src/
  components/
    layout/          — shared components (Navbar, Footer, CrtOverlay)
    faction-picker/  — Faction Picker tool components
  layouts/           — HTML shell (Layout.astro)
  pages/             — routes (index.astro = Faction Picker)
  styles/            — global.css (all styles, BEM)
public/assets/       — game images (emblems, lords)
```

## Conventions

- **CSS**: single `global.css`, BEM naming (`.block__element--modifier`), CSS custom properties for theming
- **Components**: Astro `.astro` files, no framework (no React/Vue/Svelte)
- **Interactivity**: vanilla TypeScript in `<script>` tags, DOM manipulation via `getElementById`/`querySelector`
- **Data**: faction/DLC data hardcoded in components (pending refactor to shared data files)
- **Assets**: static images in `public/assets/`, referenced as `/assets/...`

## Tools

- **Faction Picker** (implemented): random faction draw with filters (alliance, DLC), exclusion pool, history
- **Battle Roller** (planned)
- **Tech Tree** (planned)
