# Astro website design library

A small Astro starter for hosting multiple independent website concepts in one project. The home page links to three designs. Website 1 is an empty design canvas ready for reference images and reusable Astro sections. Add more designs by creating a new `src/pages/website-N/` route and a matching `src/designs/website-N/` folder.

## Start locally

```sh
npm install
npm run dev
```

Build the static site with `npm run build` and preview it with `npm run preview`.

## Structure

```text
src/
  designs/
    website-1/sections/   # Reusable sections and styles for design 1
    website-2/sections/   # Reusable components and assets for design 2
    website-3/sections/   # Reusable components and assets for design 3
  layouts/                # Shared document layouts and SEO metadata
  pages/                  # URL routes (/, /website-1/, /website-2/, /website-3/)
  styles/                 # Global foundation styles
```

Each concept is available at `/website-1/`, `/website-2/`, or `/website-3/`. Its route page imports components from its own `src/designs/website-N/` folder. Update `site` in `astro.config.mjs` to the canonical production origin before deployment so generated URLs point to the real domain.
