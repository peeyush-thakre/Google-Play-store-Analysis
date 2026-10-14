# Google Play Store Analytics Dashboard

An interactive dashboard built with HTML, CSS, JavaScript, and Plotly.js to explore the Google Play Store app catalogue.

## Dashboard features

- Responsive dashboard layout with consistent spacing for desktop, tablet, and mobile screens.
- KPI cards for app count, category count, average rating, and total listed installs.
- Interactive Plotly charts:
  1. Bubble chart: app size vs. rating.
  2. Category installs summary.
  3. Install snapshot by category.
  4. Stacked category summary by app type.
  5. Average rating and reviews by category.
  6. Installs and estimated paid-app revenue.
- Hover tooltips, zoom, pan, and chart toolbar controls provided by Plotly.

## Project files

Keep the following files together in the same project folder:

- `index.html` — dashboard page.
- `README.md` or `README.txt` — project documentation.
- `requirements.txt` — optional Python dependencies if you regenerate charts from data.

If you use the original project data to regenerate the charts, keep these CSV files in the project folder:
- `googleplaystore.csv`
- `User_Reviews_Google_Play.csv` (used for review sentiment information where available)

The supplied HTML file already contains the chart data, so the static dashboard can be opened without loading CSV files.

## How to run the dashboard

### Option 1: Open locally

1. Download or extract the project files.
2. Make sure `index.html` is in the project folder.
3. Open `index.html` in Chrome, Edge, or Firefox.
4. Keep an internet connection available because Plotly.js is loaded from a CDN.

### Option 2: Publish as a static website

You can host `index.html` using GitHub Pages or another static hosting service.

1. Put `index.html` in the repository's published root folder.
2. Enable the static-site hosting feature in the repository settings.
3. Open the published website URL and test it on desktop and mobile.

This is a static HTML dashboard. Streamlit is not required to run this `index.html` version.

## Requirements

### For viewing the static dashboard
- A modern browser (Chrome, Edge, Firefox, or Safari).
- Internet connection to load Plotly.js from `https://cdn.plot.ly/plotly-2.35.2.min.js`.

### Optional: Python environment for rebuilding charts
Install Python 3.10 or later, then run:

```bash
python -m pip install -r requirements.txt
```

The Python packages listed in `requirements.txt` are for data preparation and chart regeneration; they are not needed just to open the existing HTML dashboard.

## Data notes and limitations

- The standard Google Play Store catalogue does not include a reliable country-by-country install breakdown. The category installs chart is not a world choropleth.
- A single catalogue snapshot does not provide monthly historical installs. The time-series and stacked-area sections are snapshot-based alternatives, not genuine month-over-month history.
- For paid apps, listed price multiplied by installs is only a rough estimate. It is not verified revenue and does not include free-app advertising or in-app purchase revenue.
- Do not present these estimates as actual revenue or historical growth.

## Troubleshooting

- **Charts are blank:** Check that you have an internet connection, then reload the page. Open browser Developer Tools (`F12`) and check the Console for errors.
- **Layout looks cramped:** Use a current browser and refresh the page. The layout adjusts for smaller screens.
- **Dashboard does not update from CSV changes:** The current HTML contains an embedded chart snapshot. Rebuild/regenerate the HTML after changing the source data.
- **Need a true historical or geographic chart:** Add genuine dated snapshots or country-level install data before making those charts.

## Author

Peeyush Thakre

Google Play Store Data Analytics Internship Project
