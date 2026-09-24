# Conference Finder

A prototype directory tracking when and where management, labor-relations, and HR / I–O psychology academic conferences convene next.

Hand-curated from each society's own site — not a live feed. Includes a clickable world map (real country borders via [D3.js](https://d3js.org/) + [topojson](https://github.com/topojson/topojson-client) + [world-atlas](https://github.com/topojson/world-atlas) data) for filtering the list by country.

## Files

- `index.html` — the page itself (single file, no build step)
- `countries-110m.json` — Natural Earth country boundary data (public domain), used to render the map

## Running locally

Just open `index.html` in a browser, or serve the directory with any static file server (needed for the map's `fetch()` call to work — opening the file directly via `file://` will not load the map data):

```bash
python3 -m http.server 8000
```

Then visit `http://localhost:8000`.
