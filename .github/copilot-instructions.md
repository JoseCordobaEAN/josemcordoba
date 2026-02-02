# Copilot Instructions — josemcordoba.com

This file gives targeted, actionable guidance for AI coding agents working on this repo.

Purpose

- Quickly orient agents to the app's architecture, workflows, and conventions so generated changes are correct and idiomatic.

Big picture

- Frontend SPA built with Vue 3 + Vite + TypeScript. Entrypoint: [src/main.ts](src/main.ts#L1).
- Router lives at [src/router/index.ts](src/router/index.ts#L1) — currently an empty route list; add routes here.
- Styling uses Tailwind; the compiled CSS is imported from [src/assets/tailwind.css](src/assets/tailwind.css).
- Dev server and build are handled by Vite; alias `@` -> `src` is defined in [vite.config.ts](vite.config.ts#L1).

Key files to inspect before making changes

- [package.json](package.json#L1) — scripts, dependencies, and Node engine requirements.
- [vite.config.ts](vite.config.ts#L1) — plugins (Vue, `vite-plugin-vue-devtools`) and aliases.
- [vitest.config.ts](vitest.config.ts#L1) — unit test environment (`jsdom`) and test root.
- [tailwind.config.js](tailwind.config.js#L1) — content globs for Tailwind scanning.
- [src/**tests**/App.spec.ts](src/__tests__/App.spec.ts) — example unit test pattern.

Developer workflows & commands

- Install: `npm install` (see `package.json`).
- Dev: `npm run dev` (runs `vite`).
- Build: `npm run build` (type-check + `vite build`).
- Preview production build: `npm run preview`.
- Type-check: `npm run type-check` (uses `vue-tsc` — important because `.vue` imports need `vue-tsc`).
- Unit tests: `npm run test:unit` (Vitest configured to use `jsdom`).
- Linting: `npm run lint` (runs `lint:*` — see `lint:oxlint` and `lint:eslint`).
- Formatting: `npm run format` (Prettier on `src/`).

Project-specific conventions

- Type checking: prefer `vue-tsc` for project-level checks rather than `tsc` (see `type-check` script).
- Linting: both `oxlint` and `eslint` are present; use the existing scripts to fix issues (`--fix` enabled).
- Test environment: Vitest uses `jsdom` in [vitest.config.ts](vitest.config.ts#L1) — write tests assuming DOM APIs are available.
- Routing: Router is initialized in `src/router/index.ts` with `createWebHistory(import.meta.env.BASE_URL)`; add route records to the `routes` array.
- Aliases: Use `@/` to import from `src` (configured in `vite.config.ts`) instead of relative import chains.

Integration points & external tools

- `vite-plugin-vue-devtools` is enabled for easier debugging during development (see `vite.config.ts`).
- Tailwind CSS v4 configured; content globs are in [tailwind.config.js](tailwind.config.js#L1).
- Vitest for unit tests; see [vitest.config.ts](vitest.config.ts#L1) for customizations.
- Prettier and ESLint (with `@vue/eslint-config-typescript`) are used for formatting and linting. Use provided npm scripts.

Guidelines for code-gen and patches

- Keep changes small and focused; run `npm run test:unit` and `npm run type-check` locally to validate.
- When adding imports prefer the alias form: `import Foo from '@/components/Foo.vue'`.
- When adding routes edit [src/router/index.ts](src/router/index.ts#L1) and add components under `src/`.
- For UI changes ensure Tailwind classes are used (project uses Tailwind utility-first styles).

Examples

- Add a route: edit `src/router/index.ts` and push `{ path: '/about', component: () => import('@/views/About.vue') }` into `routes`.
- Run tests: `npm run test:unit` (Vitest will run with `jsdom`).

If anything here is unclear or you want more detail (testing patterns, release steps, or component conventions), tell me which area to expand.
