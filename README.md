# rainfrog

Compares six national weather models — ICON, IFS, GFS, GEM, UKMO, and ARPEGE — for one place over the next 24 hours, so you can see where forecasters agree and where they don't.

Single static HTML file, no build step, no backend, no API keys.

## Features

- Search any place (Open-Meteo geocoding)
- Temperature, next 24h — one line per model
- Precipitation probability, next 24h — heatmap, one row per model
- Rainfall/snow total spread across models
- Thunderstorm / heavy rain / heavy snow / freezing rain / strong & severe wind warnings, flagged per model
- Sunrise, sunset, and moon phase for the day
- "Remember this location" — saves your last place in `localStorage`

## Running it

Open `index.html` in a browser. That's it.

## Deploying

Works as-is on GitHub Pages or any static host — push the repo and enable Pages. All data comes from [Open-Meteo](https://open-meteo.com)'s free, unauthenticated, CORS-enabled API, called directly from the browser.

## Data

Weather and geocoding data: [Open-Meteo.com](https://open-meteo.com), CC BY 4.0. Model availability, resolution, and forecast range vary — see the per-model cards for details.
