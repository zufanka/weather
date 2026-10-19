# rainfrog

Compares six national weather models — ICON, IFS, GFS, GEM, UKMO, and ARPEGE — for one place over the next 24 or 72 hours, so you can see where forecasters agree and where they don't.

Single static HTML file, no build step, no backend, no API keys. `social-preview.png` is the Open Graph/Twitter card image (`social-preview.svg` is its source) — keep it next to `index.html` when deploying, since the page links to it with a relative path.

## Features

- Edit the location heading to search any place (Open-Meteo geocoding); choose a result with a click or the arrow keys and Enter, or press Escape to cancel
- Temperature and wind — a coloured hourly average curve over thin grey individual model forecasts (warm orange for temperature, blue for wind). Hover the average for values and model counts; select a model to focus the curve on it. Missing values are excluded from averages and gaps are not connected
- Wind direction — an arrow band under the wind chart points where the wind blows toward; fainter = more disagreement between models
- Precipitation probability, next 24h — heatmap, one row per model
- Sunshine and haze — compact stacked hourly heatmaps sharing one time axis: brighter yellow = more sun (model average), stronger blue-gray = more haze (CAMS aerosol optical depth, unaffected by model filters)
- Rainfall/snow total spread across models
- Thunderstorm / heavy rain / heavy snow / freezing rain / strong & severe wind warnings, flagged per model
- Sunrise, sunset, and moon phase for the day
- Sketch-style hero: editable location, remember toggle and 24h/72h switch, current temperature and condition with emoji icons. High/low, precipitation and sunshine totals cover the selected rolling 24h/72h window; current wind and today's sunrise/sunset/moon phase stay fixed. Weather values are averaged across available models and are unaffected by model filters
- "Remember this location" — saves your last place in `localStorage`

## Running it

Open `index.html` in a browser. That's it.

## Deploying

Works as-is on GitHub Pages or any static host — push the repo and enable Pages. All data comes from [Open-Meteo](https://open-meteo.com)'s free, unauthenticated, CORS-enabled API, called directly from the browser.

## Data

Weather, geocoding, and haze data: [Open-Meteo.com](https://open-meteo.com), CC BY 4.0. Haze (aerosol optical depth) is based on the [Copernicus Atmosphere Monitoring Service (CAMS)](https://atmosphere.copernicus.eu) — see the [CAMS attribution requirements](https://confluence.ecmwf.int/display/CKB/CAMS+Regional%3A+European+air+quality+analysis+and+forecast+data+documentation). Model availability, resolution, and forecast range vary — see the per-model cards for details.
