# josemcordoba.com — Jose Manuel Córdoba C

This repository contains the source for my personal website: a small Vue 3 + Vite single-page app showcasing my experience, projects and contact information.

About me

- I'm Jose Manuel Córdoba C. I've worked in IT since 2006 across roles including developer, manager, director and startup founder. This site surfaces my portfolio, writings, and ways to get in touch.

Project purpose

- Serve as a lightweight, fast personal site built with modern web tooling (Vue 3, Vite, Tailwind).
- Keep the content primarily static with a small SPA shell for navigation and future interactive widgets.

Quick developer guide

- Install dependencies:

```bash
npm install
```

- Run dev server (hot reload):

```bash
npm run dev
```

- Build for production (includes type-check):

```bash
npm run build
```

- Run unit tests (Vitest, `jsdom` environment):

```bash
npm run test:unit
```

- Lint and format:

```bash
npm run lint
npm run format
```

Key files & conventions

- Entry: `src/main.ts` mounts the app and registers the router.
- Router: `src/router/index.ts` — currently an empty `routes` array; add route records here.
- Styles: `src/assets/tailwind.css` and `tailwind.config.js` (Tailwind v4).
- Use `@/` alias for imports (configured in `vite.config.ts`).
- Type checking uses `vue-tsc`; prefer `npm run type-check` for CI-style checks.

Notes for contributors and AI agents

- Keep changes minimal and focused; run `npm run test:unit` and `npm run type-check` after edits.
- Prefer lazy-loaded route components for new pages, e.g. `{ path: '/about', component: () => import('@/views/About.vue') }`.
- Follow existing styling with Tailwind utility classes.
- See `.github/copilot-instructions.md` for AI-specific guidance and conventions.

If you'd like, I can expand the README with deployment instructions, content guidelines, or a summary of site routes and pages.
