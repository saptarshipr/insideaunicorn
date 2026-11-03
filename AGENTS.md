# insideaunicorn.com

Website for *Inside a Unicorn* by Saptarshi Prakash (Penguin Random House India).

## How this site works

- Plain static site. No build step, no framework, no package manager.
- Everything lives in `index.html` (markup and CSS together) plus the `images/` folder.
- Hosted on GitHub Pages from the `main` branch root. Every push to `main` goes live in about a minute.
- `CNAME` holds the custom domain. Do not delete or rename it, or the domain stops working.
- `.nojekyll` tells GitHub Pages to serve files as they are. Keep it.

## Design source

- Figma: https://www.figma.com/design/48M5ljMfROQcXXUBL2lo6x/Inside-a-Unicorn?node-id=233-184
- Desktop frame is 1280 wide (node 231:30). Mobile frame is 360 wide (node 232:62).
- Layout switches from desktop to mobile at 820px (`@media (max-width: 820px)`).
- Fonts: Gowun Batang (headings) and Google Sans Flex (body and buttons), both from Google Fonts.
- Colors: page `#f2f2f2`, text `#000`, body text at 60% black, highlight `#ff9900` with multiply blend. Text selection uses `#f29100` to match the highlight.

## Favicon

- `favicon.svg` is the source (from Saptarshi's design). Its background `#FF7700` is the default colour.
- A small script in the `<head>` of `index.html` picks a random colour on each page load and swaps it into the SVG favicon, never repeating the previous colour. Palette: `#FF7700`, `#7B16FF`, `#E02881`, `#00AC61`, `#0055FF`, `#00A1E0`.
- Static fallbacks in the default orange: `favicon.ico` (16, 32 and 48 px), `apple-touch-icon.png` (180), `icon-192.png` and `icon-512.png` (listed in `site.webmanifest`). Google Search, bookmarks and iPhone home screens use these, so they always show orange.
- To change the palette, edit the `colours` list in that script. To change the design, replace `favicon.svg` (keep `#FF7700` as the background fill) and regenerate the PNG and ICO files from it.

## Links used on the page

- Amazon (all three buttons): https://link.amazon/B0alZPqhm
- LinkedIn: https://www.linkedin.com/in/saptarshipr
- YouTube: https://www.youtube.com/@saptarshipr
- Instagram: https://www.instagram.com/saptarshiux/

If a link changes, update every occurrence in `index.html`.

## Rules for editing

- Keep it a single `index.html`. Do not add a framework or build tooling unless asked.
- Copy style: no em dashes, no Oxford commas.
- New images go in `images/`. Export at 2x the displayed size and save as `.webp` (keep `og-image.jpg` as JPG, since LinkedIn previews need it).
- Check both layouts before committing: 1280px wide and 360px wide.
- Commit with a short message that says what changed, then push to `main`.
