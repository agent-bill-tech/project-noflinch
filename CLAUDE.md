# No Flinch — Band Landing Page

## Stack
- Astro 5 (static), Tailwind CSS v4 (CSS-based config via `@theme` in `src/styles/global.css`), Formspree (contact)
- Fonts: Bebas Neue (headings), Inter (body) via @fontsource

## Commands
- `npm run dev` — local dev server
- `npm run build` — static build to `dist/`

## Environment Quirks
- Windows username has special char (ö) — `create-astro` and some npm tools fail with EPERM. Scaffold manually instead.
- FFmpeg installed via winget (`Gyan.FFmpeg`) — not on PATH in bash, use full path: `"/c/Users/MikaelSköldefjord-No/AppData/Local/Microsoft/WinGet/Packages/Gyan.FFmpeg_Microsoft.Winget.Source_8wekyb3d8bbwe/ffmpeg-8.0.1-full_build/bin/ffmpeg.exe"`
- Video already optimized (9.4MB → 2.0MB, h264 crf=28, no audio, faststart)
- Puppeteer MCP server configured for browser automation/screenshots

## Key Files
- `src/styles/global.css` — Tailwind v4 theme tokens (brand colors, fonts)
- `src/components/Contact.astro` — Formspree form ID (`xqaeanwk` is placeholder, needs real ID)
- `pictures/` — original unprocessed assets (keep as source of truth)
- `src/assets/` — renamed copies used by Astro `<Image>` for optimization

## Conventions
- Astro `<Image>` for all images (auto WebP conversion + compression)
- SVG social icons inlined (Instagram, Spotify)
- Spotify artist ID: `7p21zvucmMrlGyepJmZQHV`
- Spotify track "Hunt You Down": `7c5OstKuyJsReh6LfPBj9E`
